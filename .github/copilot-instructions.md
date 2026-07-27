# 🤖 Instrucciones para GitHub Copilot

## 📋 Contexto del Bootcamp

Este repositorio contiene el material de la actividad de formación **Asesoría Desarrollo —
Codificación del Proyecto** (SENA ADSO, cadena de formación). Es contenido educativo en
Markdown, no una aplicación en producción.

### 📊 Datos del Bootcamp

| Campo | Valor |
|---|---|
| Duración | 9 semanas |
| Horas totales | 90h (10h/semana: 6h Ambiente de Formación + 4h Trabajo Autónomo) |
| Población | Cadena de formación (Técnico en Programación → Tecnólogo ADSO) |
| RAP | Planear actividades de construcción del software de acuerdo con el diseño establecido |
| Competencia | Asesoría Desarrollo - Codificación |
| Meta de avance | ≥90% del código del proyecto real construido al final de la semana 9 |

---

## 🎯 Objetivos de Aprendizaje

Al finalizar, el aprendiz:

1. Interpreta su informe de diseño (anteproyecto, arquitectura, casos de uso, historias de usuario) para definir un plan de trabajo
2. Selecciona y configura herramientas de desarrollo según las condiciones de su proyecto
3. Define estándares de codificación según las reglas de la plataforma seleccionada
4. Selecciona y configura herramientas de versionamiento para el control de cambios
5. Ejecuta sprints reales sobre su propio proyecto con Sprint Review semanal

---

## 📚 Estructura del Bootcamp

Single-track — solo cadena de formación (no hay versión "oferta abierta" en este repositorio).

| Fase | Semana | Enfoque |
| :---: | :---: | --- |
| Alistamiento acelerado | 1 (1ª mitad) | Interpretar diseño, definir stack, configurar entorno/estándares/Git/CI |
| Arranque de código | 1 (2ª mitad) | Sprint 0 — primer commit, primera feature, primer PR verde |
| Sprint 1 — Dominio y persistencia | 2 | Modelos de dominio, esquema de datos, migraciones |
| Sprint 2 — Autenticación y autorización | 3 | Login, roles, control de acceso |
| Sprint 3 — API CRUD de entidades core | 4 | Endpoints principales del backend |
| Sprint 4 — Reglas de negocio y servicios | 5 | Validaciones, capa de servicios |
| Sprint 5 — Integración frontend-backend | 6 | Consumo de API, pantallas principales |
| Sprint 6 — Flujos y funcionalidades secundarias | 7 | Casos de uso restantes del backlog |
| Sprint 7 — Pruebas y manejo de errores | 8 | Testing, hardening, UX de errores |
| Sprint 8 — Cierre y avance 90% | 9 | Code review final, deuda técnica, demo integrada, **gate Docker obligatorio** |

Docker se integra gradualmente cada sprint (ver `docs/docker-guia.md`) — no es opcional ni
sustituible por otra herramienta de contenerización. El entregable de la semana 9 no se acepta
si no levanta completo con `docker compose up`.

### Principio Pedagógico Transversal

**El proyecto real de cada equipo es el hilo conductor desde la semana 1.** No hay caso de
estudio ficticio compartido — a diferencia de otros bootcamps de este catálogo, aquí todo el
contenido de `3-proyecto/` se aplica directamente al proyecto de diseño ya aprobado del equipo.
El contenido genérico (`1-teoria/`, `2-practicas/`) describe **proceso**, no dominio de negocio,
para mantenerse aplicable a cualquier stack.

---

## 🗂️ Estructura de Carpetas

```
bc-asesoria-proyecto/
├── .github/                  # Config de GitHub (este archivo, workflows)
├── assets/                   # SVG del header del bootcamp
├── bootcamp/
│   └── week-XX-tema/         # Una carpeta por semana (ver estructura abajo)
├── docs/
│   ├── plan-curricular.md          # Trazabilidad RAP completa
│   ├── guia-github-projects.md     # Backlog, sprints, plantillas de ceremonias
│   ├── estandar-codigo-template.md # Plantilla de estándar de código por stack
│   ├── git-workflow.md             # feature/* → develop → main
│   ├── ci-cd-guia.md               # GitHub Actions básico
│   └── docker-guia.md              # Contenerización gradual, obligatoria, gate semana 9
├── README.md / README_EN.md
├── CONTRIBUTING.md / CODE_OF_CONDUCT.md / SECURITY.md / LICENSE
```

### 📁 Carpetas Raíz

- `bootcamp/`: contenido semanal, única fuente de verdad para instructores y aprendices
- `docs/`: guías transversales reutilizadas por varias semanas — no dupliques su contenido dentro de `bootcamp/`, enlázalas

---

## 🎓 Componentes de Cada Semana

```
week-XX-tema/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
├── 1-teoria/
├── 2-practicas/
├── 3-proyecto/
│   ├── README.md
│   ├── starter/
│   └── solution/       ← NUNCA se sube al repo (.gitignore)
├── 4-recursos/{ebooks-free,videografia,webgrafia}/
└── 5-glosario/
```

### 1. Teoría (`1-teoria/`)

