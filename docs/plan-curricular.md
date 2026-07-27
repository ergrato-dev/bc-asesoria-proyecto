# 📐 Plan Curricular y Trazabilidad RAP

## Ficha del RAP

| Campo | Valor |
|---|---|
| **RAP** | Planear actividades de construcción del software de acuerdo con el diseño establecido |
| **Competencia** | Asesoría Desarrollo - Codificación |
| **Duración** | 9 semanas · 90 horas (10h/semana: 6h Ambiente de Formación + 4h Trabajo Autónomo) |
| **Población** | Cadena de formación — Técnico en Programación → Tecnólogo ADSO |
| **Meta de cierre** | ≥90% del código del proyecto real construido al final de la semana 9 |

---

## Saberes de Conceptos y Principios

| # | Saber | Dónde se cubre |
|---|---|---|
| 1 | **Informe de diseño**: interpretación, análisis | Semana 1 · `1-teoria/01-interpretacion-informe-diseno.md` |
| 2 | **Estándares de codificación**: plantilla de estándar de código (documentación de código, reglas de nombrado para variables, métodos, atributos, clases, tablas, campos, indentación) | Semana 1 · `1-teoria/05-estandares-de-codificacion.md` + [`docs/estandar-codigo-template.md`](estandar-codigo-template.md) |
| 3 | **Herramientas de apoyo**: versionamiento, control de cambios del código, integración continua | Semana 1 · `1-teoria/06-control-de-versiones.md`, `1-teoria/07-integracion-continua.md` + [`docs/git-workflow.md`](git-workflow.md), [`docs/ci-cd-guia.md`](ci-cd-guia.md) |

---

## Saberes de Proceso

| # | Saber | Semana de introducción | Reforzado en |
|---|---|:---:|---|
| 1 | Interpretar informe de diseño | 1 | Sprint Planning de cada semana 2-9 |
| 2 | Seleccionar herramientas de desarrollo | 1 | — (decisión de semana 1, no se repite) |
| 3 | Configurar herramientas de desarrollo | 1 | — (decisión de semana 1, no se repite) |
| 4 | Definir estándares de codificación | 1 | Code review de cada PR, semanas 2-9 |
| 5 | Seleccionar herramientas de versionamiento | 1 | — (decisión de semana 1, no se repite) |
| 6 | Configurar herramientas de versionamiento | 1 | Ajustes de flujo de ramas, semanas 2-9 según necesidad |

---

## Criterios de Evaluación

| # | Criterio | Instrumento principal |
|---|---|---|
| RAP-1 | Interpreta el informe de diseño para definir el plan de trabajo en la construcción del software | Backlog inicial (semana 1) + Sprint Planning semanal (semanas 2-9) |
| RAP-2 | Selecciona y configura herramientas de desarrollo de acuerdo con las condiciones del software a construir | Entorno de desarrollo configurado y documentado (semana 1) |
| RAP-3 | Define estándares de codificación de acuerdo con las reglas de la plataforma de desarrollo seleccionada | `CODING_STANDARDS.md` del proyecto real (semana 1) + cumplimiento verificado en cada PR (semanas 2-9) |
| RAP-4 | Selecciona y configura herramientas de versionamiento para el control de cambios en el código | Repositorio con flujo `feature → develop → main` operativo (semana 1) + disciplina de ramas/PR (semanas 2-9) |

---

## Tabla de Trazabilidad: Semana × Saberes × Criterios

