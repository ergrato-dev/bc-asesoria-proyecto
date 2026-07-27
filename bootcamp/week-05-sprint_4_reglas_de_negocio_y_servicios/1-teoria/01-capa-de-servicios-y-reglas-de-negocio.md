# Capa de Servicios y Reglas de Negocio

## 🎯 Objetivos

- Separar la lógica de negocio del código de los endpoints/controladores
- Distinguir validación de entrada de validación de dominio
- Modelar excepciones de dominio explícitas

## 📋 Contenido

### 1. Por qué el endpoint no es el lugar de la regla de negocio (Criterio RAP-3)

Es común que en el Sprint 3 (API CRUD) la lógica quede toda en el controlador: recibe la
petición, valida, decide, guarda, responde. Funciona para un CRUD simple, pero cada regla de
negocio nueva que se agrega ahí hace el endpoint más largo, más difícil de testear sin levantar
un servidor HTTP, y más difícil de reutilizar si dos endpoints distintos necesitan la misma
regla. La capa de servicios existe para que la regla de negocio se pueda leer, testear y
reutilizar sin depender del protocolo (HTTP, CLI, cola de mensajes) que la disparó.

### 2. Tres capas, tres responsabilidades

```
Endpoint/Controlador   →   Servicio                    →   Repositorio/Acceso a datos
(protocolo: HTTP,           (orquesta reglas de              (persistencia: SQL,
 request/response,          negocio del dominio)             ORM, queries)
 validación de entrada)
```

- **Endpoint**: traduce la petición HTTP a algo que el servicio entiende, y el resultado del
  servicio a una respuesta HTTP. No decide nada de negocio.
- **Servicio**: aplica las reglas de negocio. No sabe qué es un `request` HTTP ni un `status
  code`.
- **Repositorio**: lee y escribe datos. No decide si una operación está permitida.

### 3. Validación de entrada vs validación de dominio

| | Validación de entrada | Validación de dominio |
|---|---|---|
| **Pregunta que responde** | ¿El dato tiene el formato/tipo correcto? | ¿La operación está permitida por el negocio? |
| **Ejemplo** | El campo `email` es un string con formato de correo | Ese correo ya está registrado |
| **Dónde vive** | En el borde (endpoint, DTO de entrada) | En el servicio |
| **Cambia cuando** | Cambia el contrato de la API | Cambia una regla del negocio |

Mezclar ambas en el mismo bloque de código es la causa más común de que una regla de negocio
termine duplicada en dos endpoints distintos que hacen "casi lo mismo".

### 4. Excepciones de dominio

Una excepción de dominio representa una regla de negocio violada, no un error técnico. Se lanza
desde el servicio, con un nombre que describe la regla (`EmailAlreadyRegisteredError`, no
`ValidationError` genérico). El endpoint la captura y decide a qué código HTTP se traduce — el
servicio nunca sabe qué es un `404` o un `409`.

### 5. Ejemplo ilustrativo

> ⚠️ **Ejemplo ilustrativo — pseudocódigo, no ligado a ningún stack específico.** El objetivo es
> mostrar la separación de capas, no una sintaxis a copiar.

```
// Excepción de dominio: nombra la regla, no el mecanismo
class OrderAlreadyCancelledError extends DomainError { ... }

// Servicio: conoce las reglas de negocio, no conoce HTTP
service OrderService {
  function cancel(orderId):
    order = repository.findById(orderId)         // acceso a datos
    if order.status == "CANCELLED":
      throw OrderAlreadyCancelledError(orderId)   // regla de negocio
    order.status = "CANCELLED"
    repository.save(order)
    return order
}

// Endpoint: conoce HTTP, no conoce la regla de negocio
endpoint POST /orders/{id}/cancel:
  validate(id is UUID)                            // validación de entrada
  try:
    order = OrderService.cancel(id)
    return 200, order
  catch OrderAlreadyCancelledError:
    return 409, "Order already cancelled"          // el endpoint decide el status
```

### 6. Aplicación al proyecto real

<!-- 📝 Instrucción: aplicar en equipo sobre el código real del Sprint 3 -->

- [ ] Revisar los endpoints del Sprint 3: ¿alguno tiene una regla de negocio directamente en el controlador?
- [ ] Extraer esa lógica a un servicio, dejando el endpoint solo con protocolo + validación de entrada
- [ ] Nombrar al menos una excepción de dominio real del proyecto (no genérica)
- [ ] Confirmar en code review que el servicio no importa nada del framework HTTP

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para el patrón Service Layer y `5-glosario/README.md` para
el vocabulario completo de esta semana.
