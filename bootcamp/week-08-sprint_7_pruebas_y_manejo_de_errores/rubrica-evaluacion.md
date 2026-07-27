# 📊 Rúbrica de Evaluación — Semana 08

> **Semana 08**: Sprint 7 — Pruebas y Manejo de Errores
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-cobertura-de-pruebas-criticas/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s08-sprint-7-review.md` + Sprint 7 en el repo real |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Cuál es la diferencia entre una prueba unitaria y una prueba de integración?
2. Con tiempo limitado, ¿qué se prioriza primero al escribir pruebas: caso feliz o caso límite? ¿Por qué ambos importan?
3. ¿Qué hace que un flujo se considere "crítico" dentro de un proyecto?
4. ¿Por qué un manejo de errores inconsistente en la API es un problema de experiencia de usuario, no solo técnico?
5. ¿Qué código HTTP corresponde a un recurso inexistente? ¿Y a una petición sin autenticación?
6. ¿Qué es un build multi-stage y qué problema resuelve frente a un `Dockerfile` de una sola etapa?
7. ¿Para qué sirve `.dockerignore` y qué riesgo evita si no existe?
8. ¿Por qué el CI de esta semana debe correr pruebas contra la imagen Docker real y no solo en el runner desnudo?
9. ¿Qué evidencia el code review guiado de esta semana respecto a RAP-3?
10. ¿Por qué esta semana es la última antes del gate de entrega de la semana 9?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 8 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-cobertura-de-pruebas-criticas/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Identificación de flujos críticos** | 5 flujos identificados, justificados y priorizados correctamente | 5 flujos identificados, justificación parcial | 3-4 flujos identificados | Menos de 3 o inexistente |
| **Cobertura de pruebas** | Los 5 flujos tienen prueba automatizada corriendo en CI | 4 de 5 flujos cubiertos | 2-3 de 5 flujos cubiertos | 0-1 flujos cubiertos |
| **Casos límite** | Al menos un caso límite probado en los flujos sensibles (auth, dinero, permisos) | Casos límite parciales | Solo casos felices probados | Sin casos límite |
| **Manejo de errores** | Formato de respuesta consistente en todos los endpoints revisados | Consistente en la mayoría | Consistente en algunos | Sin estandarizar |

**Fórmula:** Promedio ponderado de los 4 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s08-sprint-7-review.md` + Sprint 7 en el repositorio real

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el backlog para el plan del Sprint 7 | 30 | Sprint Planning documentado, historias correctamente priorizadas y trazables al backlog real |
| **RAP-3** — Estándares de codificación aplicados, vía code review | 30 | Al menos un PR revisado en code review real contra `CODING_STANDARDS.md`, con hallazgos corregidos antes de mergear |
| **RAP-4** — Disciplina de flujo `feature/* → develop`, PR revisado | 25 | PRs de la semana siguen el flujo correcto, CI en verde antes de mergear, sin push directo a `develop`/`main` |
| **Estado Docker de la semana** | 15 | Imágenes optimizadas (multi-stage, `.dockerignore`) y CI corriendo contra ellas, según [`docs/docker-guia.md`](../../docs/docker-guia.md) |

**Total:** 100 puntos

**Condición adicional, no negociable:** sin al menos un flujo crítico con prueba automatizada
corriendo en CI, el Producto no puede superar 70/100 sin importar qué tan completo esté el
documento de Sprint Review — el objetivo de esta semana es hardening real del código, no solo
un reporte bien escrito.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días)
2. **Desempeño:** completar la cobertura de pruebas faltante según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar lo faltante del Sprint Review o del estado Docker (plazo: 3 días)

**Sin margen para arrastrar deuda a la semana 9.** Al ser la última semana antes del gate de
entrega, cualquier recuperación debe cerrarse dentro de esta misma semana o al inicio de la
semana 9, nunca acumularse hasta el cierre final.

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 8
(semana 9).

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 8 de 9*
