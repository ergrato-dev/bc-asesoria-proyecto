# 📚 Semana 09 — Sprint 8: Cierre y Avance 90%

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Ejecutar un code review final sobre todo el repositorio del proyecto real, no solo sobre el último sprint
2. Identificar y documentar la deuda técnica pendiente, sin necesidad de resolverla toda en esta semana
3. Medir y verificar el avance real del proyecto contra el backlog completo, con una meta de **≥90%**
4. Superar el **gate de entrega Docker**: `docker compose up` sobre un clon limpio del repositorio, sin pasos manuales adicionales — condición bloqueante, sin alternativa
5. Preparar y presentar una demo integrada end-to-end del proyecto
6. Dejar el hand-off documentado para que el siguiente trimestre continúe la codificación restante, la documentación y la implementación final

---

## 📋 Requisitos Previos

- Sprints 1 a 7 completados (semanas 2-8), con `develop` estable y checkpoints en `main`
- `docker-compose.yml` con backend, frontend y base de datos definidos (semana 6 en adelante) y healthchecks/orden de arranque estables (semana 7)
- Backlog en GitHub Projects actualizado con el estado real de cada historia

---

## 🗂️ Estructura de la Semana

```
week-09-sprint_8_cierre_y_avance_90/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-code-review-final-y-deuda-tecnica.md
│   ├── 02-gate-docker-de-entrega.md
│   └── 03-demo-integrada-end-to-end.md
├── 2-practicas/
│   └── 01-taller-gate-docker-y-cierre/    ← Checklist guiado, ejecución real del gate
├── 3-proyecto/
│   ├── README.md
│   └── starter/                           ← Entregable de cierre del trimestre
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas — última semana del trimestre)

Esta semana **no** es un sprint de funcionalidad nueva. Es cierre: revisar, verificar y dejar
documentado lo que sigue.

```
🅰️ Ambiente de Formación (guiado)    █████████████░░░░░░  6h  (~60%)
🅱️ Trabajo Autónomo                  ████████░░░░░░░░░░░  4h  (~40%)
```

### 🅰️ Bloque de Ambiente de Formación (6h)

Code review cruzado entre equipos (o con el instructor) sobre todo el repositorio, seguido de la
verificación formal del gate Docker. Ver `1-teoria/` y `2-practicas/01-taller-gate-docker-y-cierre/`.

### 🅱️ Bloque de Trabajo Autónomo (4h)

Resolver los hallazgos del code review que sean bloqueantes para el gate o para el 90% de avance,
y terminar el gate Docker si algo quedó pendiente. La deuda técnica no bloqueante se documenta, no
se resuelve a la fuerza en estas 4 horas. Ver `3-proyecto/`.

---

## 📝 Contenidos

| # | Archivo | Tipo | Actividad |
|---|---------|------|-----------|
| 1 | `1-teoria/01-code-review-final-y-deuda-tecnica.md` | Teoría | Barrido completo del repositorio |
| 2 | `1-teoria/02-gate-docker-de-entrega.md` | Teoría | Gate de entrega, sin alternativa |
| 3 | `1-teoria/03-demo-integrada-end-to-end.md` | Teoría | Preparación de la demo final |
| 4 | `2-practicas/01-taller-gate-docker-y-cierre/` | Taller guiado | Ejecución paso a paso del gate |
| 5 | `3-proyecto/` | Entregable real — Cierre del trimestre | Producto final ancla RAP-1, RAP-3, RAP-4 |

---

## 📌 Entregable de la Semana

**El Producto de esta semana no aprueba sin el gate Docker superado**, sin importar cuánto código
haya construido el equipo. Checklist completo (copiado de
[`docs/docker-guia.md`](../../docs/docker-guia.md#checklist-de-verificación--semana-9-gate-de-entrega)):

- [ ] `git clone` limpio + `cp .env.example .env` + `docker compose up` levanta el proyecto completo
- [ ] Backend, frontend y base de datos corren cada uno en su propio contenedor
- [ ] No hay ningún proceso corriendo fuera de Docker para que el proyecto funcione
- [ ] El Sprint Review final se demuestra sobre la versión containerizada, no sobre el entorno local del aprendiz

Además del gate, el entregable de cierre debe incluir:

- [ ] **≥90% de avance del proyecto**, medido contra el backlog completo (no solo el último sprint)
- [ ] Code review final documentado, cubriendo todo el repositorio
- [ ] Lista de deuda técnica pendiente, documentada para el siguiente trimestre (no necesariamente resuelta)
- [ ] Demo integrada end-to-end preparada y ejecutada sobre la versión containerizada
- [ ] Hand-off documentado: qué queda por codificar, documentar o implementar en el siguiente trimestre

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s09-cierre-final.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Gate de entrega** | Condición bloqueante que el Producto debe superar sin excepción — aquí, `docker compose up` end-to-end |
| **Deuda técnica** | Trabajo pendiente o soluciones subóptimas, documentadas para resolver más adelante, no ahora |
| **Clon limpio** | Copia recién clonada del repositorio, sin configuración manual previa ni artefactos locales |
| **Demo integrada** | Demostración en vivo del flujo completo de la aplicación, de punta a punta |
| **Hand-off** | Documento que transfiere el estado del proyecto al siguiente equipo o trimestre |
| **Avance del 90%** | Meta de cierre del trimestre: proporción del backlog completo con código funcional construido |

---

## ✅ Checklist de Verificación

- [ ] El code review final cubrió todo el repositorio, no solo el Sprint 7
- [ ] El avance medido contra el backlog completo es ≥90% (o el equipo documenta por qué no, con plan concreto)
- [ ] `docker compose up`, en un clon limpio del repositorio + `.env` copiado de `.env.example`, levanta backend + frontend + BD sin ningún paso manual adicional
- [ ] La demo integrada se ejecutó sobre la versión containerizada, no sobre el entorno local
- [ ] La deuda técnica pendiente quedó documentada, con impacto y prioridad, para el siguiente trimestre

---

## 🔗 Navegación

| ← Anterior | → Fin del bootcamp |
|-----------|-------------|
| [← Semana 08 — Sprint 7: Pruebas y Manejo de Errores](../week-08-sprint_7_pruebas_y_manejo_de_errores/README.md) | Vuelve al [Inicio](../../README.md) — el siguiente trimestre continúa desde aquí |

---

## 💡 Consejos para esta Semana

- **El gate Docker no es negociable.** No hay "casi funciona" ni "en mi máquina sí corre" — si `docker compose up` no levanta el proyecto completo en un clon limpio, el Producto queda topado sin importar el resto.
- **Documentar deuda técnica no es fallar.** Un equipo que llega al cierre con una lista honesta de pendientes está mejor evaluado que uno que oculta atajos tomados bajo presión.
- **La demo se ensaya antes del Sprint Review.** No la improvises en vivo frente al instructor — corre el flujo completo sobre contenedores al menos una vez antes.
- **Si el gate falla, ese es el problema más urgente de las 4 horas de Trabajo Autónomo**, por encima de cualquier funcionalidad nueva.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 9 de 9 — Cierre*
