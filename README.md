<p align="center">
  <img src="assets/bootcamp-header.svg" alt="Bootcamp Asesoría Desarrollo — Codificación del Proyecto" width="800">
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License MIT"></a>
  <a href="#"><img src="https://img.shields.io/badge/semanas-9-yellow.svg" alt="9 Semanas"></a>
  <a href="#"><img src="https://img.shields.io/badge/horas-90-orange.svg" alt="90 Horas"></a>
  <a href="#"><img src="https://img.shields.io/badge/SENA-ADSO-1565C0?logo=graduation-cap&logoColor=white" alt="SENA ADSO"></a>
  <a href="CONTRIBUTING.md"><img src="https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat-square" alt="PRs Welcome"></a>
</p>

<p align="center">
  <a href="README_EN.md"><img src="https://img.shields.io/badge/🇺🇸_English-0969DA?style=for-the-badge&logoColor=white" alt="English Version"></a>
</p>

---

## 📋 Descripción

Bootcamp de **9 semanas (~1 trimestre)** para la actividad de formación **Asesoría Desarrollo —
Codificación del Proyecto**, dirigido a aprendices de **cadena de formación** (Técnico en
Programación → Tecnólogo ADSO).

Cubre el RAP *"Planear actividades de construcción del software de acuerdo con el diseño
establecido"*: parte del informe de diseño entregado en el trimestre anterior (anteproyecto,
arquitectura, casos de uso, historias de usuario) y lleva al aprendiz a **codificar su propio
proyecto real** con estándares profesionales, control de versiones y automatización básica desde
el primer día.

> 📐 Ver [`docs/plan-curricular.md`](docs/plan-curricular.md) para la trazabilidad completa de
> Competencia, Saberes de Conceptos, Saberes de Proceso y Criterios de Evaluación del RAP.

### 🎯 Objetivos

Al finalizar el bootcamp, los aprendices serán capaces de:

- ✅ Interpretar su informe de diseño para definir un plan de trabajo de construcción
- ✅ Seleccionar y configurar un entorno de desarrollo completo para su stack
- ✅ Definir y documentar estándares de codificación propios del stack elegido
- ✅ Seleccionar y configurar herramientas de versionamiento con flujo colaborativo
- ✅ Configurar integración continua básica (lint + test en cada Pull Request)
- ✅ Ejecutar 8 sprints reales sobre su propio proyecto con revisión semanal
- ✅ Containerizar el proyecto de forma gradual con Docker, sprint a sprint
- ✅ Llegar a la semana 9 con **mínimo 90% del código construido y corriendo en contenedores — sin alternativa**

### 💡 ¿Por qué este bootcamp?

> **No hay tiempo que perder.** El alistamiento (interpretar el diseño, definir stack, configurar
> entorno, estándares, Git y CI/CD) se resuelve en la primera mitad de la semana 1 — la segunda
> mitad ya es código real sobre el proyecto del aprendiz.

Los aprendices llegan a este trimestre con diseño ya aprobado (anteproyecto, arquitectura, casos
de uso, historias de usuario del trimestre anterior). La meta no es enseñar a programar desde
cero — es instalar la disciplina de ingeniería (estándares, versionamiento, sprints, CI) que
convierte ese diseño en software real, y dejar el proyecto en 90% de avance para que el siguiente
trimestre solo cierre codificación, documentación e implementación.

**No se impone un stack único.** Cada equipo trae su propio proyecto y elige su stack en la
semana 1 según lo que su diseño requiere. `proyecto-be_fastapi-fe_react` se usa como referencia
de mejores prácticas (nomenclatura, linters, estructura `be/`/`fe/`) — no como stack obligatorio.

---

## 🗓️ Estructura del Bootcamp

| Fase | Semana | Horas | Enfoque |
| :---: | :---: | :---: | --- |
| **Alistamiento acelerado** | 1 (1ª mitad) | 5h | Diseño, stack, entorno, estándares, Git, CI/CD |
| **Arranque de código** | 1 (2ª mitad) | 5h | Sprint 0 — primer commit, primera feature, primer PR verde |
| **Ejecución de sprints** | 2-9 | 80h | Sprints 1 a 8, uno por semana, con Sprint Review semanal |

**Total: 9 semanas** | **90 horas** de formación (10h/semana: 6h Ambiente de Formación + 4h Trabajo Autónomo)

> 🐳 **Contenerización gradual y obligatoria**: desde la semana 1 se instala Docker; cada sprint
> agrega al `docker-compose.yml` lo que ese sprint construyó. El entregable de la semana 9
> (90% de avance) **debe** levantarse completo con `docker compose up` — no hay entrega válida
> fuera de contenedores. Ver [`docs/docker-guia.md`](docs/docker-guia.md).

---

## 📚 Contenido por Semana

