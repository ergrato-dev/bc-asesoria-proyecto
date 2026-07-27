# 📚 Semana 08 — Sprint 7: Pruebas y Manejo de Errores

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Interpretar el backlog restante para planificar el Sprint 7 (Sprint Planning breve)
2. Distinguir pruebas unitarias de pruebas de integración y priorizar cuáles escribir con tiempo limitado
3. Priorizar casos felices y casos límite al decidir qué probar primero
4. Implementar manejo consistente de errores en la API (formato de respuesta uniforme, códigos HTTP correctos)
5. Aplicar estándares de codificación del proyecto mediante code review guiado entre pares
6. Optimizar imágenes Docker con builds multi-stage y `.dockerignore`
7. Verificar que el pipeline de CI corra las pruebas contra las imágenes Docker reales, no solo en local
8. Documentar el Sprint Review con el estado de avance acumulado y el estado de Docker de la semana

---

## 📋 Requisitos Previos

- Semanas 1 a 7 completadas: dominio persistido, autenticación, API CRUD, reglas de negocio, frontend integrado, flujos secundarios y healthchecks de Docker operativos
- Backlog actualizado en GitHub Projects con las historias restantes hacia el 90% de avance
- Suite de pruebas existente del proyecto (aunque sea mínima) corriendo en CI

---

## 🗂️ Estructura de la Semana

