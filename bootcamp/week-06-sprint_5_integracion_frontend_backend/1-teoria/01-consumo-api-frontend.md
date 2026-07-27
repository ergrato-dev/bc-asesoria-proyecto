# Consumo de API desde el Frontend

## 🎯 Objetivos

- Consumir endpoints reales del backend desde las pantallas principales del frontend
- Manejar estado de carga y error sin dejar la interfaz inconsistente
- Configurar CORS y variables de entorno correctamente, sin URLs hardcodeadas

## 📋 Contenido

### 1. El contrato ya existe — no se inventa (Criterio RAP-1)

El backend de las semanas 2-5 ya define payloads, códigos de estado y errores. Consumirlo bien
significa leer ese contrato (documentación de la API, o el código de los endpoints) antes de
codificar la pantalla — no adivinar la forma de la respuesta.

### 2. Tres estados obligatorios en toda pantalla que llama a la API

Cualquier librería o patrón que use el equipo (fetch, axios, un cliente generado, un hook
propio) debe exponer, como mínimo:

| Estado | Qué muestra la UI |
|---|---|
| **Cargando** | Indicador de progreso — nunca una pantalla en blanco sin explicación |
| **Error** | Mensaje entendible por el usuario, no el stack trace crudo |
| **Éxito** | Los datos reales, ya renderizados |

### 3. Ejemplo ilustrativo (⚠️ no es código a copiar tal cual)

<!-- ⚠️ ILUSTRATIVO: pseudocódigo tipo JavaScript solo para mostrar el patrón de los 3 estados.
     No asume ninguna librería ni framework — adapta la sintaxis al stack real del equipo. -->

```javascript
// ⚠️ Ejemplo ilustrativo del patrón, no código de producción
async function loadOrders() {
  setLoading(true);
  setError(null);
  try {
    const response = await fetch(`${API_BASE_URL}/orders`);
    if (!response.ok) throw new Error(`API respondió ${response.status}`);
    setOrders(await response.json());
  } catch (err) {
    setError("No se pudieron cargar las órdenes. Intenta de nuevo.");
  } finally {
    setLoading(false);
  }
}
```

El punto no es la sintaxis — es que **loading**, **error** y **datos** son tres variables de
estado separadas, y las tres se actualizan en cada llamada.

### 4. CORS: quién lo configura y por qué falla

CORS lo autoriza el **backend**, no el frontend. Si el navegador bloquea la petición con un
error de CORS, el problema está en la configuración del servidor (lista de orígenes permitidos),
no en el código del cliente. Cada framework de backend tiene su propia forma de habilitarlo —
consulta la documentación oficial del framework elegido.

### 5. Variable de entorno para la URL de la API

La URL de la API **nunca** va hardcodeada en el código del frontend — cambia entre desarrollo,
Docker y producción. Se inyecta como variable de entorno (el mecanismo exacto depende del
framework de frontend: build-time o runtime), y se documenta en `fe/.env.example` junto al resto
de variables del proyecto (ver [`docs/docker-guia.md`](../../../docs/docker-guia.md)).

### 6. Aplicación al proyecto real

<!-- 📝 Instrucción: aplicar sobre las pantallas principales del backlog -->

- [ ] Cada pantalla que consume la API maneja carga, error y éxito por separado
- [ ] CORS configurado en el backend para el origen real del frontend (no `*` en producción)
- [ ] La URL base de la API viene de una variable de entorno, documentada en `fe/.env.example`
- [ ] Se probó desconectando el backend momentáneamente: la pantalla muestra el estado de error, no se congela

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para documentación oficial de fetch/axios y CORS.
