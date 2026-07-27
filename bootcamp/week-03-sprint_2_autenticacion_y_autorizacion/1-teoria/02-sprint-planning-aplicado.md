# Sprint Planning Aplicado al Sprint 2

## 🎯 Objetivos

- Interpretar el backlog priorizado para seleccionar las historias de autenticación/autorización de este sprint (RAP-1)
- Recordar la Definition of Done que rige cada PR del sprint (RAP-3, RAP-4)

## 📋 Contenido

### 1. Este no es un Sprint Planning desde cero

El proceso completo (roles, tablero, plantillas de ceremonias) ya se configuró en la semana 1 y
se aplicó en el Sprint 1. Esta semana solo se **ejecuta** de nuevo — no se vuelve a explicar Scrum.
Plantillas completas en [`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md).

### 2. Sprint Planning de esta semana (30-45 min, inicio del bloque de Ambiente de Formación)

- [ ] Revisar el `Sprint Review` del Sprint 1 (semana 2): ¿quedó algo pendiente que bloquea auth?
- [ ] Mover del `Backlog` al `Sprint Actual` solo las historias de autenticación/autorización que
      el equipo puede completar en esta semana
- [ ] Priorizar: login y hashing van antes que roles; roles van antes que permisos finos
- [ ] Asignar responsable por historia — mismo criterio de rotación de roles de semanas anteriores

### 3. Recordatorio de estándares en el código de este sprint (RAP-3)

El `CODING_STANDARDS.md` del proyecto ya existe desde la semana 1. En este sprint aplica en
particular a:

- Nombrado consistente de variables/campos sensibles (`password_hash`, no `pwd` o `p`)
- Manejo de errores de autenticación sin filtrar información (nunca "el usuario no existe" vs
  "contraseña incorrecta" como mensajes distintos — ambos casos responden igual)
- Cada PR de este sprint pasa **code review** de al menos un compañero antes de mergear, con foco
  explícito en que ningún secreto quedó hardcodeado (ver
  [`03-seguridad-basica-de-credenciales.md`](03-seguridad-basica-de-credenciales.md))

### 4. Recordatorio de flujo Git (RAP-4)

Sin cambios respecto a semanas anteriores: `feature/<slug>` desde `develop` actualizado, PR contra
`develop`, CI en verde, al menos una aprobación. Detalle completo en
[`docs/git-workflow.md`](../../../docs/git-workflow.md).

### 5. Aplicación al proyecto real

<!-- 📝 Instrucción: ejecutar en equipo, no leer solamente -->

- [ ] Sprint Planning de 30-45 min ejecutado y documentado en el tablero
- [ ] Historias del Sprint 2 visibles en la columna `Sprint Actual`
- [ ] Cada integrante sabe qué historia le toca y desde qué `feature/*` va a trabajar

## 📚 Recursos Adicionales

Ver [`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md#4-plantillas-de-ceremonias)
para la plantilla completa de Sprint Planning y Sprint Review.
