# Diseño de Endpoints REST

## 🎯 Objetivos

- Diseñar rutas y verbos HTTP correctos para un CRUD completo
- Elegir el código de estado correcto por caso, no uno genérico
- Separar los DTOs de entrada/salida del modelo de dominio
- Paginar los endpoints de listado

## 📋 Contenido

### 1. Verbos HTTP y rutas de un CRUD

Un CRUD completo sobre un recurso `items` se expresa así, sin importar el framework o lenguaje:

| Verbo | Ruta | Acción | Código de éxito |
|---|---|---|:---:|
| `GET` | `/items` | Listar (paginado) | 200 |
| `GET` | `/items/{id}` | Obtener uno | 200 |
| `POST` | `/items` | Crear | 201 |
| `PUT`/`PATCH` | `/items/{id}` | Actualizar (completo/parcial) | 200 |
| `DELETE` | `/items/{id}` | Eliminar | 204 |

Regla práctica: el recurso va en la ruta (sustantivo, plural), la acción la da el verbo HTTP — no
uses rutas como `/getItems` o `/deleteItem/{id}`.

### 2. Códigos de estado — el mínimo que hay que dominar

| Código | Significa | Cuándo usarlo |
|---|---|---|
| `200 OK` | Éxito con cuerpo de respuesta | `GET`, `PUT`/`PATCH` exitosos |
| `201 Created` | Recurso creado | `POST` exitoso, con el recurso creado en el cuerpo |
| `204 No Content` | Éxito sin cuerpo | `DELETE` exitoso |
| `400 Bad Request` | Petición inválida | Body mal formado, validación fallida |
| `401 Unauthorized` | Sin autenticación | Falta o expiró el token (ver semana 3) |
| `403 Forbidden` | Autenticado pero sin permiso | El rol no autoriza esa acción |
| `404 Not Found` | El recurso no existe | `id` inexistente en `GET`/`PUT`/`DELETE` |
| `409 Conflict` | Conflicto de estado | Ej. crear un recurso que ya existe por clave única |

Devolver siempre `200` con un campo `"error": true` en el cuerpo (en vez del código correcto) es
un antipatrón — rompe cualquier cliente HTTP estándar y el manejo de errores del frontend.

### 3. DTOs: separa lo que entra/sale de lo que persiste

El modelo de dominio (la entidad que se persiste) casi nunca debe exponerse tal cual en la API.
Un DTO (Data Transfer Object) de entrada valida y da forma a lo que llega; uno de salida controla
qué se expone.

```
# Ejemplo ilustrativo — agnóstico de framework/lenguaje

# Modelo de dominio (persistencia)
Item:
  id, name, price, cost, created_by_user_id, created_at, updated_at

# DTO de entrada (lo que el cliente puede enviar al crear)
ItemCreateDTO:
  name, price          # cost y created_by_user_id NO son responsabilidad del cliente

# DTO de salida (lo que el cliente recibe)
ItemResponseDTO:
  id, name, price, created_at   # cost queda oculto: es dato interno del negocio
```

Por qué importa: si el DTO de entrada fuera el modelo completo, cualquier cliente podría enviar
`cost` o `created_by_user_id` y falsificar datos que no le corresponden. Si el DTO de salida fuera
el modelo completo, expondrías campos internos sin darte cuenta.

### 4. Paginación

Ningún endpoint de listado devuelve la tabla completa. Patrón mínimo (offset/limit):

```
GET /items?page=1&page_size=20

# Respuesta
{
  "data": [ ... 20 items ... ],
  "page": 1,
  "page_size": 20,
  "total": 143
}
```

`page_size` debe tener un máximo razonable fijado por el servidor (ej. 100), no confiar en lo que
el cliente pida.

### 5. Idempotencia — por qué importa al elegir verbo

`GET`, `PUT`, `DELETE` deben ser idempotentes: ejecutarlos varias veces produce el mismo estado
final que ejecutarlos una vez. `POST` no lo es — cada llamada crea un recurso nuevo. Elegir mal el
verbo (ej. usar `POST` para actualizar) rompe esta expectativa para cualquier cliente que reintente
una petición fallida.

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para documentación de referencia sobre HTTP y OpenAPI.
Ver `5-glosario/README.md` para los términos usados en este documento.
