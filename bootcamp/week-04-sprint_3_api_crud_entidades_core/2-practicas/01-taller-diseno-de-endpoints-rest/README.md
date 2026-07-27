# Taller — Diseño de Endpoints REST

<!-- 📝 Instrucción: taller guiado por el instructor. Se resuelve sobre una entidad GENÉRICA
     (no la del proyecto real) para practicar la técnica antes de aplicarla en `3-proyecto/`. -->

## Objetivo

Diseñar en papel/markdown el CRUD completo de una entidad genérica — rutas, verbos, códigos de
estado, DTOs y paginación — antes de tocar el proyecto real. Es la aplicación práctica de
`1-teoria/01-diseno-de-endpoints-rest.md`.

## Duración estimada

45-60 minutos (dentro del bloque de Ambiente de Formación).

## Entidad de práctica

Usa una entidad genérica cualquiera, por ejemplo `Product` (o `Task`, `Course` — cualquiera fuera
del dominio real del proyecto), con al menos 4 campos, uno de los cuales sea interno (no debe
salir en el DTO de salida).

## Pasos

### 1. Diseñar las rutas y verbos (10 min)

- [ ] Escribir las 5 rutas del CRUD completo con su verbo HTTP correcto
- [ ] Marcar el código de estado de éxito de cada una

### 2. Elegir códigos de estado de error (10 min)

- [ ] Para cada endpoint, listar qué códigos de error puede devolver (`400`, `401`, `403`, `404`, `409` según aplique)
- [ ] Justificar en una línea por qué ese código y no otro

### 3. Separar DTOs del modelo de dominio (15 min)

- [ ] Escribir el modelo de dominio completo (todos los campos, incluido el interno)
- [ ] Escribir el DTO de entrada de creación — solo lo que el cliente puede enviar
- [ ] Escribir el DTO de salida — solo lo que el cliente debe ver
- [ ] Confirmar que el campo interno no aparece en ningún DTO expuesto al cliente

### 4. Paginar el listado (10 min)

- [ ] Escribir la firma del endpoint `GET` de listado con `page`/`page_size`
- [ ] Escribir la forma del cuerpo de respuesta paginado (`data`, `page`, `page_size`, `total`)
- [ ] Definir el `page_size` máximo permitido por el servidor

### 5. Puesta en común (10-15 min)

Cada equipo comparte su diseño en 2 minutos. El instructor revisa contra el checklist de cierre.

## Checklist de Cierre del Taller

- [ ] Las 5 rutas usan el verbo HTTP correcto, sin verbos en la URL (`/getItems` es incorrecto)
- [ ] Cada endpoint tiene su código de éxito y al menos un código de error justificado
- [ ] Ningún DTO de entrada o salida expone el campo interno del modelo de dominio
- [ ] El listado está paginado con un `page_size` máximo definido

Con este diseño resuelto en genérico, el equipo pasa directo a aplicarlo sobre las entidades core
del proyecto real en `3-proyecto/`.
