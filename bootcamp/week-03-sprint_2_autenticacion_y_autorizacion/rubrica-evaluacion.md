# 📊 Rúbrica de Evaluación — Semana 03

> **Semana 03**: Sprint 2 — Autenticación y Autorización
> **Criterios RAP evaluados**: RAP-1, RAP-3, RAP-4 (RAP-2 no aplica — es exclusivo de la semana 1)

---

## Distribución de la Evaluación

| Tipo de Evidencia | Porcentaje | Instrumento |
|-------------------|-----------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos clave |
| 💪 Desempeño | 40% | Taller `2-practicas/01-taller-diseno-de-autenticacion/` |
| 📦 Producto | 30% | Entregable `3-proyecto/starter/entregable-s03-sprint-2-review.md` + código del Sprint 2 |

**Nota mínima de aprobación por tipo: 70%**

---

## 🧠 Evidencia de Conocimiento (30%)

**Instrumento:** Cuestionario de 10 preguntas

1. ¿Cuál es la diferencia entre autenticación y autorización?
2. ¿Qué ventaja tiene un token (JWT) sobre una sesión de servidor al escalar horizontalmente?
3. ¿Por qué no basta con SHA-256 para guardar una contraseña?
4. ¿Qué papel cumple el *salt* en el hashing de contraseñas?
5. ¿Qué es RBAC y cuándo se justifica un modelo de permisos más granular?
6. ¿Por qué el login debe responder igual ante usuario inexistente y contraseña incorrecta?
7. ¿Qué diferencia hay entre un error 401 y uno 403?
8. ¿Por qué un secreto nunca va en `docker-compose.yml` ni en el `Dockerfile`?
9. ¿Para qué existe `.env.example` si `.env` nunca se commitea?
10. ¿Qué evidencia Docker de esta semana, y por qué todavía no es un gate bloqueante?

### Criterios de Calificación

| Puntaje | Desempeño |
|---------|-----------|
| 9-10 correctas | Excelente |
| 7-8 correctas | Bueno |
| 5-6 correctas | Aceptable — requiere repaso antes del Sprint 3 |
| < 5 correctas | Insuficiente — revisar toda la teoría de la semana |

---

## 💪 Evidencia de Desempeño (40%)

**Instrumento:** `2-practicas/01-taller-diseno-de-autenticacion/`

| Criterio | Excelente (100%) | Bueno (80%) | Aceptable (60%) | Insuficiente (<60%) |
|----------|-----------------|-------------|-----------------|---------------------|
| **Modelo elegido** | Sesión o JWT decidido, con razón justificada y coherente con el stack | Decidido, razón superficial | Decidido sin razón documentada | Sin decidir |
| **Diseño de hashing** | Librería y parámetros definidos, flujo de registro completo | Librería definida, flujo parcial | Solo librería mencionada | Ausente |
| **Tabla de roles** | Todos los endpoints del sprint mapeados a rol(es) | Mayoría de endpoints mapeados | Menos de la mitad mapeados | Sin tabla |
| **Manejo de errores** | 401/403 correctamente distinguidos, mensaje de login uniforme confirmado | Distinción correcta, mensaje sin verificar | Distinción parcial | Sin definir |
| **Checklist de secretos** | `.env.example` actualizado y `.gitignore` verificado por todo el equipo | Verificado por la mayoría | Verificado por un integrante | Sin verificar |

**Fórmula:** Promedio ponderado de los 5 criterios (peso igual).

---

## 📦 Evidencia de Producto (30%)

**Instrumento:** `entregable-s03-sprint-2-review.md` + código del Sprint 2 en el repositorio real

| Criterio | Puntaje Máx. | Qué se evalúa |
|----------|:---:|---|
| **RAP-1** — Interpreta el backlog para el plan del Sprint 2 | 30 | Historias de auth priorizadas correctamente, trazables al backlog real, Sprint Planning documentado |
| **RAP-3** — Estándares de codificación aplicados, vía code review | 30 | `CODING_STANDARDS.md` respetado en el código entregado, cada PR revisado por un compañero, sin secretos hardcodeados |
| **RAP-4** — Disciplina de flujo Git | 25 | `feature/*` por historia, PR contra `develop`, CI en verde, sin push directo a `develop`/`main` |
| **Estado Docker de la semana** (no bloqueante) | 15 | `docker compose up db be` levanta backend + BD; penaliza pero no anula el resto si falla |

**Total:** 100 puntos

**Nota:** a diferencia de la semana 9, el estado Docker de esta semana **no** es un gate — un
fallo aquí resta puntos en ese criterio, pero no limita el puntaje máximo de RAP-1/3/4.

---

## 📈 Nota Final de la Semana

```
Nota = (Conocimiento × 0.30) + (Desempeño × 0.40) + (Producto × 0.30)
```

---

## 🔄 Criterios de Recuperación

Si alguna evidencia está entre 60% y 69%:

1. **Conocimiento:** repetir cuestionario con preguntas distintas (plazo: 2 días — la semana 4 ya empieza el Sprint 3)
2. **Desempeño:** corregir el taller de diseño según observaciones del instructor (plazo: 2 días)
3. **Producto:** completar lo faltante del código o del Sprint Review (plazo: 3 días, sin retrasar el inicio del Sprint 3 del resto del equipo)

Si la nota es inferior al 60%, reunión obligatoria con el instructor antes de iniciar el Sprint 3.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 3 de 9*
