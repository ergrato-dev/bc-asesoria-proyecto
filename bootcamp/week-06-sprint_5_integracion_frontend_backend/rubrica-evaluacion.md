# 📊 Rúbrica de Evaluación — Semana 06

> **Semana 06**: Sprint 5 — Integración Frontend-Backend
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4 (RAP-2 no aplica — es exclusivo de la semana 1)

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-integracion-api-frontend/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s06-sprint-5-review.md` + código del Sprint 5 |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Qué son los estados de carga, error y éxito, y por qué deben manejarse por separado?
2. ¿Quién configura CORS, el backend o el frontend? ¿Por qué falla si no está configurado?
3. ¿Por qué la URL de la API no debe ir hardcodeada en el código del frontend?
4. ¿Qué es un `Dockerfile` multi-stage y qué problema resuelve frente a uno de una sola etapa?
5. ¿Qué diferencia hay entre la etapa de build y la etapa de runtime en un `Dockerfile` de frontend?
6. ¿Por qué esta semana el `docker compose up` levanta por primera vez los tres servicios juntos?
7. ¿Qué debe acordar el equipo en el Sprint Planning cuando backend y frontend se codifican en el mismo sprint?
8. ¿Qué verifica el code review de esta semana además de que el código funcione?
9. ¿Qué pasa si un PR de integración se mergea a `develop` sin que un compañero lo revise?
10. ¿Por qué no se acepta consumir datos mock si el endpoint real ya existe?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 6 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-integracion-api-frontend/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Consumo de API** | Los 3 estados (carga/error/éxito) implementados y probados desconectando el backend | Los 3 estados implementados, sin prueba real de desconexión | Solo el caso de éxito implementado | Sin consumo real de API o solo datos mock |
| **CORS** | Configurado correctamente, error provocado y entendido a propósito | Configurado correctamente, sin prueba de error | Configurado con `*` sin justificación | Sin configurar, bloqueando el consumo |
| **Variable de entorno** | URL de la API en variable de entorno, documentada en `.env.example`, verificada cambiando el valor | En variable de entorno, sin documentar | Parcialmente hardcodeada | URL hardcodeada en el código |
| **Docker multi-stage** | `fe/Dockerfile` con build y runtime separados, imagen final sin herramientas de desarrollo | Multi-stage presente, imagen final con algo de peso extra | Una sola etapa funcional | Sin `Dockerfile` de frontend o no construye |
| **Stack completo en Docker** | `docker compose up` levanta `db`+`be`+`fe` juntos en un clon limpio | Levanta los tres con algún paso manual adicional | Levanta solo `db`+`be` | Ningún servicio dockerizado corre junto |

**Fórmula:** Promedio ponderado de los 5 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s06-sprint-5-review.md` + código del Sprint 5 en el repositorio real

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el backlog para el plan del sprint | 30 | Historias de integración correctamente priorizadas y trazables al backlog real, Sprint Review preparado |
| **RAP-3** — Estándares de codificación aplicados | 30 | Código del sprint cumple `CODING_STANDARDS.md`, verificado en code review real de al menos un PR |
| **RAP-4** — Disciplina de flujo Git | 25 | `feature/* → develop`, PR revisado por un compañero, CI en verde, sin push directo a `develop`/`main` |
| **Estado Docker de la semana** | 15 | `docker compose up` levanta `db`+`be`+`fe` juntos en un clon limpio — **sin esto, este criterio no puede superar 5/15** |

**Total:** 100 puntos

**Condición adicional, no negociable:** el criterio de Docker no admite "casi funciona" — si
`docker compose up` no levanta los tres servicios juntos en un clon limpio, el puntaje de ese
criterio queda en 5/15 sin importar cuánto código de integración exista, porque el hito de esta
semana es exactamente ese: el stack completo arriba con un solo comando.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días — la semana 7 ya empieza el Sprint 6)
2. **Desempeño:** corregir el taller según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar lo faltante del Sprint Review o del código del sprint (plazo: 3 días, sin retrasar el inicio del Sprint 6 del resto del equipo)

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 6.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 6 de 9*
