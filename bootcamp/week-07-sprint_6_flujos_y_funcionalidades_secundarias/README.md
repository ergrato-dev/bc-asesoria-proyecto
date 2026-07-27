# 📚 Semana 07 — Sprint 6: Flujos y Funcionalidades Secundarias

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Priorizar el backlog restante del proyecto real considerando las 3 semanas que quedan del bootcamp
2. Aplicar la técnica de "vertical slice" para completar casos de uso secundarios de punta a punta, sin dejar funcionalidades a medias
3. Ejecutar un Sprint Planning breve y disciplinado (30-45 min) sobre el backlog restante
4. Codificar los flujos y funcionalidades secundarias asignadas al Sprint 6, aplicando los estándares de codificación del proyecto
5. Mantener la disciplina de flujo `feature/* → develop` con PR revisado por al menos un compañero
6. Configurar `depends_on` con condición y healthchecks en `docker-compose.yml` para un orden de arranque estable
7. Cerrar el sprint con un Sprint Review documentado (avance acumulado, demo, PRs mergeados)

---

## 📋 Requisitos Previos

- Sprint 5 (integración frontend-backend) cerrado: pantallas principales consumiendo la API real
- Backlog en GitHub Projects actualizado con las historias de usuario restantes
- `docker-compose.yml` levantando backend + frontend + base de datos juntos (semana 6)

---

## 🗂️ Estructura de la Semana

```
week-07-sprint_6_flujos_y_funcionalidades_secundarias/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-priorizacion-backlog-y-vertical-slice.md
│   └── 02-depends-on-healthchecks-docker-compose.md
├── 2-practicas/
│   └── 01-taller-priorizacion-de-backlog-restante/   ← Checklist guiado, en equipo
├── 3-proyecto/
│   ├── README.md
│   └── starter/                           ← Plantilla de Sprint Review
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas)

```
🅰️ Ambiente de Formación      ████████████░░░░░░░   6h  (60%)
🅱️ Trabajo Autónomo           ████████░░░░░░░░░░░   4h  (40%)
```

### 🅰️ Bloque de Ambiente de Formación (6h — guiado)

1. **Sprint Planning breve (30-45 min)**: el equipo revisa el backlog restante y decide, con criterio, qué entra al Sprint 6 (ver `2-practicas/01-taller-priorizacion-de-backlog-restante/`)
2. **Teoría del patrón técnico** (`1-teoria/`): priorización de backlog en la recta final, vertical slice, `depends_on`/healthchecks
3. **Code review guiado**: revisión en equipo de los PR abiertos, con el estándar de codificación del proyecto (`CODING_STANDARDS.md`) como referencia

### 🅱️ Bloque de Trabajo Autónomo (4h)

Codificación del sprint sobre el proyecto real: las historias priorizadas en el Sprint Planning,
completas de punta a punta (vertical slice), no fragmentadas entre capas. Cierra con el **Sprint
Review**, usando la plantilla de [`docs/guia-github-projects.md`](../../docs/guia-github-projects.md#sprint-review-con-instructor-fin-de-semana).

---

## 📝 Contenidos

| # | Archivo | Tipo | Enfoque |
|---|---------|------|---------|
| 1 | `1-teoria/01-priorizacion-backlog-y-vertical-slice.md` | Teoría | RAP-1 |
| 2 | `1-teoria/02-depends-on-healthchecks-docker-compose.md` | Teoría | Docker (transversal) |
| 3 | `2-practicas/01-taller-priorizacion-de-backlog-restante/` | Taller guiado | Sprint Planning aplicado |
| 4 | `3-proyecto/` | Entregable real — Sprint 6 | RAP-1, RAP-3, RAP-4 |

---

## 📌 Entregable de la Semana

- [ ] Backlog restante priorizado: qué entra al Sprint 6 y qué se recorta, documentado y comunicado al equipo
- [ ] Casos de uso secundarios del Sprint 6 codificados completos (vertical slice, no a medias)
- [ ] Al menos un PR de `feature/*` mergeado a `develop`, revisado por un compañero, con CI en verde
- [ ] `docker-compose.yml` con `depends_on` con condición y healthchecks — `docker compose up` sin errores de orden de arranque
- [ ] Sprint Review completado

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s07-sprint-6-review.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Backlog restante** | Historias de usuario del informe de diseño aún no codificadas, a 3 semanas del cierre |
| **Vertical slice** | Caso de uso completado de punta a punta (UI + API + persistencia), usable de inmediato |
| **Scope creep** | Crecimiento no controlado del alcance del sprint sobre lo ya priorizado |
| **Deuda técnica** | Trabajo pospuesto a propósito para cumplir el sprint, que debe quedar registrado, no olvidado |
| **`depends_on` con condición** | Regla de Docker Compose que espera a que un servicio esté *sano* (`service_healthy`), no solo iniciado |
| **Healthcheck** | Comando que Docker ejecuta periódicamente para decidir si un contenedor está listo |
| **Code review** | Revisión de un PR por al menos un compañero antes de mergear a `develop` |

---

## ✅ Checklist de Verificación

- [ ] El backlog restante refleja una decisión real de priorización, no "todo entra a medias"
- [ ] Cada funcionalidad codificada esta semana está completa end-to-end (vertical slice)
- [ ] El PR fue revisado por al menos un compañero antes de mergear (no autoaprobado)
- [ ] `docker compose up` levanta todos los servicios sin reintentos manuales ni errores de orden de arranque
- [ ] El Sprint Review documenta el % de avance acumulado real del proyecto

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 06 — Sprint 5: Integración Frontend-Backend](../week-06-sprint_5_integracion_frontend_backend/README.md) | [Semana 08 — Sprint 7: Pruebas y Manejo de Errores →](../week-08-sprint_7_pruebas_y_manejo_de_errores/README.md) |

---

## 💡 Consejos para esta Semana

- **Prioriza sin culpa.** No todo el backlog restante cabe en 3 semanas — decide con el equipo qué se recorta y déjalo por escrito, no lo dejes caer en silencio.
- **Vertical slice sobre horizontal.** Mejor una funcionalidad secundaria completa que tres a medias — a medias no se puede demostrar ni evaluar.
- **El code review ya no es cortesía.** Es evidencia directa de estándares de codificación aplicados — no lo saltes por ir más rápido.
- **Healthchecks no son opcionales cuando el compose crece.** Sin ellos, "funciona en mi máquina" se rompe por timing de arranque, no por lógica de negocio.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 7 de 9*
