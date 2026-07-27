# Taller — Integración API-Frontend

<!-- 📝 Instrucción: taller guiado por el instructor, en equipo. No es el proyecto real todavía —
     es la técnica en sí, sobre un endpoint de práctica, antes de aplicarla al backlog real. -->

## Objetivo

Practicar el patrón completo de consumo de API (carga/error/éxito, CORS, variable de entorno,
Docker multi-stage) sobre un endpoint sencillo, antes de aplicarlo a las pantallas principales
del proyecto real en `3-proyecto/`. Es la aplicación práctica de `1-teoria/01` y `1-teoria/03`.

## Duración estimada

90 minutos (dentro del bloque de Ambiente de Formación).

## Pasos

### 1. Elegir un endpoint de práctica (10 min)

- [ ] Elegir un endpoint ya existente y funcional del backend del proyecto (ej. listado de una entidad simple)
- [ ] Confirmar el payload real de la respuesta (documentación o prueba manual con curl/Postman)

### 2. Consumo con los tres estados (30 min)

- [ ] Implementar la llamada al endpoint desde una pantalla o componente de práctica
- [ ] Implementar el estado de carga (indicador visible mientras la petición está en curso)
- [ ] Implementar el estado de error (apagar el backend momentáneamente y verificar que se muestra)
- [ ] Implementar el estado de éxito (los datos reales renderizados)

### 3. CORS (15 min)

- [ ] Confirmar que el backend tiene CORS configurado para el origen del frontend
- [ ] Provocar el error de CORS a propósito (quitando el origen de la lista permitida) y confirmar que el navegador lo bloquea — para reconocer el error cuando aparezca en el proyecto real

### 4. Variable de entorno (10 min)

- [ ] Mover la URL base de la API a una variable de entorno del frontend
- [ ] Documentarla en `fe/.env.example`
- [ ] Confirmar que cambiar el valor de la variable cambia el destino de las peticiones, sin tocar código

### 5. Docker multi-stage (25 min)

- [ ] Escribir `fe/Dockerfile` con etapa de build y etapa de runtime
- [ ] Construir la imagen y confirmar que corre sirviendo los archivos estáticos
- [ ] Agregar el servicio `fe` a `docker-compose.yml` y correr `docker compose up` con los tres servicios

## Cierre del taller

Al terminar, el equipo tiene el patrón probado en un caso simple y puede aplicarlo directamente
a las historias reales del Sprint 5 en `3-proyecto/`, sin descubrir CORS o variables de entorno
a mitad del sprint.
