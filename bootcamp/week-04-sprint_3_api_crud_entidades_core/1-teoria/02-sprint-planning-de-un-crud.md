# Sprint Planning Aplicado a un CRUD Completo

## 🎯 Objetivos

- Descomponer el CRUD de una entidad core en tareas concretas por endpoint
- Mover del `Backlog` al `Sprint Actual` solo lo que el equipo puede completar en la semana (Criterio RAP-1)

## 📋 Contenido

### 1. Por qué no es "una tarea", son varias

Es un error común cargar el backlog con una sola tarea `"Implementar CRUD de items"`. Un CRUD
completo son mínimo 5 unidades de trabajo independientes, revisables por separado:

```
[ ] Endpoint POST /items (crear)
[ ] Endpoint GET /items (listar, paginado)
[ ] Endpoint GET /items/{id} (obtener uno)
[ ] Endpoint PUT/PATCH /items/{id} (actualizar)
[ ] Endpoint DELETE /items/{id} (eliminar)
```

Cada uno es un Issue propio en GitHub Projects, con su propia `feature/*` y su propio PR — no un
solo PR gigante con los cinco endpoints mezclados. Detalle del flujo completo en
[`docs/git-workflow.md`](../../../docs/git-workflow.md).

### 2. Sprint Planning de este sprint (30-45 min)

1. Revisar el backlog priorizado (definido en semana 1, `3-proyecto/starter/entregable-s01-plan-de-trabajo.md`)
2. Identificar qué entidad(es) core del backlog corresponden a este sprint según la progresión
   sugerida en [`docs/plan-curricular.md`](../../../docs/plan-curricular.md#progresión-de-sprints-semanas-2-9)
3. Descomponer cada entidad en sus 5 tareas por endpoint (ver arriba)
4. Asignar responsable por tarea — no por entidad completa, para permitir trabajo en paralelo
5. Mover los Issues resultantes de `Backlog` a `Sprint Actual`

### 3. Qué NO entra en este sprint

Reglas de negocio complejas (validaciones cruzadas, cálculos, transiciones de estado) se dejan
para la semana 5 (Sprint 4 — Reglas de Negocio y Servicios). Este sprint es CRUD directo: entrada
válida → persistencia → salida. Si una tarea empieza a acumular lógica de negocio, es señal de que
pertenece al siguiente sprint, no a este.

### 4. Definition of Done de cada tarea

La misma de siempre — sin atajos por ser "solo un CRUD":

- [ ] Endpoint cumple los criterios de aceptación del Issue
- [ ] DTOs de entrada/salida separados del modelo de dominio
- [ ] PR revisado por al menos un compañero, contra `CODING_STANDARDS.md`
- [ ] CI en verde (lint + test)
- [ ] Mergeado a `develop`

Ver Definition of Done completa en [`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md#5-definition-of-done).

## 📚 Recursos Adicionales

Ver `1-teoria/01-diseno-de-endpoints-rest.md` para el patrón técnico que estas tareas implementan.
