# 📊 Rúbrica de Evaluación — Semana 04

> **Semana 04**: Sprint 3 — API CRUD de Entidades Core
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-diseno-de-endpoints-rest/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s04-sprint-3-review.md` + CRUD codificado en el proyecto real |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Qué verbo HTTP y qué código de estado corresponden a crear un recurso?
2. ¿Qué diferencia hay entre `200 OK` y `204 No Content`?
3. ¿Por qué el modelo de dominio no debe exponerse tal cual en la API?
4. ¿Qué es un DTO de entrada y qué es un DTO de salida?
5. ¿Por qué se pagina un endpoint de listado?
6. ¿Qué significa que `GET`, `PUT` y `DELETE` sean idempotentes y `POST` no?
7. ¿Cómo se descompone un CRUD completo en tareas para el Sprint Planning?
8. ¿Qué debe verificar un code review además de que el código compile?
9. ¿Qué significa que la API "responda dentro del contenedor" y no solo en local?
10. ¿Por qué la configuración de la API va en variables de entorno y no hardcodeada?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 4 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-diseno-de-endpoints-rest/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Rutas y verbos HTTP** | Las 5 rutas del CRUD con verbo correcto, sin verbos en la URL | 4-5 rutas correctas | 3 rutas correctas | 2 o menos correctas |
| **Códigos de estado** | Éxito y error justificados en cada endpoint | Éxito correcto en todos, error parcial | Solo éxito correcto | Códigos genéricos o ausentes |
| **Separación de DTOs** | DTO de entrada y salida completos, campo interno nunca expuesto | DTOs completos, campo interno expuesto en uno | Solo un DTO definido | Sin separación de DTOs |
| **Paginación** | Firma del endpoint, forma de respuesta y `page_size` máximo definidos | Firma y respuesta definidas, sin máximo | Solo la firma del endpoint | Sin paginación |

**Fórmula:** Promedio ponderado de los 4 criterios (peso igual).

---

## 📦 Evidencia de Producto (30% · 100 puntos)

**Instrumento:** `entregable-s04-sprint-3-review.md` + CRUD codificado en el repositorio real

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el backlog para el plan del sprint | 30 | Sprint Planning documentado: tareas por endpoint, trazables al backlog priorizado, sin historias inventadas |
| **RAP-3** — Estándares de codificación aplicados, vía code review | 30 | PRs revisados por un compañero contra `CODING_STANDARDS.md`, no autoaprobados; DTOs separados del modelo |
| **RAP-4** — Disciplina de flujo `feature/* → develop` | 25 | Ramas `feature/*` por tarea, PRs con CI en verde, mergeados a `develop`, sin push directo |
| **Estado Docker de la semana** (no bloqueante) | 15 | API responde en el puerto mapeado del contenedor, configurada por `.env` |

**Total:** 100 puntos

**Nota sobre el estado Docker:** a diferencia de la semana 9, esta evidencia **no es un gate
bloqueante** — un equipo puede alcanzar hasta 85/100 sin ella si RAP-1, RAP-3 y RAP-4 están
completos. Sí es evidencia obligatoria de desempeño acumulado hacia el gate final.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días — la semana 5 ya empieza el Sprint 4)
2. **Desempeño:** corregir el taller según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar los endpoints o PRs faltantes del sprint (plazo: 3 días, sin retrasar el inicio del Sprint 4 del resto del equipo)

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 4.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 4 de 9*
