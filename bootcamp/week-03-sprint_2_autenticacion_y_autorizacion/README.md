# 📚 Semana 03 — Sprint 2: Autenticación y Autorización

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Interpretar el backlog priorizado para planificar el Sprint 2 (RAP-1)
2. Distinguir autenticación de autorización y elegir un modelo (sesión vs token/JWT) para su proyecto
3. Implementar login con hashing seguro de contraseñas (bcrypt/argon2 o equivalente del stack)
4. Implementar control de acceso basado en roles (RBAC) sobre los endpoints del backlog
5. Manejar credenciales y secretos por variables de entorno, sin hardcodearlos (nunca en el código ni en `docker-compose.yml`)
6. Aplicar estándares de codificación del proyecto vía code review en cada PR (RAP-3)
7. Sostener la disciplina de flujo `feature/* → develop` con PR revisado y CI en verde (RAP-4)
8. Dockerizar el backend y conectarlo a la base de datos por red de compose

---

## 📋 Requisitos Previos

- Semana 2 (Sprint 1) completada: modelos de dominio y esquema de datos codificados, `docker compose up db` funcional
- Entorno de desarrollo, `CODING_STANDARDS.md`, Git y CI ya operativos desde la semana 1

---

## 🗂️ Estructura de la Semana

```
week-03-sprint_2_autenticacion_y_autorizacion/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-modelos-de-autenticacion.md
│   ├── 02-sprint-planning-aplicado.md
│   └── 03-seguridad-basica-de-credenciales.md
├── 2-practicas/
│   └── 01-taller-diseno-de-autenticacion/  ← Checklist guiado, diseño antes de código
├── 3-proyecto/
│   ├── README.md
│   └── starter/                            ← Plantilla de Sprint Review de este sprint
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas)

```
🅰️ Ambiente de Formación   ████████████░░░░░░░   6h  (60%)
🅱️ Trabajo Autónomo         ████████░░░░░░░░░░░   4h  (40%)
```

### 🅰️ Ambiente de Formación (6h — guiado)

- **Sprint Planning** (30-45 min): ver `1-teoria/02-sprint-planning-aplicado.md`
- **Teoría del patrón técnico** (~2h): `1-teoria/01-modelos-de-autenticacion.md` y
  `1-teoria/03-seguridad-basica-de-credenciales.md`
- **Taller de diseño** (~1h): `2-practicas/01-taller-diseno-de-autenticacion/`
- **Code review guiado** (resto del bloque): el instructor revisa en vivo los primeros PR de auth
  del sprint, con foco en estándares (RAP-3) y ausencia de secretos hardcodeados

### 🅱️ Trabajo Autónomo (4h)

Codificación del sprint sobre el proyecto real del equipo: login, hashing, roles, endpoints
protegidos, hasta cerrar el checklist de `3-proyecto/README.md`. Cierra con el **Sprint Review**
(plantilla de [`docs/guia-github-projects.md`](../../docs/guia-github-projects.md#sprint-review-con-instructor-fin-de-semana)),
completado en `3-proyecto/starter/entregable-s03-sprint-2-review.md`.

---

## 📝 Contenidos

| # | Archivo | Tipo |
|---|---------|------|
| 1 | `1-teoria/01-modelos-de-autenticacion.md` | Teoría |
| 2 | `1-teoria/02-sprint-planning-aplicado.md` | Teoría / Proceso |
| 3 | `1-teoria/03-seguridad-basica-de-credenciales.md` | Teoría |
| 4 | `2-practicas/01-taller-diseno-de-autenticacion/` | Taller guiado |
| 5 | `3-proyecto/` | Entregable real — Sprint 2 Review |

---

## 📌 Entregable de la Semana

**Al cierre del Sprint 2**, el repositorio del proyecto real debe tener:

- [ ] Login funcional, con hashing seguro de contraseñas (bcrypt/argon2 o equivalente)
- [ ] Control de acceso por rol (RBAC) en los endpoints protegidos del backlog de este sprint
- [ ] `.env.example` actualizado, sin ningún secreto real hardcodeado en el código o en Docker
- [ ] Backend dockerizado (`Dockerfile` funcional), `docker compose up db be` levanta backend + BD
- [ ] Al menos una `feature/*` por historia de auth, cada una con PR revisado y mergeado a `develop` con CI en verde
- [ ] Sprint Review completado

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s03-sprint-2-review.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Autenticación** | Verifica quién es el usuario |
| **Autorización** | Verifica qué puede hacer un usuario ya autenticado |
| **Sesión / Token (JWT)** | Los dos modelos de autenticación comparados en `1-teoria/01` |
| **Hash de contraseña** | Resultado no reversible de bcrypt/argon2, nunca texto plano |
| **RBAC** | Control de acceso basado en roles |
| **`.env` / `.env.example`** | Secretos por variable de entorno, nunca commiteados; plantilla pública sí |
| **Sprint Review** | Ceremonia de cierre de sprint con el instructor: demo + % de avance |

---

## ✅ Checklist de Verificación

- [ ] El backlog del Sprint 2 refleja historias reales de auth del proyecto, no inventadas
- [ ] El modelo de autenticación (sesión o JWT) está decidido y documentado, no ambiguo
- [ ] Ningún secreto (clave de sesión/JWT, credencial) aparece hardcodeado en el historial de Git
- [ ] Cada PR del sprint fue revisado por al menos un compañero antes de mergear
- [ ] `docker compose up db be` levanta backend + base de datos sin pasos manuales adicionales
- [ ] El Sprint Review quedó documentado con demo y % de avance acumulado

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Semana 02 — Sprint 1: Dominio y Persistencia](../week-02-sprint_1_dominio_y_persistencia/README.md) | [Semana 04 — Sprint 3: API CRUD de Entidades Core →](../week-04-sprint_3_api_crud_entidades_core/README.md) |

---

## 💡 Consejos para esta Semana

- **Diseña antes de codificar.** El taller de `2-practicas/` existe para evitar reescribir el
  modelo de auth a mitad de sprint por una decisión no discutida en equipo.
- **El mensaje de error de login no distingue casos.** "Usuario no existe" y "contraseña
  incorrecta" deben responder exactamente igual — de lo contrario, un atacante puede enumerar
  usuarios válidos.
- **No hardcodees nunca la clave de sesión/firma**, ni siquiera "temporalmente para probar" — ese
  código temporal es el que termina en el commit que se revisa en producción.
- **RBAC simple primero.** Si el backlog solo pide `admin` vs `usuario`, no construyas permisos
  granulares que nadie pidió todavía.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 3 de 9*
