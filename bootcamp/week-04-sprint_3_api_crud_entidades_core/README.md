# 📚 Semana 04 — Sprint 3: API CRUD de Entidades Core

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Descomponer un CRUD completo del backlog en tareas concretas por endpoint (Sprint Planning)
2. Diseñar endpoints REST con verbos HTTP, rutas y códigos de estado correctos
3. Separar los DTOs de entrada/salida del modelo de dominio
4. Implementar paginación en los endpoints de listado
5. Codificar los endpoints principales del backlog sobre el proyecto real, con PR revisado y mergeado a `develop`
6. Verificar que la API responde dentro del contenedor Docker, configurada por variables de entorno

---

## 📋 Requisitos Previos

- Semana 3 completada: login y control de acceso funcionando, backend dockerizado y conectado a `db`
- Modelos de dominio y esquema de datos de la semana 2 ya persistidos
- `CODING_STANDARDS.md` y flujo `feature/* → develop` operativos (semana 1)

---

## 🗂️ Estructura de la Semana

```
week-04-sprint_3_api_crud_entidades_core/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-diseno-de-endpoints-rest.md
│   └── 02-sprint-planning-de-un-crud.md
├── 2-practicas/
│   └── 01-taller-diseno-de-endpoints-rest/
├── 3-proyecto/
│   ├── README.md
│   └── starter/
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas)

```
🅰️ Ambiente de Formación   ██████████████░░░░░░   6h  (60%)
🅱️ Trabajo Autónomo        ██████████░░░░░░░░░░   4h  (40%)
```

### 🅰️ Ambiente de Formación (6h — guiado por el instructor)

- **Sprint Planning (30-45min)**: el equipo descompone el CRUD de sus entidades core en tareas
  por endpoint, mueve las tareas del `Backlog` al `Sprint Actual` en GitHub Projects
- **Teoría del patrón técnico**: `1-teoria/01-diseno-de-endpoints-rest.md` — diseño de endpoints,
  DTOs, paginación, códigos de estado
- **Taller guiado**: `2-practicas/01-taller-diseno-de-endpoints-rest/` — aplicar el patrón antes
  de tocar el proyecto real
- **Code review guiado**: revisión en vivo de al menos un PR del sprint anterior o del avance
  parcial de este sprint, con foco en `CODING_STANDARDS.md`

### 🅱️ Trabajo Autónomo (4h)

Codificación del sprint sobre el proyecto real: los endpoints CRUD asignados en el Sprint
Planning, con commits siguiendo Conventional Commits, PR contra `develop` revisado por al menos
un compañero y CI en verde.

Cierra con el **Sprint Review** (plantilla en [`docs/guia-github-projects.md`](../../docs/guia-github-projects.md#sprint-review-con-instructor-fin-de-semana)) — ver `3-proyecto/`.

---

## 📝 Contenidos

| # | Archivo | Tipo | Enfoque |
|---|---------|------|---------|
| 1 | `1-teoria/01-diseno-de-endpoints-rest.md` | Teoría | Verbos HTTP, códigos de estado, paginación, DTOs |
| 2 | `1-teoria/02-sprint-planning-de-un-crud.md` | Teoría | Descomponer un CRUD en tareas por endpoint |
| 3 | `2-practicas/01-taller-diseno-de-endpoints-rest/` | Taller guiado | Diseño de endpoints aplicado a una entidad genérica |
| 4 | `3-proyecto/` | Entregable real — Sprint 3 | Endpoints CRUD codificados sobre el proyecto real |

---

## 📌 Entregable de la Semana

Al final de la semana, el repositorio del proyecto real debe tener:

- [ ] Sprint Planning documentado en GitHub Projects (issues del CRUD movidos a `Sprint Actual`)
- [ ] Endpoints CRUD de las entidades core codificados, con DTOs de entrada/salida separados del modelo de dominio
- [ ] Códigos de estado HTTP correctos por caso (200/201/204/400/404, etc.)
- [ ] Paginación implementada en los endpoints de listado
- [ ] Al menos un PR de `feature/*` mergeado a `develop`, revisado por un compañero, con CI en verde
- [ ] API respondiendo dentro del contenedor Docker (puerto mapeado, config por `.env`)
- [ ] Sprint Review completado con el instructor

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s04-sprint-3-review.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Endpoint** | Ruta HTTP concreta que expone una operación de la API |
| **DTO (Data Transfer Object)** | Estructura de datos de entrada/salida de un endpoint, distinta del modelo de dominio |
| **Verbo HTTP** | `GET`, `POST`, `PUT`/`PATCH`, `DELETE` — la operación que expresa la petición |
| **Código de estado** | Número de 3 dígitos que indica el resultado de la petición (2xx éxito, 4xx error de cliente, 5xx error de servidor) |
| **Paginación** | Entregar resultados de un listado en páginas, no todos de una vez |
| **Idempotencia** | Ejecutar la misma operación varias veces produce el mismo resultado que ejecutarla una vez |

Glosario completo en `5-glosario/README.md`.

---

## ✅ Checklist de Verificación

- [ ] Cada endpoint del CRUD tiene un verbo HTTP y un código de estado correctos, no genéricos
- [ ] Ningún endpoint devuelve el modelo de dominio directo — pasa por un DTO de salida
- [ ] El listado principal implementa paginación, no devuelve toda la tabla
- [ ] El PR fue revisado por al menos un compañero antes de mergear (no autoaprobado)
- [ ] La API responde en el puerto mapeado del contenedor, no solo en local
- [ ] El Sprint Review quedó documentado con % de avance acumulado

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 03 — Sprint 2: Autenticación y Autorización](../week-03-sprint_2_autenticacion_y_autorizacion/README.md) | [Semana 05 — Sprint 4: Reglas de Negocio y Servicios →](../week-05-sprint_4_reglas_de_negocio_y_servicios/README.md) |

---

## 💡 Consejos para esta Semana

- **Diseña la ruta antes de escribir el handler.** Un endpoint mal nombrado o con el verbo
  equivocado se arrastra el resto del proyecto — es más barato corregirlo en el papel que en código ya mergeado.
- **No expongas el modelo de dominio tal cual.** Aunque hoy parezca redundante, el DTO de salida
  te salva cuando el modelo cambie y la API no deba romperse.
- **Pagina desde el primer listado**, no cuando la tabla ya tenga miles de filas.
- **El code review no es un trámite.** Un PR autoaprobado o revisado por encima no cumple el
  criterio RAP-3 — el revisor debe verificar contra `CODING_STANDARDS.md`, no solo que compile.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 4 de 9*