Archivos numerados `01-*.md`, `02-*.md`, ≤150 líneas cada uno. Contenido de proceso, agnóstico de
stack. Cuando se necesite un ejemplo de código, márcalo explícitamente como **ilustrativo** y
usa un stack distinto al de la semana anterior para reforzar que no hay stack único.

### 2. Prácticas (`2-practicas/`)

Checklists guiados y talleres cortos (configuración de herramientas, ejercicios de estándares,
simulacros de ceremonia ágil). No usan el proyecto real — son ejercicios de la herramienta en sí.

### 3. Proyecto (`3-proyecto/`)

Entregable aplicado al proyecto real de cada equipo. Plantilla en `starter/`, siempre con
instrucción en comentario HTML (`<!-- 📝 Instrucción: ... -->`) y al menos un ejemplo parcial.

### 4. Recursos (`4-recursos/`)

Enlaces a documentación oficial (no tutoriales de un stack específico salvo que la semana lo
amerite), videografía y webgrafía en español cuando exista.

### 5. Glosario (`5-glosario/`)

Términos clave de la semana, formato tabla `Término | Definición breve`.

---

## 📝 Convenciones de Documentación

### Nomenclatura de Archivos

Kebab-case, sin tildes, sin espacios. Teoría `01-nombre-tema.md`, plantillas `plantilla-*.md`,
entregables `entregable-*.md`.

### Idioma

- Documentación, teoría, guías: **español**
- Nomenclatura técnica (código, ramas, commits, nombres de archivo de código): **inglés**
- No mezclar idiomas dentro de un mismo párrafo

---

## 🔀 Git y Versionamiento

Este bootcamp **no está** en `main` únicamente — a diferencia de otros repos del catálogo, aquí
se enseña y exige el flujo:

- `develop`: rama de integración del equipo
- `feature/<slug>`: una rama por historia de usuario o tarea, creada desde `develop`
- PR + revisión de al menos un compañero antes de merge a `develop`
- `main`: solo recibe merge de `develop` en checkpoints de sprint (fin de cada semana 2-9)
- Conventional Commits obligatorio, ver `docs/git-workflow.md`

Cuando generes ejemplos de comandos Git en el contenido, usa siempre este flujo — nunca
`git push origin main` directo ni commits sin tipo convencional.

---

## 📊 Evaluación

Modelo híbrido, igual en todas las semanas:

| Evidencia | % | Instrumento |
|---|---|---|
| 🧠 Conocimiento | 30% | Cuestionario de conceptos |
| 💪 Desempeño | 40% | Checklist/taller de la herramienta o práctica de la semana |
| 📦 Producto | 30% | Entregable sobre el proyecto real, anclado a un criterio de evaluación del RAP |

Nota mínima de aprobación por tipo: 70%. Ver `docs/plan-curricular.md` para qué criterio del RAP
ancla cada semana.

### Criterios de Aprobación

- Cada `rubrica-evaluacion.md` referencia explícitamente el/los criterio(s) de evaluación oficial(es) del RAP que aplica
- No inventes criterios nuevos — usa únicamente los 4 definidos en `docs/plan-curricular.md`

---

## 🚀 Metodología de Aprendizaje

- Aprendizaje Basado en Proyectos (ABP) sobre el proyecto real de cada equipo
- Scrum: backlog en GitHub Projects, sprints semanales, roles, ceremonias (daily/review/retro)
- Sprint Review semanal con instructor a partir de la semana 2
- Distribución de tiempo: 6h Ambiente de Formación (guiado) + 4h Trabajo Autónomo (codificación)

---

## 🤖 Instrucciones para Copilot

### Límites de Respuesta

- No generes datos reales de aprendices, instructores o proyectos institucionales — solo ejemplos sintéticos
- No propongas un stack tecnológico único como si fuera obligatorio — el contenido genérico es agnóstico de stack
- No inventes criterios de evaluación fuera de los 4 oficiales del RAP

### Generación de Contenido

- Sigue exactamente la estructura de carpetas de semana descrita arriba
- Todo README de semana incluye navegación `← Anterior / Siguiente →`
- Toda rúbrica nueva sigue el modelo híbrido 30/40/30 y referencia el criterio del RAP correspondiente
- Comandos de ejemplo de Git siguen el flujo `feature/* → develop → main`

---

## 📖 Formatos Estándar de Documentación

### README.md de Semana

```markdown
# 📚 Semana XX — [Tema]

## 🎯 Objetivos de Aprendizaje
## 📋 Requisitos Previos
## 🗂️ Estructura de la Semana
## 📝 Contenidos
## ⏱️ Distribución del Tiempo (10h)
## 📌 Entregable de la Semana
## 🎓 Conceptos Clave
## ✅ Checklist de Verificación
## 🔗 Navegación
```

### Archivos de Teoría

```markdown
# Título del Tema

## 🎯 Objetivos
## 📋 Contenido
### 1. Introducción
### 2. Conceptos Clave
### 3. Aplicación al proyecto real
### 4. Plantilla y cómo usarla

## 📚 Recursos Adicionales
```
