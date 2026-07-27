# Sprint Planning: Coordinación Backend-Frontend

## 🎯 Objetivos

- Planificar el Sprint 5 cuando el trabajo de backend y frontend ocurre en el mismo sprint
- Evitar bloqueos entre quien construye la API y quien la consume

## 📋 Contenido

### 1. Por qué este sprint necesita más coordinación (Criterio RAP-1)

En los sprints 1-4 el trabajo era mayormente backend. Este sprint depende de que **ambos lados
del contrato** avancen juntos: si el frontend espera un campo que el backend no envía, o un
código de error que el backend no distingue, el bloqueo aparece a mitad de semana, no en el
Sprint Review.

### 2. Qué se acuerda en el Sprint Planning de esta semana

Además de mover historias del `Backlog` al `Sprint Actual` (ver
[`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md#2-definir-sprints)),
este sprint agrega un acuerdo explícito por cada historia de integración:

- Payload exacto que el endpoint ya devuelve (o forma de consultarlo — la documentación existe desde el Sprint 3)
- Qué códigos de error puede devolver, y qué debe mostrar el frontend para cada uno
- Quién codifica cada lado, y en qué orden si hay dependencia real

### 3. Daily más corto, mismo formato

El Daily de esta semana usa la misma plantilla de siempre — ver
[`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md#4-plantillas-de-ceremonias) —
pero conviene que quien trabaja frontend reporte explícitamente si está bloqueado esperando un
endpoint, para que el equipo lo resuelva el mismo día, no al final del sprint.

### 4. Aplicación al proyecto real

<!-- 📝 Instrucción: completar en equipo durante el Sprint Planning -->

- [ ] Cada historia de integración movida al `Sprint Actual` tiene el contrato de su endpoint documentado o enlazado
- [ ] Está claro quién codifica backend y quién frontend por cada historia (o si es la misma persona)
- [ ] El equipo definió cuándo hace el Sprint Review con el instructor

## 📚 Recursos Adicionales

Ver `docs/guia-github-projects.md` para las plantillas completas de ceremonias ágiles.
