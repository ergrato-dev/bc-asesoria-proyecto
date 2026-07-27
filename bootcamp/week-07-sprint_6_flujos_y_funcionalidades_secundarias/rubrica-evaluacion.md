# 📊 Rúbrica de Evaluación — Semana 07

> **Semana 07**: Sprint 6 — Flujos y Funcionalidades Secundarias
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-priorizacion-de-backlog-restante/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s07-sprint-6-review.md` + código del Sprint 6 |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Por qué el backlog restante casi nunca cabe completo a 3 semanas del cierre?
2. ¿Qué criterios usa la matriz de impacto/esfuerzo para priorizar una historia?
3. ¿Qué diferencia hay entre vertical slice y horizontal slice?
4. ¿Por qué dejar una historia a medias es peor que no empezarla, en esta etapa del proyecto?
5. ¿Qué debe documentarse cuando una historia se recorta del sprint?
6. ¿Por qué `depends_on` sin condición no garantiza que un servicio esté listo?
7. ¿Qué verifica un healthcheck en Docker Compose?
8. ¿Qué significa `condition: service_healthy` en un `depends_on`?
9. ¿Qué evidencia RAP-3 en esta semana, más allá de la existencia del `CODING_STANDARDS.md`?
10. ¿Qué disciplina de flujo Git exige RAP-4 en cada PR de esta semana?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 7 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-priorizacion-de-backlog-restante/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Backlog restante revisado** | Todas las historias pendientes evaluadas, ninguna fuera del tablero | La mayoría evaluadas, alguna omitida | Solo las historias obvias revisadas | Sin revisión estructurada |
| **Matriz impacto/esfuerzo aplicada** | Aplicada a cada historia, con criterio explícito | Aplicada a la mayoría | Aplicada de forma superficial | No se aplicó |
| **Decisión de priorización documentada** | Sprint 6 definido en el Milestone, recortes con motivo en cada issue | Sprint 6 definido, recortes sin motivo explícito | Sprint 6 definido informalmente, fuera del tablero | Sin decisión clara de qué entra |
| **Verificación de vertical slice** | Cada historia del sprint confirmada como viable de punta a punta | La mayoría confirmadas | Verificación parcial | Sin verificación |
| **Participación del equipo** | Todo el equipo participó en la priorización | La mayoría participó | Participación mínima | Decisión de una sola persona |

**Fórmula:** Promedio ponderado de los 5 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s07-sprint-6-review.md` + código del Sprint 6 en el repositorio real

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el backlog restante para el plan del sprint | 30 | Priorización documentada, historias del Sprint 6 trazables al backlog real, recortes justificados |
| **RAP-3** — Estándares de codificación aplicados en el código entregado | 30 | Código del sprint cumple `CODING_STANDARDS.md`, evidenciado en comentarios reales de code review sobre el/los PR |
| **RAP-4** — Disciplina de flujo `feature/* → develop`, PR revisado | 25 | Rama(s) `feature/*` correctas, PR revisado por un compañero, CI en verde antes de mergear |
| **Estado Docker de la semana** (no bloqueante) | 15 | `depends_on` con condición y healthchecks en `docker-compose.yml`, `docker compose up` sin errores de orden de arranque |

**Total:** 100 puntos

**Condición adicional, no negociable:** sin al menos un PR de `feature/*` mergeado a `develop`
con revisión de un compañero y CI en verde, el Producto no puede superar 70/100, sin importar qué
tan completo esté el Sprint Review escrito — el flujo de Git y el code review son evidencia
directa de RAP-3 y RAP-4, no un documento aparte.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días — la semana 8 ya empieza el Sprint 7)
2. **Desempeño:** completar la priorización faltante del backlog según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar el código o el Sprint Review pendiente (plazo: 3 días, sin retrasar el inicio del Sprint 7 del resto del equipo)

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 7.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 7 de 9*
