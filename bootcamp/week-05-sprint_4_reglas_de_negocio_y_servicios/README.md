# 📚 Semana 05 — Sprint 4: Reglas de Negocio y Servicios

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Ejecutar el Sprint Planning del Sprint 4, identificando reglas de negocio implícitas en las historias de usuario del backlog
2. Diseñar una capa de servicios que separe la lógica de negocio de los endpoints/controladores
3. Distinguir validación de entrada (formato, tipos) de validación de dominio (reglas de negocio)
4. Modelar y lanzar excepciones de dominio explícitas para las reglas de negocio violadas
5. Aplicar el flujo `feature/* → develop` con PR revisado por un compañero sobre el código del sprint
6. Verificar que los servicios y reglas de negocio corren igual dentro y fuera del contenedor Docker
7. Cerrar el sprint con un Sprint Review documentado: avance acumulado, demo, PRs mergeados

---

## 📋 Requisitos Previos

- Sprint 3 cerrado: API CRUD de entidades core funcionando (`week-04`)
- Backend dockerizado y respondiendo dentro del contenedor (semana 4)
- Backlog en GitHub Projects con historias pendientes de reglas de negocio para este sprint

---

## 🗂️ Estructura de la Semana

```
week-05-sprint_4_reglas_de_negocio_y_servicios/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-capa-de-servicios-y-reglas-de-negocio.md
│   └── 02-sprint-planning-reglas-de-negocio-implicitas.md
├── 2-practicas/
│   └── 01-taller-extraccion-de-reglas-de-negocio/   ← Checklist guiado sobre la técnica
├── 3-proyecto/
│   ├── README.md
│   └── starter/                           ← Plantilla de Sprint Review para tu proyecto real
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas)

```
🅰️ Ambiente de Formación      ████████████░░░░░░░░   6h  (60%)
🅱️ Trabajo Autónomo            ████████░░░░░░░░░░░░   4h  (40%)
```

### 🅰️ Ambiente de Formación (6h — guiado)

- **Sprint Planning breve (30-45 min)**: repasar el backlog, mover historias del Sprint 4 a
  "Sprint Actual" y aplicar la técnica de `1-teoria/02` para detectar reglas de negocio
  implícitas antes de codificar.
- **Teoría del patrón técnico (~2h)**: `1-teoria/01` — capa de servicios, validación de entrada
  vs validación de dominio, excepciones de dominio.
- **Taller guiado (~2h)**: `2-practicas/01-taller-extraccion-de-reglas-de-negocio/` — practicar
  la técnica antes de aplicarla al proyecto real.
- **Code review guiado (~1h)**: el instructor revisa en vivo el primer PR de servicios del
  equipo, con foco en separación de capas (evidencia de RAP-3).

### 🅱️ Trabajo Autónomo (4h)

Codificación del sprint sobre el proyecto real del equipo: servicios, validaciones de dominio,
excepciones. Cierra con el **Sprint Review** (plantilla en `3-proyecto/starter/`).

---

## 📝 Contenidos

| # | Archivo | Tipo | Saber de proceso reforzado |
|---|---------|------|------------------------------|
| 1 | `1-teoria/01-capa-de-servicios-y-reglas-de-negocio.md` | Teoría | Saber 4 — estándares aplicados en el código |
| 2 | `1-teoria/02-sprint-planning-reglas-de-negocio-implicitas.md` | Teoría | Saber 1 — interpretar backlog en Sprint Planning |
| 3 | `2-practicas/01-taller-extraccion-de-reglas-de-negocio/` | Taller guiado | Saberes 1 y 4 aplicados |
| 4 | `3-proyecto/` | Entregable real — Sprint 4 Review | Saberes 1, 4 y 6 — cierre del sprint |

---

## 📌 Entregable de la Semana

**Al final de la semana**, el repositorio del proyecto real debe tener:

- [ ] Sprint Planning del Sprint 4 documentado (historias en "Sprint Actual", reglas de negocio implícitas identificadas antes de codificar)
- [ ] Capa de servicios codificada, separada de los endpoints/controladores
- [ ] Validaciones de dominio (reglas de negocio) diferenciadas de validaciones de entrada (formato/tipos)
- [ ] Excepciones de dominio explícitas para las reglas de negocio violadas
- [ ] Al menos un PR de `feature/*` mergeado a `develop`, revisado por un compañero, con CI en verde
- [ ] Servicios y reglas de negocio verificados corriendo igual dentro y fuera del contenedor Docker (tests contra el backend containerizado)
- [ ] Sprint Review documentado en `3-proyecto/starter/entregable-s05-sprint-4-review.md`

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s05-sprint-4-review.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Regla de negocio** | Restricción o comportamiento propio del dominio, independiente de cómo llega la petición |
| **Capa de servicios** | Código que orquesta reglas de negocio, entre el endpoint y la persistencia |
| **Validación de entrada** | Verificación de formato/tipo de un dato recibido, antes de tocar el dominio |
| **Validación de dominio** | Verificación de una regla de negocio, dentro del servicio |
| **Excepción de dominio** | Error explícito que representa una regla de negocio violada, no un error técnico |
| **Sprint Planning** | Ceremonia de inicio de sprint que mueve historias del backlog al sprint actual |

---

## ✅ Checklist de Verificación

- [ ] El Sprint Planning quedó documentado antes de que empezara la codificación, no reconstruido después
- [ ] Ningún endpoint del sprint contiene una regla de negocio directamente en el controlador
- [ ] Cada excepción de dominio tiene un nombre que describe la regla violada, no un mensaje genérico
- [ ] El PR del sprint fue revisado por al menos un compañero antes de mergear (evidencia de RAP-3)
- [ ] Los tests de reglas de negocio se corrieron contra el backend containerizado, no solo en local
- [ ] El Sprint Review quedó documentado con % de avance acumulado real, no estimado de memoria

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 04 — Sprint 3: API CRUD de Entidades Core](../week-04-sprint_3_api_crud_entidades_core/README.md) | [Semana 06 — Sprint 5: Integración Frontend-Backend →](../week-06-sprint_5_integracion_frontend_backend/README.md) |

---

## 💡 Consejos para esta Semana

- **No mezcles validación de entrada con reglas de negocio en el mismo bloque de código.** Son responsabilidades distintas y cambian a ritmos distintos — la primera cambia si cambia el contrato de la API, la segunda si cambia el negocio.
- **Una excepción de dominio no es un código de estado HTTP.** El mapeo a `400`/`404`/`409` va en la capa de presentación (el endpoint), nunca dentro del servicio.
- **Si una historia de usuario no menciona una regla pero el negocio real la necesita, pregúntale al Product Owner de tu equipo** antes de asumirla en silencio — ver `1-teoria/02`.
- **El code review de esta semana no es un trámite.** Es la evidencia concreta de RAP-3: estándares de codificación aplicados, no solo documentados.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 5 de 9*