| Semana | Tema | Estado Docker esperado |
|:---:|---|---|
| [1](bootcamp/week-01-alistamiento_acelerado_y_arranque/README.md) | Alistamiento acelerado y arranque de código | Docker instalado, `Dockerfile` esqueleto |
| [2](bootcamp/week-02-sprint_1_dominio_y_persistencia/README.md) | Sprint 1 — Dominio y persistencia | Servicio `db` en `docker-compose.yml` |
| [3](bootcamp/week-03-sprint_2_autenticacion_y_autorizacion/README.md) | Sprint 2 — Autenticación y autorización | Backend dockerizado, conectado a `db` |
| [4](bootcamp/week-04-sprint_3_api_crud_entidades_core/README.md) | Sprint 3 — API CRUD de entidades core | API responde dentro del contenedor |
| [5](bootcamp/week-05-sprint_4_reglas_de_negocio_y_servicios/README.md) | Sprint 4 — Reglas de negocio y servicios | Paridad local/contenedor |
| [6](bootcamp/week-06-sprint_5_integracion_frontend_backend/README.md) | Sprint 5 — Integración frontend-backend | `docker compose up` levanta todo el stack |
| [7](bootcamp/week-07-sprint_6_flujos_y_funcionalidades_secundarias/README.md) | Sprint 6 — Flujos y funcionalidades secundarias | Healthchecks y orden de arranque |
| [8](bootcamp/week-08-sprint_7_pruebas_y_manejo_de_errores/README.md) | Sprint 7 — Pruebas y manejo de errores | Imágenes optimizadas, CI sobre contenedores |
| [9](bootcamp/week-09-sprint_8_cierre_y_avance_90/README.md) | Sprint 8 — Cierre y avance 90% | **Gate de entrega**: `docker compose up` end-to-end, sin alternativa |

Cada semana incluye:

```
bootcamp/
└── week-XX-tema_principal/
    ├── README.md                # Descripción y objetivos
    ├── rubrica-evaluacion.md    # Criterios de evaluación (trazados al RAP)
    ├── 0-assets/                # Imágenes y diagramas
    ├── 1-teoria/                # Material teórico y de proceso
    ├── 2-practicas/             # Checklists y talleres guiados
    ├── 3-proyecto/              # Entregable aplicado al proyecto real del equipo
    ├── 4-recursos/              # Recursos adicionales
    │   ├── ebooks-free/
    │   ├── videografia/
    │   └── webgrafia/
    └── 5-glosario/              # Términos clave
```

### 🔑 Componentes Clave

- 📖 **Teoría**: Conceptos y proceso, aplicables a cualquier stack
- 💻 **Prácticas**: Checklists de configuración y buenas prácticas
- 🚀 **Proyecto**: Entregable semanal sobre el proyecto real del equipo (backlog, sprint, PRs)
- 🎓 **Recursos**: Glosario y material complementario por semana

---

## 🛠️ Herramientas del Bootcamp

| Herramienta | Uso | Costo |
| --- | --- | :---: |
| Git + GitHub | Control de versiones, ramas, Pull Requests | Gratuito |
| GitHub Projects | Backlog, sprints y tablero kanban vinculado al repo | Gratuito |
| GitHub Actions | Integración continua (lint + test en cada PR) | Gratuito |
| **Docker + Docker Compose** | **Contenerización del proyecto — obligatorio, sin alternativa** | Gratuito |
| IDE (VS Code recomendado) | Desarrollo, extensiones de linter/formatter | Gratuito |
| Runtime del stack elegido (Node, Python, etc.) | Ejecución local del proyecto | Gratuito |
| Motor de base de datos elegido (PostgreSQL, MySQL, MongoDB, etc.) | Persistencia del proyecto | Gratuito |
| Jira / ClickUp | Alternativas a GitHub Projects, si el equipo ya las usa | Gratuito (tier free) |

---

## 🚀 Inicio Rápido

### Prerrequisitos

- **Git** para control de versiones
- **VS Code** (recomendado) con extensiones incluidas
- Cuenta de **GitHub** activa
- Informe de diseño del trimestre anterior (anteproyecto, arquitectura, casos de uso, historias de usuario)

### 1. Clonar el Repositorio

```bash
git clone https://github.com/ergrato-dev/bc-asesoria-proyecto.git
cd bc-asesoria-proyecto
```

### 2. Instalar Extensiones de VS Code

```bash
code .
# Las extensiones recomendadas aparecerán automáticamente
```

### 3. Empezar por la Semana 1

```bash
cd bootcamp/week-01-alistamiento_acelerado_y_arranque
```

### 4. Seguir las Instrucciones

Cada semana contiene un `README.md` con instrucciones detalladas.

---

## 📊 Metodología de Aprendizaje

### Estrategias Didácticas

- 🎯 **Aprendizaje Basado en Proyectos (ABP)**: el proyecto real de cada equipo es el hilo conductor, desde la semana 1
- 🌀 **Scrum**: backlog, sprints semanales, roles (Scrum Master, PO, Dev, QA), daily/review/retro
- 🧩 **Construcción incremental**: cada sprint suma código funcional verificable, no solo documentación
- 👥 **Sprint Review con instructor**: seguimiento semanal del avance real contra el backlog
- 🔀 **Trunk-based collaborative flow**: `feature/*` sobre `develop`, `develop` → `main` en checkpoints — ver [`docs/git-workflow.md`](docs/git-workflow.md)