```
week-08-sprint_7_pruebas_y_manejo_de_errores/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-pruebas-y-manejo-de-errores.md
│   └── 02-optimizacion-imagenes-docker.md
├── 2-practicas/
│   └── 01-taller-cobertura-de-pruebas-criticas/
├── 3-proyecto/
│   ├── README.md
│   └── starter/                           ← Plantilla de Sprint Review de esta semana
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## 📝 Contenidos

| # | Archivo | Tipo | Enfoque |
|---|---------|------|---------|
| 1 | `1-teoria/01-pruebas-y-manejo-de-errores.md` | Teoría | Unitarias vs integración, priorización con tiempo limitado, manejo consistente de errores |
| 2 | `1-teoria/02-optimizacion-imagenes-docker.md` | Teoría | Multi-stage builds, `.dockerignore`, CI contra imágenes reales |
| 3 | `2-practicas/01-taller-cobertura-de-pruebas-criticas/` | Taller guiado | Cobertura de los 5 flujos más críticos del proyecto real |
| 4 | `3-proyecto/` | Entregable real — Sprint 7 | Sprint Review + pre-checklist del gate de semana 9 |

---

## ⏱️ Distribución del Tiempo (10 horas)

Sprint normal — sin bloques especiales. La estructura es la misma de las semanas 2 a 7.

```
🅰️ Ambiente de Formación (guiado)   ██████████████░░░░░░   6h  (60%)
🅱️ Trabajo Autónomo (equipo)        █████████░░░░░░░░░░░   4h  (40%)
```

### 🅰️ Ambiente de Formación (6h)

1. **Sprint Planning** (30-45 min) — el equipo revisa el backlog restante, define el objetivo del Sprint 7 y mueve las historias de pruebas/errores/optimización que puede cerrar esta semana. Usa la plantilla de [`docs/guia-github-projects.md`](../../docs/guia-github-projects.md#4-plantillas-de-ceremonias).
2. **Teoría guiada** — `1-teoria/01-...md` y `1-teoria/02-...md`, en orden.
3. **Code review guiado** — el instructor y el equipo revisan en vivo un PR reciente del proyecto real contra `CODING_STANDARDS.md` (RAP-3), señalando qué se acepta y qué se corrige antes de mergear.
4. **Taller** — `2-practicas/01-taller-cobertura-de-pruebas-criticas/`.

### 🅱️ Trabajo Autónomo (4h)

El equipo codifica el Sprint 7 sobre el proyecto real: pruebas de los flujos críticos identificados en el taller, manejo de errores consistente en la API, optimización de `Dockerfile`s. Cierra con el **Sprint Review** (ver `3-proyecto/`).

> ⚠️ **Esta semana prepara el terreno para el gate de entrega de la semana 9.** Dejar las pruebas o la optimización de Docker "para después" no es una opción — la semana 9 es cierre y demo final, no tiempo para resolver deuda de la semana 8.

---

## 📌 Entregable de la Semana

Al final de la semana, el repositorio del proyecto real debe tener:

- [ ] Sprint Planning documentado (objetivo del Sprint 7, historias movidas del backlog)
- [ ] Al menos una prueba automatizada por cada uno de los 5 flujos críticos identificados en el taller
- [ ] Manejo de errores consistente en la API: formato de respuesta uniforme y códigos HTTP correctos en los endpoints principales
- [ ] Al menos un PR revisado en code review con estándares de `CODING_STANDARDS.md` aplicados, mergeado a `develop`
- [ ] `Dockerfile`(s) optimizados con build multi-stage y `.dockerignore` (ver [`docs/docker-guia.md`](../../docs/docker-guia.md))
- [ ] CI corriendo las pruebas contra las imágenes Docker reales, no solo en el entorno local
- [ ] Sprint Review documentado en `3-proyecto/starter/entregable-s08-sprint-7-review.md`

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s08-sprint-7-review.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Prueba unitaria** | Verifica una unidad de código aislada (función, método, clase) sin dependencias externas |
| **Prueba de integración** | Verifica que varias unidades (o la app y sus dependencias reales: BD, API) trabajen juntas correctamente |
| **Caso feliz** | Escenario donde todo ocurre como se espera, sin errores ni datos inválidos |
| **Caso límite** | Escenario en el borde de lo válido o fuera de él: entradas vacías, valores extremos, datos malformados |
| **Manejo consistente de errores** | Formato de respuesta uniforme ante fallos, con el código HTTP correcto según el tipo de error |
| **Multi-stage build** | `Dockerfile` con varias etapas `FROM`, donde solo la última pasa a la imagen final |
| **`.dockerignore`** | Lista de archivos/carpetas excluidos del contexto de build de Docker |
| **Imagen optimizada** | Imagen final sin dependencias de desarrollo, herramientas de build ni archivos innecesarios |

---

## ✅ Checklist de Verificación

- [ ] Los 5 flujos más críticos del proyecto tienen al menos una prueba automatizada, ejecutada en CI
- [ ] Los endpoints principales devuelven errores con formato y códigos HTTP consistentes (no un `500` genérico para todo)
- [ ] Al menos un PR de esta semana fue revisado por un compañero contra `CODING_STANDARDS.md`, con comentarios reales, no solo aprobado sin leer
- [ ] El `Dockerfile` de backend y/o frontend usa build multi-stage y la imagen final no incluye dependencias de desarrollo
- [ ] `.dockerignore` existe y excluye lo que no debe entrar al contexto de build (`node_modules`, `.git`, `.env`, etc.)
- [ ] El workflow de CI ejecuta las pruebas contra las imágenes Docker construidas, no contra el entorno del runner sin contenedor
- [ ] El Sprint Review quedó documentado con % de avance acumulado y enlaces a PRs mergeados

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 07 — Sprint 6: Flujos y Funcionalidades Secundarias](../week-07-sprint_6_flujos_y_funcionalidades_secundarias/README.md) | [Semana 09 — Sprint 8: Cierre y Avance 90% →](../week-09-sprint_8_cierre_y_avance_90/README.md) |

---

## 💡 Consejos para esta Semana

- **No pruebes todo, prueba lo crítico.** Con tiempo limitado, cubre primero los flujos donde un fallo rompería la operación del proyecto (login, pago, creación de la entidad principal), no cada getter trivial.
- **Un error mal manejado es peor que una funcionalidad faltante.** Un `500` sin contexto frente al usuario es una falla de UX tan real como un botón que no responde.
- **Docker optimizado hoy es tiempo ganado en la semana 9.** El gate de entrega no perdona un `docker compose up` lento o una imagen que falla por dependencias de desarrollo faltantes en producción.
- **El code review guiado de esta semana es evidencia de RAP-3.** No lo trates como trámite — es donde se verifica que los estándares definidos en la semana 1 se estén aplicando de verdad.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 8 de 9*
