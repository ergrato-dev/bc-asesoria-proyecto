# Demo Integrada End-to-End

## 🎯 Objetivos

- Preparar una demo que recorra el flujo completo del proyecto, no funcionalidades sueltas
- Ejecutar la demo sobre la versión containerizada, tal como exige el gate Docker

## 📋 Contenido

### 1. Qué es una demo "integrada"

No es mostrar cada historia de usuario por separado. Es recorrer un flujo real de principio a fin
—como lo haría un usuario final— tocando la mayor cantidad de capas posible: autenticación,
persistencia, reglas de negocio, frontend, manejo de errores. Un buen flujo cruza varios sprints
del backlog en una sola secuencia de acciones.

### 2. Cómo prepararla

1. Elegir un flujo de usuario completo y representativo del proyecto (login → acción core → resultado persistido → verificación)
2. Levantar el proyecto con `docker compose up` — la demo se ejecuta ahí, no en local
3. Ensayar el flujo completo al menos una vez antes de la Sprint Review, cronometrado
4. Preparar un caso de error intencional (ej. dato inválido) para mostrar el manejo de errores, no solo el camino feliz
5. Tener a mano `docker compose logs` por si algo falla en vivo — no perder tiempo improvisando debugging frente al instructor

### 3. Qué NO hacer

- ❌ No demostrar sobre el entorno local del aprendiz "porque es más rápido" — invalida el gate
- ❌ No mostrar pantallas o endpoints sueltos sin conectarlos en un flujo
- ❌ No improvisar el orden en vivo — la demo se ensaya

## 📚 Recursos Adicionales

Ver la plantilla de Sprint Review en [`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md#4-plantillas-de-ceremonias).
