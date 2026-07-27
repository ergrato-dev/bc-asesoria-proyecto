# 📊 Rúbrica de Evaluación — Semana 05

> **Semana 05**: Sprint 4 — Reglas de Negocio y Servicios
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4 (RAP-2 no aplica esta semana — selección/configuración de herramientas es una decisión de una sola vez, tomada y evaluada en la semana 1)

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-extraccion-de-reglas-de-negocio/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s05-sprint-4-review.md` + código del Sprint 4 |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Cuál es la diferencia entre validación de entrada y validación de dominio?
2. ¿Por qué la capa de servicios no debe conocer el framework HTTP?
3. ¿Qué es una excepción de dominio y en qué se diferencia de un error técnico?
4. ¿Quién decide el código de estado HTTP: el servicio o el endpoint? ¿Por qué?
5. ¿Qué es una regla de negocio implícita y cómo se detecta antes de codificar?
6. ¿Por qué el Sprint Planning de este sprint incluye buscar reglas no escritas en la historia de usuario?
7. ¿Qué evidencia el code review de este sprint sobre el criterio RAP-3?
8. ¿Por qué "servicios y reglas de negocio corren igual dentro y fuera del contenedor" es la evidencia Docker de esta semana?
9. ¿Qué diferencia hay entre un DTO y el modelo de dominio?
10. ¿Por qué RAP-2 no se evalúa esta semana?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 5 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-extraccion-de-reglas-de-negocio/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Reglas implícitas identificadas** | 2+ reglas por cada historia de ejemplo, justificadas | 2 reglas por historia, justificación parcial | 1 regla por historia | Sin reglas identificadas |
| **Separación de capas en código existente** | Las tres capas marcadas correctamente en un endpoint real del Sprint 3 | Dos de las tres capas marcadas correctamente | Solo una capa identificada | Sin marcar |
| **Diseño de servicio (firma)** | Firma completa, con excepción de dominio asociada | Firma completa, sin excepción asociada | Firma incompleta | Ausente |
| **Excepciones de dominio** | 2+ nombradas, con mapeo a código HTTP justificado | 2 nombradas, sin mapeo justificado | 1 nombrada | Ninguna |
| **Aplicación al proyecto real** | Técnica aplicada a todas las historias del Sprint 4 real, documentada en los issues | Aplicada a la mayoría de las historias | Aplicada parcialmente | No aplicada |

**Fórmula:** Promedio ponderado de los 5 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s05-sprint-4-review.md` + código del Sprint 4 en el repositorio real

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el backlog para el plan del sprint | 30 | Sprint Planning documentado, reglas de negocio implícitas identificadas antes de codificar, trazables a las historias reales |
| **RAP-3** — Estándares de codificación aplicados, vía code review | 30 | Capa de servicios separada de los endpoints, validaciones de dominio distinguidas de las de entrada, excepciones de dominio nombradas — verificado en el PR revisado |
| **RAP-4** — Disciplina de flujo `feature/* → develop`, PR revisado | 25 | Al menos un PR de `feature/*` mergeado a `develop`, revisado por un compañero, CI en verde |
| **Estado Docker de la semana** (no bloqueante) | 15 | Tests de reglas de negocio pasan contra el backend containerizado — evidencia de paridad local/contenedor |

**Total:** 100 puntos

**Nota sobre el estado Docker:** a diferencia del gate de la semana 9, este criterio **no bloquea**
el Producto — si los tests no corren aún contra el contenedor pero sí en local, el equipo pierde
los 15 puntos de ese criterio, no el entregable completo. Es evidencia de progreso, no condición
de entrega.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días — la semana 6 ya empieza el Sprint 5)
2. **Desempeño:** corregir el taller según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar lo faltante del Sprint Review o del código del sprint (plazo: 3 días, sin retrasar el inicio del Sprint 5 del resto del equipo)

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 5.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 5 de 9*