| Semana | Tema | Saberes de proceso | Criterios (RAP) | Producto de la rúbrica ancla | Estado Docker esperado |
|---|---|---|:---:|---|---|
| 1 | Alistamiento acelerado y arranque | 1, 2, 3, 4, 5, 6 | RAP-1, RAP-2, RAP-3, RAP-4 | Repo configurado: backlog, entorno, `CODING_STANDARDS.md`, Git+CI operativos | Docker instalado, `Dockerfile` esqueleto |
| 2 | Sprint 1 — Dominio y persistencia | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Modelos de dominio y esquema de datos codificados | Servicio `db` en `docker-compose.yml` |
| 3 | Sprint 2 — Autenticación y autorización | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Login y control de acceso funcionando | Backend dockerizado, conectado a `db` |
| 4 | Sprint 3 — API CRUD de entidades core | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Endpoints principales del backlog codificados | API responde dentro del contenedor |
| 5 | Sprint 4 — Reglas de negocio y servicios | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Validaciones y capa de servicios codificadas | Servicios corren igual dentro y fuera del contenedor |
| 6 | Sprint 5 — Integración frontend-backend | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Pantallas principales consumiendo la API real | Frontend dockerizado, `docker compose up` levanta todo |
| 7 | Sprint 6 — Flujos y funcionalidades secundarias | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Casos de uso restantes del backlog codificados | Healthchecks y orden de arranque estables |
| 8 | Sprint 7 — Pruebas y manejo de errores | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Pruebas y manejo de errores sobre lo construido | Imágenes optimizadas, CI corre sobre contenedores |
| 9 | Sprint 8 — Cierre y avance 90% | 1, 4, 6 | RAP-1, RAP-3, RAP-4 | Proyecto ≥90% codificado, code review final | **Gate de entrega**: `docker compose up` end-to-end, sin alternativa |

> El Producto de la semana 9 no se acepta sin este gate — ver [`docker-guia.md`](docker-guia.md#checklist-de-verificación--semana-9-gate-de-entrega).

> Los saberes 2, 3 y 5 (selección/configuración de herramientas de desarrollo y versionamiento) son
> decisiones de una sola vez, tomadas y evidenciadas en la semana 1. No se repiten como criterio
> semanal — se auditan una vez y se dan por adquiridas, salvo que el equipo cambie de herramienta.

---

## Progresión de Sprints (Semanas 2-9)

Progresión sugerida para un proyecto backend + frontend típico (API REST + cliente web). No es
obligatoria — cada equipo la adapta a las historias de usuario reales de su backlog — pero da un
orden lógico por dependencias técnicas (no se puede autenticar sin dominio persistido, no se
integra frontend sin API, no se prueba a fondo sin funcionalidad completa):

1. **Dominio y persistencia** — modelos, esquema de base de datos, migraciones · Docker: `db` en compose
2. **Autenticación y autorización** — login, roles, control de acceso · Docker: backend dockerizado
3. **API CRUD de entidades core** — endpoints principales del backend · Docker: API en contenedor
4. **Reglas de negocio y servicios** — validaciones, capa de servicios, reglas del dominio · Docker: paridad local/contenedor
5. **Integración frontend-backend** — consumo de API, pantallas principales · Docker: frontend dockerizado, stack completo arriba
6. **Flujos y funcionalidades secundarias** — resto del backlog · Docker: healthchecks y orden de arranque
7. **Pruebas y manejo de errores** — testing, hardening, UX de errores · Docker: imágenes optimizadas
8. **Cierre y avance 90%** — deuda técnica, code review final, demo integrada · Docker: **gate de entrega obligatorio, sin alternativa**

> Progresión de contenerización detallada en [`docker-guia.md`](docker-guia.md).

---

## Documentos de Referencia

- [`guia-github-projects.md`](guia-github-projects.md) — backlog, sprints, plantillas de ceremonias ágiles
- [`estandar-codigo-template.md`](estandar-codigo-template.md) — plantilla de estándar de código que cada equipo completa según su stack
- [`git-workflow.md`](git-workflow.md) — flujo `feature/* → develop → main`, Conventional Commits
- [`ci-cd-guia.md`](ci-cd-guia.md) — configuración básica de GitHub Actions (lint + test en PR)
- [`docker-guia.md`](docker-guia.md) — contenerización gradual, obligatoria, gate de entrega en semana 9
