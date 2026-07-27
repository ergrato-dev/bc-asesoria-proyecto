# Sprint Planning del Sprint 1

## 🎯 Objetivos

- Descomponer "modelar el dominio y persistirlo" en tareas concretas del backlog
- Aplicar por primera vez, sobre un sprint real, el proceso definido en la semana 1

## 📋 Contenido

### 1. Este no es un tema nuevo — es la primera aplicación real

La planificación ágil (roles, ceremonias, backlog → sprint backlog) ya se definió en
`week-01/1-teoria/02-planificacion-agil-scrum-sprints.md` y en
[`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md). Esta semana no repite la
teoría — la aplica al primer sprint con código real.

### 2. Sprint Planning (30-45 min, inicio de la semana)

- Revisa el backlog priorizado (`entregable-s01-plan-de-trabajo.md` de la semana pasada)
- Crea el Milestone `Sprint 1 — Dominio y persistencia` en GitHub
- Mueve del `Backlog` al `Sprint Actual` **solo** las historias que dependen de tener el dominio
  modelado y persistido — típicamente las de menor dependencia técnica (ver
  `1-teoria/01-modelado-de-dominio.md`, sección 3)

### 3. De "modelar el dominio" a tareas de un issue

"Modelar el dominio" no es una tarea — es un objetivo de sprint. Se descompone en issues
accionables, por ejemplo:

```markdown
[HU-02] Como sistema, necesito persistir productos con su catálogo de atributos

## Criterios de Aceptación
- [ ] Entidad Product modelada con sus atributos (ver 1-teoria/01)
- [ ] Migración de la tabla/colección product, aplicable desde cero
- [ ] Servicio `db` levanta con `docker compose up db`
- [ ] PR revisado por un compañero, CI en verde, mergeado a develop
```

Cada issue así descompuesto ya es trazable a RAP-1 (interpretación del backlog), RAP-3 (aplicado
en review) y RAP-4 (flujo de PR) — la rúbrica de esta semana evalúa exactamente esto.

### 4. Code review guiado (dentro del bloque de Ambiente de Formación)

A diferencia de la semana 1 (donde el estándar solo se documentó), desde este sprint cada PR se
revisa contra `CODING_STANDARDS.md` real, con al menos un compañero aprobando antes del merge —
ver [`docs/git-workflow.md`](../../../docs/git-workflow.md#5-pull-request--develop). El
instructor guía la primera ronda de review de la semana para calibrar criterio del equipo.

### 5. Cierre: Sprint Review

El sprint no cierra con código mergeado silenciosamente — cierra con un Sprint Review documentado
en `3-proyecto/starter/entregable-s02-sprint-1-review.md`, usando la plantilla de
[`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md#sprint-review-con-instructor-fin-de-semana).

## 📚 Recursos Adicionales

Ver [`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md) para las plantillas completas de ceremonias.
