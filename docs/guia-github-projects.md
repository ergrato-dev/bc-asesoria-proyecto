# 📋 Guía de GitHub Projects

Herramienta ágil primaria del bootcamp. Si tu equipo ya usa Jira o ClickUp, esta guía aplica
igual — solo cambia dónde vive el tablero, no el proceso.

---

## 1. Crear el Backlog

1. En el repositorio del proyecto (no en este bootcamp), ve a la pestaña **Projects** → **New project** → plantilla **Board**.
2. Crea una columna por estado: `Backlog`, `Sprint Actual`, `En Progreso`, `En Revisión (PR)`, `Hecho`.
3. Convierte cada historia de usuario del informe de diseño (trimestre anterior) en un **Issue**:
   - Título: `[HU-XX] Como <rol>, quiero <acción> para <beneficio>`
   - Descripción: criterios de aceptación en checklist
   - Label: `feature`, `bug`, `chore`, `docs` según tipo
4. Todo issue entra primero a `Backlog`.

```markdown
<!-- 📝 Plantilla de Issue / Historia de Usuario -->
## Historia de Usuario
Como [rol], quiero [acción] para [beneficio].

## Criterios de Aceptación
- [ ] Criterio 1
- [ ] Criterio 2
- [ ] Criterio 3

## Notas técnicas
(Referencia al informe de diseño: sección/HU/RF que origina esta historia)
```

---

## 2. Definir Sprints

- Un sprint = 1 semana del bootcamp (semanas 2-9 = Sprints 1-8).
- Al inicio de cada sprint (Sprint Planning, ~30-45 min), el equipo mueve del `Backlog` al
  `Sprint Actual` solo lo que puede completarse esa semana.
- Usa un **Milestone** de GitHub por sprint (`Sprint 1 — Dominio y persistencia`, etc.) para
  agrupar los issues y medir velocidad.

---

## 3. Roles del Equipo

| Rol | Responsabilidad |
|---|---|
| **Scrum Master** | Facilita ceremonias, remueve bloqueos, cuida el proceso |
| **Product Owner (PO)** | Prioriza el backlog, valida criterios de aceptación |
| **Dev (Backend/Frontend)** | Codifica las historias asignadas |
| **QA** | Verifica criterios de aceptación antes de cerrar el issue |

En equipos pequeños, un mismo aprendiz puede rotar entre roles cada sprint — rotar es
recomendable para que todos practiquen Scrum Master y PO al menos una vez.

---

## 4. Plantillas de Ceremonias

### Daily (async o 10 min sincrónico)

```markdown
<!-- 📝 Completar antes de empezar a codificar cada sesión -->
**Ayer:** ¿Qué completé?
**Hoy:** ¿Qué voy a hacer?
**Bloqueos:** ¿Algo me está deteniendo?
```

### Sprint Review (con instructor, fin de semana)

```markdown
<!-- 📝 Preparar antes de la sesión con el instructor -->
## Sprint N — Review

**Objetivo del sprint:** ...
**Historias completadas:** (lista con enlace a PR mergeado)
**Historias no completadas:** (y por qué)
**Demo:** (qué se va a mostrar en vivo)
**% de avance acumulado del proyecto:** ...%
```

### Retrospectiva (15-20 min, cierre de sprint)

```markdown
<!-- 📝 El equipo, sin el instructor -->
## Sprint N — Retrospectiva

**¿Qué salió bien?**
- ...

**¿Qué no salió bien?**
- ...

**¿Qué vamos a cambiar en el próximo sprint?**
- ...
```

---

## 5. Definition of Done

Un issue solo pasa a `Hecho` cuando:

- [ ] El código cumple los criterios de aceptación de la historia
- [ ] El PR fue revisado por al menos un compañero
- [ ] El PR pasó CI (lint + test) — ver [`ci-cd-guia.md`](ci-cd-guia.md)
- [ ] El PR fue mergeado a `develop`
- [ ] No quedó código comentado, `console.log`/`print` de debug, ni TODOs sin issue asociado
