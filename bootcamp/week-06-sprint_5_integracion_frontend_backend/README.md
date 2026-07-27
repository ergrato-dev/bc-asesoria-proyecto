# 📚 Semana 06 — Sprint 5: Integración Frontend-Backend

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Planificar el Sprint 5 a partir del backlog, coordinando el trabajo de quien construye backend con quien consume la API desde el frontend
2. Consumir los endpoints del backend real desde las pantallas principales del frontend
3. Manejar estados de carga y error en las llamadas a la API, sin dejar la interfaz "colgada" ni silenciar fallos
4. Configurar CORS en el backend para permitir el origen del frontend
5. Usar variables de entorno del frontend para apuntar a la URL de la API, sin URLs hardcodeadas
6. Dockerizar el frontend con un `Dockerfile` multi-stage (build → servidor estático/Nginx)
7. Levantar backend, frontend y base de datos juntos con un solo `docker compose up`

---

## 📋 Requisitos Previos

- Backend con reglas de negocio y capa de servicios codificadas (Semana 5), dockerizado y con paridad local/contenedor
- Endpoints CRUD de las entidades core respondiendo (Semana 4)
- Entorno frontend (`fe/`) seleccionado y configurado desde la Semana 1
- Docker y Docker Compose funcionando en la máquina de cada integrante

---

## 🗂️ Estructura de la Semana

```
week-06-sprint_5_integracion_frontend_backend/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-consumo-api-frontend.md
│   ├── 02-sprint-planning-integracion-fe-be.md
│   └── 03-docker-multistage-frontend.md
├── 2-practicas/
│   └── 01-taller-integracion-api-frontend/   ← Checklist guiado, mano a mano
├── 3-proyecto/
│   ├── README.md
│   └── starter/                              ← Plantilla de Sprint Review para tu proyecto real
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas)

```
🅰️ Ambiente de Formación   ████████████░░░░░░░   6h  (60%)
🅱️ Trabajo Autónomo        ████████░░░░░░░░░░░   4h  (40%)
```

### 🅰️ Ambiente de Formación (6h — guiado)

1. **Sprint Planning** (30-45 min): revisar el backlog, mover al Sprint Actual las historias de
   integración FE-BE que el equipo puede cerrar esta semana — plantilla en
   [`docs/guia-github-projects.md`](../../docs/guia-github-projects.md#4-plantillas-de-ceremonias)
2. **Teoría del patrón técnico** (`1-teoria/`): consumo de API, estados de carga/error, CORS,
   variables de entorno, Docker multi-stage del frontend
3. **Code review guiado**: el instructor revisa en vivo un PR de integración FE-BE de un equipo,
   aplicando `CODING_STANDARDS.md` (Criterio RAP-3)

### 🅱️ Trabajo Autónomo (4h)

Codificación del Sprint 5 sobre el proyecto real del equipo: cada integrante trabaja su
`feature/*` de integración, abre PR contra `develop`, pasa CI y revisión de un compañero antes de
mergear (Criterio RAP-4). Cierra con el **Sprint Review** — plantilla en `3-proyecto/`.

---

## 📝 Contenidos

| # | Archivo | Tipo |
|---|---------|------|
| 1 | `1-teoria/01-consumo-api-frontend.md` | Teoría — patrón técnico |
| 2 | `1-teoria/02-sprint-planning-integracion-fe-be.md` | Teoría — proceso |
| 3 | `1-teoria/03-docker-multistage-frontend.md` | Teoría — patrón técnico |
| 4 | `2-practicas/01-taller-integracion-api-frontend/` | Taller guiado |
| 5 | `3-proyecto/` | Entregable real — Sprint 5 Review |

---

## 📌 Entregable de la Semana

**Al final de la semana**, el repositorio del proyecto real debe tener:

- [ ] Al menos las pantallas principales del backlog consumiendo la API real (no datos mock)
- [ ] Manejo visible de estado de carga y de error en esas pantallas
- [ ] CORS configurado en el backend para el origen del frontend
- [ ] URL de la API leída desde variable de entorno del frontend, no hardcodeada
- [ ] `fe/Dockerfile` multi-stage funcional (build → servidor estático/Nginx)
- [ ] `docker compose up` levanta backend + frontend + base de datos juntos, por primera vez
- [ ] Al menos un PR de `feature/*` de integración mergeado a `develop`, con CI en verde y revisión de un compañero
- [ ] Sprint Review completado con el instructor

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s06-sprint-5-review.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **CORS** | Mecanismo del navegador que bloquea peticiones entre orígenes distintos salvo que el servidor lo autorice explícitamente |
| **Estado de carga (`loading`)** | Indicador de que una petición a la API está en curso, usado para no dejar la UI en blanco o inconsistente |
| **Estado de error** | Manejo explícito de una respuesta fallida de la API, mostrado al usuario, no silenciado |
| **Variable de entorno de frontend** | Valor de configuración (ej. URL base de la API) inyectado en tiempo de build o de arranque, no hardcodeado en el código |
| **Multi-stage build** | `Dockerfile` con varias etapas `FROM`; una compila, otra sirve solo el resultado, sin herramientas de build en la imagen final |
| **Servidor estático/Nginx** | Servidor liviano que sirve los archivos ya compilados del frontend en producción |

---

## ✅ Checklist de Verificación

- [ ] Las pantallas principales muestran datos reales del backend, no mocks ni datos quemados
- [ ] Existe feedback visible de carga y de error — probado desapagando el backend momentáneamente
- [ ] Ninguna URL de la API está hardcodeada en el código del frontend
- [ ] `fe/Dockerfile` construye una imagen final sin dependencias de desarrollo (multi-stage real, no una sola etapa)
- [ ] `docker compose up` en un clon limpio levanta los tres servicios (`db`, `be`, `fe`) sin pasos manuales
- [ ] El PR de integración fue revisado por al menos un compañero antes de mergear
- [ ] El Sprint Review se hizo con el instructor y quedó registrado en el tablero

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 05 — Sprint 4: Reglas de Negocio y Servicios](../week-05-sprint_4_reglas_de_negocio_y_servicios/README.md) | [Semana 07 — Sprint 6: Flujos y Funcionalidades Secundarias →](../week-07-sprint_6_flujos_y_funcionalidades_secundarias/README.md) |

---

## 💡 Consejos para esta Semana

- **No mockees lo que ya existe.** Si el backend responde, consume el endpoint real desde el primer momento — mockear retrasa descubrir problemas de CORS o de contrato de datos.
- **El estado de error no es opcional.** Una pantalla que se queda "congelada" cuando la API falla no pasa el criterio de Desempeño de esta semana.
- **Coordina antes de codificar.** Si backend y frontend los construyen personas distintas, acuerden el contrato del endpoint (payload, códigos de error) en el Sprint Planning, no a mitad de sprint.
- **El `docker compose up` completo es la prueba real.** Si solo corre "en mi máquina" fuera de Docker, el hito Docker de esta semana no está cumplido.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 6 de 9*
