# 📊 Rúbrica de Evaluación — Semana 02

> **Semana 02**: Sprint 1 — Dominio y Persistencia
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4 (RAP-2 no aplica — fue decisión única de la semana 1)

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-modelado-de-dominio/` + code review real del PR del sprint |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s02-sprint-1-review.md` + Sprint 1 en el repositorio real |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Qué diferencia hay entre entidad y value object?
2. ¿Qué es un agregado y qué es su raíz?
3. ¿Por qué se modela el dominio antes de crear tablas o colecciones?
4. ¿Qué información debe extraerse de cada historia de usuario para identificar entidades?
5. ¿Qué es una migración y por qué no se reemplaza con `CREATE TABLE` manual?
6. ¿Qué debe tener una migración bien escrita (tamaño, reversibilidad)?
7. ¿Qué garantiza (y qué no garantiza) el esquema de base de datos frente a las reglas de negocio?
8. ¿Qué significa que un volumen de Docker sea persistente?
9. ¿Qué diferencia hay entre `docker compose down` y `docker compose down -v`?
10. ¿Qué debe revisar un compañero en un code review antes de aprobar un PR?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 2 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-modelado-de-dominio/` + code review real del PR del sprint

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Modelado de dominio (taller)** | Entidades, value objects y relaciones correctamente distinguidos y justificados | Distinción correcta, justificación parcial | Confunde entidad y value object en algún caso | Sin distinción clara |
| **Esquema de datos** | Tipos, claves primarias y foráneas correctos, nombrado según `CODING_STANDARDS.md` | Correcto con alguna inconsistencia de nombrado | Esquema funcional pero con tipos genéricos | Esquema no refleja el modelo de dominio |
| **Migraciones** | Aplicables desde cero, reversibles, un cambio conceptual por migración | Aplicables desde cero, sin `downgrade` | Aplicables con pasos manuales adicionales | No reproducibles |
| **Servicio `db` en Docker** | Levanta con `docker compose up db`, volumen persistente verificado por todo el equipo | Levanta, volumen persistente sin verificar por todos | Levanta sin volumen persistente | No levanta |
| **Code review aplicado** | Al menos un PR revisado con comentarios sustantivos contra `CODING_STANDARDS.md`, cambios solicitados y aplicados | PR revisado y aprobado, sin comentarios sustantivos | PR aprobado sin evidencia de revisión real | Autoaprobado o sin review |
| **Disciplina de flujo Git** | `feature/*` desde `develop` actualizado, commits Conventional, PR referencia el issue | Flujo correcto, algún commit no convencional | `feature/*` correcta, sin referencia al issue | Commits directos a `develop` o `main` |

**Fórmula:** Promedio ponderado de los 6 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s02-sprint-1-review.md` + Sprint 1 en el repositorio real

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el backlog para el plan del sprint | 30 | Historias del Sprint 1 trazables al backlog priorizado, modelo de dominio coherente con las historias asignadas |
| **RAP-3** — Estándares de codificación aplicados vía review | 30 | Código del sprint conforme a `CODING_STANDARDS.md`, evidencia real de comentarios de review, no solo documento sin aplicar |
| **RAP-4** — Disciplina de flujo `feature/* → develop` | 25 | PR revisado por un compañero, CI en verde, mergeado sin saltarse el flujo |
| **Estado Docker de la semana** | 15 | Servicio `db` en `docker-compose.yml` con volumen persistente — **no bloqueante**, pero exigido como evidencia |

**Total:** 100 puntos

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días)
2. **Desempeño:** corregir el taller o el code review según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar lo faltante del modelo de dominio, esquema o Sprint Review (plazo: 3 días, sin retrasar el inicio del Sprint 2 del resto del equipo)

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 2.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 2 de 9*