### Distribución del Tiempo (10h/semana)

- **Ambiente de Formación (6h)**: teoría breve, checklists guiados, Sprint Review con instructor
- **Trabajo Autónomo (4h)**: codificación del proyecto real, entre sesiones de AF

### Evaluación

Cada semana incluye tres tipos de evidencias:

1. **Conocimiento 🧠** (30%): Cuestionarios y checklists de conceptos clave
2. **Desempeño 💪** (40%): Configuración y aplicación de buenas prácticas (Git, estándares, CI/CD, ceremonias Scrum)
3. **Producto 📦** (30%): Entregable de código aplicado al proyecto real del equipo, anclado a un criterio de evaluación del RAP

**Criterio de aprobación**: Mínimo 70% en cada tipo de evidencia. Ver [`docs/plan-curricular.md`](docs/plan-curricular.md) para la trazabilidad completa.

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Este es un proyecto educativo de código abierto.

### Cómo Contribuir

1. Lee la [Guía de Contribución](CONTRIBUTING.md)
2. Revisa el [Código de Conducta](CODE_OF_CONDUCT.md)
3. Fork del repositorio
4. Crea tu rama (`git checkout -b feature/nueva-funcionalidad`)
5. Commit con [Conventional Commits](https://www.conventionalcommits.org/) (`git commit -m 'feat: add new checklist'`)
6. Push a la rama (`git push origin feature/nueva-funcionalidad`)
7. Abre un Pull Request

### 📋 Áreas de Contribución

- ✨ Checklists y plantillas adicionales
- 📚 Mejoras en documentación y teoría
- 🐛 Corrección de errores
- 🎨 Recursos visuales (diagramas SVG)
- 🌐 Traducciones
- 📋 Plantillas y rúbricas

---

## 📞 Soporte

- 💬 **Discussions**: [GitHub Discussions](https://github.com/ergrato-dev/bc-asesoria-proyecto/discussions)
- 🐛 **Issues**: [GitHub Issues](https://github.com/ergrato-dev/bc-asesoria-proyecto/issues)

---

## ⚠️ Exención de Responsabilidad

Este repositorio es un recurso **educativo** creado con fines de aprendizaje. Al utilizarlo, aceptas los siguientes términos:

- **Solo fines educativos**: El contenido, los ejemplos y los proyectos están diseñados exclusivamente para la enseñanza y el aprendizaje. No constituyen asesoramiento profesional, legal ni comercial.
- **Sin garantías**: El material se proporciona **"tal cual"**, sin garantías de ningún tipo, expresas o implícitas.
- **Sin datos reales**: Ningún ejemplo o plantilla debe completarse con datos personales reales de aprendices, instructores o terceros — usar siempre datos sintéticos en pruebas y ejemplos.
- **Responsabilidad del aprendiz**: Cada equipo es responsable de su propio código, sus decisiones técnicas y el cumplimiento de los criterios de evaluación del RAP.

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---

## 🏆 Agradecimientos

- Comunidad SENA ADSO - Por los casos reales que inspiraron el contenido
- [Conventional Commits](https://www.conventionalcommits.org/) - Por el estándar de commits adoptado
- [Scrum Guide](https://scrumguides.org/) - Por el marco ágil que estructura la ejecución de sprints
- Todos los contribuidores

---

## 📚 Documentación Adicional

- [🤖 Instrucciones de Copilot](.github/copilot-instructions.md)
- [🧭 Instrucciones de Claude Code](CLAUDE.md)
- [🤝 Guía de Contribución](CONTRIBUTING.md)
- [📜 Código de Conducta](CODE_OF_CONDUCT.md)
- [🔒 Política de Seguridad](SECURITY.md)
- [📐 Plan Curricular y Trazabilidad RAP](docs/plan-curricular.md)
- [📋 Guía de GitHub Projects](docs/guia-github-projects.md)
- [📏 Plantilla de Estándar de Código](docs/estandar-codigo-template.md)
- [🔀 Flujo de Git](docs/git-workflow.md)
- [⚙️ Guía de CI/CD](docs/ci-cd-guia.md)
- [🐳 Guía de Contenerización (Docker)](docs/docker-guia.md)

---

<p align="center">
  <strong>🎓 Bootcamp Asesoría Desarrollo — Codificación del Proyecto</strong><br>
  <em>Del informe de diseño al 90% del código construido</em>
</p>

<p align="center">
  <a href="bootcamp/week-01-alistamiento_acelerado_y_arranque">Comenzar Semana 1</a> •
  <a href="docs">Ver Documentación</a> •
  <a href="https://github.com/ergrato-dev/bc-asesoria-proyecto/issues">Reportar Issue</a>
</p>

<p align="center">
  Hecho con ❤️ para la comunidad de aprendices SENA
</p>
