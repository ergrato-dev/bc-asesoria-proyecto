# 📚 Semana 02 — Sprint 1: Dominio y Persistencia

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Interpretar el backlog priorizado de la semana 1 para definir el alcance del Sprint 1
2. Modelar el dominio del proyecto real: entidades, value objects, relaciones y cardinalidad
3. Diseñar un esquema de datos a partir del modelo de dominio, siguiendo el `CODING_STANDARDS.md` del proyecto
4. Escribir y aplicar migraciones de base de datos versionadas y reproducibles
5. Aplicar los estándares de codificación de la semana 1 en un code review real de PR
6. Mantener la disciplina de flujo `feature/* → develop`, con PR revisado y CI en verde
7. Levantar el servicio `db` en `docker-compose.yml`, con volumen persistente
8. Cerrar el sprint con un Sprint Review documentado y demostrado al instructor

---

## 📋 Requisitos Previos

- Repositorio del proyecto real configurado en la semana 1: backlog, stack decidido, `CODING_STANDARDS.md`, `develop` + branch protection, CI, Docker esqueleto
- `entregable-s01-plan-de-trabajo.md` completo, con backlog priorizado

---

## 🗂️ Estructura de la Semana

```
week-02-sprint_1_dominio_y_persistencia/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-modelado-de-dominio.md
│   ├── 02-esquema-de-datos-y-migraciones.md
│   └── 03-sprint-planning-del-sprint.md
├── 2-practicas/
│   └── 01-taller-modelado-de-dominio/     ← Calentamiento guiado, 20-45 min
├── 3-proyecto/
│   ├── README.md
│   └── starter/                           ← Plantilla de Sprint Review
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas)

```
🅰️ Ambiente de Formación     ████████████░░░░░░   6h  (60%)
🅱️ Trabajo Autónomo          ████████░░░░░░░░░░   4h  (40%)
```

### 🅰️ Ambiente de Formación (6h — guiado)

Sprint Planning breve (30-45 min) + `1-teoria/01` y `02` (patrón técnico del sprint) + taller de
calentamiento (`2-practicas/`) + arranque de la codificación real con code review guiado por el
instructor sobre el primer PR de la semana.

### 🅱️ Trabajo Autónomo (4h)

El equipo continúa la codificación del Sprint 1 sobre el proyecto real: modelo de dominio,
esquema, migraciones, servicio `db`. Cierra con el **Sprint Review** (ver `3-proyecto/`).

---

## 📝 Contenidos

| # | Archivo | Tipo | Cubre |
|---|---------|------|-------|
| 1 | `1-teoria/01-modelado-de-dominio.md` | Teoría | Patrón técnico del sprint |
| 2 | `1-teoria/02-esquema-de-datos-y-migraciones.md` | Teoría | Patrón técnico del sprint |
| 3 | `1-teoria/03-sprint-planning-del-sprint.md` | Teoría | Proceso — Sprint Planning aplicado |
| 4 | `2-practicas/01-taller-modelado-de-dominio/` | Taller guiado | Calentamiento de la técnica |
| 5 | `3-proyecto/` | Entregable real — Sprint 1 | Cierre con Sprint Review |

---

## 📌 Entregable de la Semana

Al final de la semana, el repositorio del proyecto real debe tener:

- [ ] Milestone `Sprint 1 — Dominio y persistencia` en GitHub, con historias movidas del `Backlog`
- [ ] Modelo de dominio del alcance del sprint documentado (entidades, value objects, relaciones)
- [ ] Esquema de datos codificado, con migraciones aplicables desde una base de datos vacía
- [ ] Servicio `db` en `docker-compose.yml`, con volumen persistente — `docker compose up db` funcional (ver [`docs/docker-guia.md`](../../docs/docker-guia.md))
- [ ] Al menos un PR de `feature/*` revisado por un compañero y mergeado a `develop`, con CI en verde
- [ ] Sprint Review documentado y presentado al instructor

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s02-sprint-1-review.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Dominio** | El área de negocio que el software modela |
| **Entidad** | Objeto con identidad propia que persiste en el tiempo |
| **Value Object** | Objeto definido solo por sus atributos, sin identidad propia |
| **Esquema de datos** | Definición estructural de tablas/colecciones, tipos y relaciones |
| **Migración** | Cambio de esquema versionado y reproducible |
| **Servicio `db`** | Contenedor de base de datos en `docker-compose.yml`, con volumen persistente |
| **Sprint Planning** | Ceremonia de inicio de sprint que define qué entra al `Sprint Actual` |
| **Sprint Review** | Ceremonia de cierre de sprint, demo de lo construido al instructor |

---

## ✅ Checklist de Verificación

- [ ] El modelo de dominio es trazable a historias reales del backlog, no inventado
- [ ] Las migraciones corren desde cero sin pasos manuales adicionales
- [ ] `docker compose up db` levanta la base de datos y los datos persisten tras `docker compose down` (sin `-v`)
- [ ] El PR mergeado esta semana fue revisado por al menos un compañero, no autoaprobado
- [ ] El commit sigue Conventional Commits y referencia el issue de la historia
- [ ] El Sprint Review quedó documentado antes de iniciar el Sprint 2

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 01 — Alistamiento Acelerado y Arranque de Código](../week-01-alistamiento_acelerado_y_arranque/README.md) | [Semana 03 — Sprint 2: Autenticación y Autorización →](../week-03-sprint_2_autenticacion_y_autorizacion/README.md) |

---

## 💡 Consejos para esta Semana

- **Modela antes de crear tablas.** Abrir el editor de base de datos sin haber nombrado entidades y relaciones es el error más común de este sprint — y el más caro de deshacer.
- **Una migración, un cambio conceptual.** No metas todo el esquema del sprint en una sola migración — dificulta revertir si el modelo cambia a mitad de semana.
- **El code review no es un trámite.** Es la evidencia real de RAP-3 esta semana — revisa contra `CODING_STANDARDS.md`, no solo "si compila".
- **`db` no es gate todavía.** Solo hace falta que levante con volumen persistente — el gate completo de Docker es en la semana 9.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 2 de 9*
