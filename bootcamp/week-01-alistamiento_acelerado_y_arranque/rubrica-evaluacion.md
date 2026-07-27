# 📊 Rúbrica de Evaluación — Semana 01

> **Semana 01**: Alistamiento Acelerado y Arranque de Código
> **Criterios RAP evaluados**: RAP-1, RAP-2, RAP-3, RAP-4 (los 4 — única semana que los introduce todos)

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-configuracion-entorno/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s01-plan-de-trabajo.md` + Sprint 0 |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Qué documentos componen el informe de diseño de este proyecto?
2. ¿Cuál es la diferencia entre backlog y sprint backlog?
3. ¿Por qué el stack se decide en la semana 1 y no se difiere a semanas posteriores?
4. ¿Qué debe cubrir un `CODING_STANDARDS.md`?
5. ¿Por qué no se trabaja directo sobre `main`?
6. ¿Qué es Conventional Commits y para qué sirve?
7. ¿Qué verifica un pipeline de CI mínimo?
8. ¿Por qué Docker se integra gradualmente y no todo en la semana 1?
9. ¿Qué diferencia hay entre el `Dockerfile` esqueleto de esta semana y uno funcional?
10. ¿Qué significa que el entregable de la semana 9 no tenga alternativa fuera de contenedores?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 1 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-configuracion-entorno/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Backlog en GitHub Projects** | 5+ historias reales, priorizadas y con dependencias claras | 5 historias, priorización parcial | 3-4 historias | Menos de 3 o inexistente |
| **Entorno local** | Todo el equipo verifica instalación, proyecto corre local | Mayoría del equipo verifica | Solo un integrante verifica | Sin verificación |
| **CODING_STANDARDS.md** | Completo, sin `[ ]` pendientes, linter probado con violación real | Completo, linter configurado sin prueba real | Parcial | Ausente o vacío |
| **Git + branch protection** | `develop` activo, protección en ambas ramas, feature branch creada | `develop` activo, protección parcial | Solo `develop` sin protección | Sin `develop` |
| **CI configurado y probado** | CI bloquea un error de lint real, prueba documentada | CI configurado, sin prueba de bloqueo | Workflow existe pero no corre | Ausente |
| **Docker esqueleto** | `Dockerfile` en `be/` y `fe/`, versiones verificadas por todo el equipo | `Dockerfile` en una capa, versión verificada por el equipo | Solo instalación verificada | Docker no instalado |

**Fórmula:** Promedio ponderado de los 6 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s01-plan-de-trabajo.md` + Sprint 0 en el repositorio real

**Ancla a los 4 criterios RAP** (única semana que evalúa los 4 en un solo entregable):

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el informe de diseño para el plan de trabajo | 25 | Backlog priorizado con dependencias correctas, trazable al informe de diseño real |
| **RAP-2** — Selecciona y configura herramientas de desarrollo | 25 | Stack justificado, entorno funcionando, verificado por todo el equipo |
| **RAP-3** — Define estándares de codificación | 25 | `CODING_STANDARDS.md` completo y aplicado (linter real, no solo documento) |
| **RAP-4** — Selecciona y configura herramientas de versionamiento | 25 | `develop` + `feature/*` operativos, Sprint 0 mergeado con CI en verde |

**Total:** 100 puntos

**Condición adicional, no negociable:** sin Sprint 0 mergeado a `develop` con CI en verde, el
Producto no puede superar 70/100 sin importar qué tan completo esté el plan de trabajo escrito —
el objetivo de esta semana es código real, no solo documentación.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días — la semana 2 ya empieza el Sprint 1)
2. **Desempeño:** corregir el taller según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar lo faltante del plan de trabajo o del Sprint 0 (plazo: 3 días, sin retrasar el inicio del Sprint 1 del resto del equipo)

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 1.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 1 de 9*
