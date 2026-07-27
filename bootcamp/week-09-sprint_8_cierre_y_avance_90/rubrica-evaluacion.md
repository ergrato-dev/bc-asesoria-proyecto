# 📊 Rúbrica de Evaluación — Semana 09

> **Semana 09**: Sprint 8 — Cierre y Avance 90%
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4 (forma final/consolidada del trimestre — RAP-2 no aplica, es exclusivo de la semana 1)

---

## ⛔ Condición de Gate — Léelo Antes de Todo lo Demás

Esta semana es el **gate de entrega del trimestre, sin alternativa**: si `docker compose up`, en
un clon limpio del repositorio con `.env` copiado de `.env.example`, no levanta el proyecto
completo (backend + frontend + base de datos, cada uno en su propio contenedor, sin ningún paso
manual adicional), el bloque de Producto queda **topado en 40/100**, sin importar cuánto código
haya construido el equipo ni qué tan bien salgan el resto de criterios. Ver detalle en la sección
"📦 Evidencia de Producto".

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-gate-docker-y-cierre/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s09-cierre-final.md` + gate Docker verificado |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Por qué el gate Docker de la semana 9 no tiene alternativa, a diferencia de otras decisiones del proyecto?
2. ¿Qué diferencia hay entre correr el proyecto en local y correrlo en un clon limpio con `docker compose up`?
3. ¿Qué significa que un `docker-compose.yml` solo levante la base de datos, y por qué eso no cumple el gate?
4. ¿Qué información debe llevar cada ítem de deuda técnica documentada?
5. ¿Por qué no se resuelve toda la deuda técnica en la semana 9?
6. ¿Cómo se mide el % de avance del proyecto contra el backlog completo?
7. ¿Qué diferencia hay entre el code review de un PR normal y el code review final de esta semana?
8. ¿Por qué la demo integrada debe ejecutarse sobre contenedores y no sobre el entorno local?
9. ¿Qué se revisa con `docker compose logs` cuando un servicio no levanta?
10. ¿Qué debe quedar documentado en el hand-off al siguiente trimestre?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del hand-off |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-gate-docker-y-cierre/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Verificación del gate Docker** | Pasa en clon limpio, verificado por alguien fuera del equipo | Pasa en clon limpio, verificado solo por el equipo | Pasa solo tras corregir fallos durante el taller | No pasa |
| **Code review final cruzado** | Cubre todo el repositorio, hallazgos clasificados bloqueante/deuda | Cubre la mayor parte del repositorio | Cubre solo el último sprint | No se realizó |
| **Medición de avance** | % calculado contra backlog completo, con evidencia trazable a GitHub Projects | % calculado contra backlog completo, sin evidencia trazable | % estimado sin medición real | No se midió |
| **Resolución de hallazgos bloqueantes** | Todos los bloqueantes corregidos y verificados de nuevo contra el gate | Bloqueantes corregidos, sin re-verificación del gate | Bloqueantes parcialmente corregidos | Bloqueantes ignorados |
| **Ensayo de demo integrada** | Flujo completo ensayado sobre contenedores, cronometrado | Flujo ensayado sobre contenedores, sin cronometrar | Flujo ensayado sobre entorno local | No se ensayó |

**Fórmula:** Promedio ponderado de los 5 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s09-cierre-final.md` + gate Docker verificado en el repositorio real

**Ancla a RAP-1, RAP-3 y RAP-4 en su forma final del trimestre**, más la condición de gate y de
avance mínimo:

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el informe de diseño para el plan de trabajo (forma consolidada) | 25 | El backlog completo del trimestre refleja fielmente el informe de diseño original, con desviaciones justificadas |
| **RAP-3** — Define estándares de codificación (forma consolidada) | 25 | `CODING_STANDARDS.md` aplicado de forma consistente en todo el repositorio, no solo en los últimos sprints |
| **RAP-4** — Selecciona y configura herramientas de versionamiento (forma consolidada) | 20 | Historial de `develop`/`feature`/`main` limpio y disciplinado a lo largo de las 9 semanas, checkpoints de sprint presentes |
| **Gate Docker** | 30 | `docker compose up` en clon limpio levanta backend + frontend + BD sin pasos manuales — **BLOQUEANTE** |

**Total:** 100 puntos

**Condición bloqueante, no negociable:** si el gate Docker no pasa (`docker compose up` en un
clon limpio no levanta el proyecto completo, o requiere algún paso manual adicional), el Producto
**queda topado en 40/100**, sin importar el puntaje que hayan obtenido RAP-1, RAP-3 y RAP-4. No
hay puntaje parcial por "el gate casi pasa" — pasa o no pasa.

**Condición adicional del Producto:** el avance medido contra el backlog completo debe ser
**≥90%**. Si es menor, el Producto no puede superar 80/100 aunque el gate Docker sí haya pasado —
el equipo debe documentar en el entregable qué falta y por qué, y ese análisis se evalúa como
parte de RAP-1.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Última semana del trimestre — plazos cortos, sin margen para retrasar el cierre:

1. **Gate Docker no superado:** corrección obligatoria e inmediata, plazo máximo **1 día** — sin esto, no hay Sprint Review final válida
2. **Conocimiento o Desempeño entre 60% y 69%:** corrección según observaciones del instructor, plazo **1-2 días**
3. **Producto (avance < 90% o RAP incompletos):** completar lo faltante y documentarlo en el hand-off, plazo **2 días máximo**

Si la nota es inferior al 60%, o el gate Docker no se logra superar en el plazo de recuperación,
reunión obligatoria con el instructor y con coordinación académica antes del cierre formal del
trimestre.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 9 de 9 — Cierre*
