# 📚 Semana 01 — Alistamiento Acelerado y Arranque de Código

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, el aprendiz será capaz de:

1. Interpretar su informe de diseño (anteproyecto, arquitectura, casos de uso, historias de usuario) para definir un plan de trabajo
2. Organizar un backlog y sprints en GitHub Projects, con roles y ceremonias ágiles definidas
3. Seleccionar el stack de desarrollo de su proyecto real, sin dilación
4. Configurar un entorno de desarrollo completo (IDE, runtime, base de datos) con estructura de carpetas API REST
5. Definir y documentar estándares de codificación propios de su stack
6. Configurar Git con el flujo `feature/* → develop → main` y Conventional Commits
7. Configurar integración continua básica (lint + test en cada PR)
8. Instalar Docker y dejar el esqueleto de contenerización listo para crecer sprint a sprint
9. Escribir el primer código real de su proyecto (Sprint 0)

---

## 📋 Requisitos Previos

- Informe de diseño aprobado del trimestre anterior (anteproyecto, arquitectura, casos de uso, historias de usuario)
- Cuenta de GitHub activa, Git instalado
- Equipo de proyecto conformado (roles: Scrum Master, PO, Dev, QA — pueden rotar)

---

## 🗂️ Estructura de la Semana

```
week-01-alistamiento_acelerado_y_arranque/
├── README.md                              ← Estás aquí
├── rubrica-evaluacion.md
├── 1-teoria/
│   ├── 01-interpretacion-informe-diseno.md
│   ├── 02-planificacion-agil-scrum-sprints.md
│   ├── 03-seleccion-herramientas-desarrollo.md
│   ├── 04-configuracion-entorno-desarrollo.md
│   ├── 05-estandares-de-codificacion.md
│   ├── 06-control-de-versiones-git.md
│   ├── 07-integracion-continua.md
│   └── 08-contenerizacion-gradual-docker.md
├── 2-practicas/
│   └── 01-taller-configuracion-entorno/   ← Checklist guiado, mano a mano
├── 3-proyecto/
│   ├── README.md
│   └── starter/                           ← Plantillas para tu proyecto real
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

---

## ⏱️ Distribución del Tiempo (10 horas — sin tiempo que perder)

Esta semana **no** se reparte en 5 días iguales de teoría. La mitad se codifica ya.

```
🅰️ Alistamiento (1ª mitad)   █████████░░░░░░░░░░   5h  (~50%)
🅱️ Arranque de código (2ª)   █████████░░░░░░░░░░   5h  (~50%)
```

### 🅰️ Bloque de Alistamiento (5h — Ambiente de Formación, guiado)

Las 8 actividades de `1-teoria/` + el taller de `2-practicas/` se resuelven en este bloque,
en el mismo orden de los archivos numerados. No es un bloque de lectura pasiva: cada tema
termina con una decisión tomada y algo configurado, no con apuntes.

### 🅱️ Bloque de Arranque de Código (5h — arranca en Ambiente de Formación, continúa en Trabajo Autónomo)

Con el repo configurado (backlog, entorno, estándares, Git, CI, Docker esqueleto), el equipo
escribe su **Sprint 0**: primer commit real de dominio, primera rama `feature/*`, primer PR
que pasa CI y se mergea a `develop`. Ver `3-proyecto/`.

---

## 📝 Contenidos

| # | Archivo | Tipo | Actividad RAP original |
|---|---------|------|------------------------|
| 1 | `1-teoria/01-interpretacion-informe-diseno.md` | Teoría | Actividad 1 |
| 2 | `1-teoria/02-planificacion-agil-scrum-sprints.md` | Teoría | Actividad 2 |
| 3 | `1-teoria/03-seleccion-herramientas-desarrollo.md` | Teoría | Actividad 3 |
| 4 | `1-teoria/04-configuracion-entorno-desarrollo.md` | Teoría | Actividad 4 |
| 5 | `1-teoria/05-estandares-de-codificacion.md` | Teoría | Actividad 5 |
| 6 | `1-teoria/06-control-de-versiones-git.md` | Teoría | Actividad 6 |
| 7 | `1-teoria/07-integracion-continua.md` | Teoría | Actividad 7 |
| 8 | `1-teoria/08-contenerizacion-gradual-docker.md` | Teoría | (transversal, obligatorio) |
| 9 | `2-practicas/01-taller-configuracion-entorno/` | Taller guiado | Actividades 3-7 aplicadas |
| 10 | `3-proyecto/` | Entregable real — Sprint 0 | Cierre de todas las actividades |

---

## 📌 Entregable de la Semana

**Al final del bloque de alistamiento**, el repositorio del proyecto real debe tener:

- [ ] Backlog inicial en GitHub Projects, derivado del informe de diseño
- [ ] Stack de desarrollo elegido y documentado (sin dilación — no se espera a otra semana)
- [ ] Entorno local funcionando: IDE, runtime, base de datos, estructura `be/`/`fe/` (o equivalente)
- [ ] `CODING_STANDARDS.md` completado a partir de [`docs/estandar-codigo-template.md`](../../docs/estandar-codigo-template.md)
- [ ] Repositorio con `main` + `develop`, branch protection activa
- [ ] `.github/workflows/ci.yml` corriendo lint + test en cada PR
- [ ] Docker instalado, `Dockerfile` esqueleto de backend y frontend (ver [`docs/docker-guia.md`](../../docs/docker-guia.md))

**Al final del bloque de arranque**, además:

- [ ] Al menos un PR de `feature/*` mergeado a `develop`, con CI en verde
- [ ] Primer commit de dominio real (no boilerplate vacío)

> 📁 Plantilla completa en `3-proyecto/starter/entregable-s01-plan-de-trabajo.md`.

---

## 🎓 Conceptos Clave

| Término | Definición breve |
|---------|-------------------|
| **Informe de diseño** | Conjunto de documentos aprobados el trimestre anterior: anteproyecto, arquitectura, casos de uso, historias de usuario |
| **Backlog** | Lista priorizada de historias de usuario pendientes |
| **Sprint** | Ciclo corto (aquí: 1 semana) de trabajo con un objetivo concreto |
| **Sprint 0** | Primer ciclo, dedicado a dejar el proyecto listo para codificar en serio |
| **Estándar de codificación** | Reglas de nombrado, formato e indentación acordadas para el proyecto |
| **`develop`** | Rama de integración continua del equipo |
| **`feature/*`** | Rama de una historia de usuario o tarea concreta |
| **CI (Integración Continua)** | Verificación automática (lint + test) en cada Pull Request |
| **Contenerización** | Empaquetar la aplicación en imágenes Docker reproducibles |

---

## ✅ Checklist de Verificación

- [ ] El backlog inicial refleja las historias de usuario del informe de diseño, no historias inventadas
- [ ] El stack está decidido y documentado — no queda "pendiente de definir"
- [ ] `CODING_STANDARDS.md` no tiene secciones sin completar (`[ ]` sin llenar)
- [ ] Un PR de prueba con un error de lint intencional fue bloqueado por CI (verificación real, no solo config)
- [ ] `docker --version` y `docker compose version` corren sin error en la máquina de cada integrante
- [ ] Existe al menos un commit con Conventional Commits en `develop`, mergeado desde una `feature/*`

---

## 🔗 Navegación

| ← Anterior | → Siguiente |
|-----------|-------------|
| [← Inicio del Bootcamp](../../README.md) | [Semana 02 — Sprint 1: Dominio y Persistencia →](../week-02-sprint_1_dominio_y_persistencia/README.md) |

---

## 💡 Consejos para esta Semana

- **No hay tiempo que perder.** El objetivo no es discutir el stack ideal en abstracto — es decidir y avanzar. Si el equipo lleva más de 30 minutos debatiendo una herramienta, elige la opción con la que ya tienen experiencia.
- **Docker desde el día 1, pero solo el esqueleto.** No dockerices lógica que aún no existe — el `Dockerfile` de esta semana es intencionalmente mínimo.
- **El primer commit real importa más que un README perfecto.** Prioriza tener algo de dominio codificado sobre pulir documentación en Sprint 0.
- **Habla con tu instructor** si tu informe de diseño tiene vacíos que bloquean decidir el stack o el modelo de datos inicial.

---

*Cadena de Formación · Asesoría Desarrollo — Codificación · Semana 1 de 9*
