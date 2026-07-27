# Taller — Configuración Completa del Entorno

<!-- 📝 Instrucción: taller guiado por el instructor, en equipo, con el proyecto real a la vista.
     Sigue el orden exacto — cada paso depende del anterior. -->

## Objetivo

Salir de este taller con el repositorio del proyecto real completamente configurado: backlog,
entorno, estándares, Git, CI y esqueleto Docker. Es la aplicación práctica de
`1-teoria/03` a `1-teoria/08` en un solo flujo continuo.

## Duración estimada

120 minutos (dentro del bloque de Alistamiento de 5h).

## Pasos

### 1. Backlog (15 min)

- [ ] Crear el GitHub Project del repositorio del proyecto real
- [ ] Cargar mínimo 5 historias de usuario del informe de diseño como Issues
- [ ] Columnas: `Backlog`, `Sprint Actual`, `En Progreso`, `En Revisión (PR)`, `Hecho`

### 2. Entorno local (20 min)

- [ ] Cada integrante instala el runtime del stack elegido
- [ ] Cada integrante corre `<runtime> --version` y comparte el resultado en el chat del equipo
- [ ] Crear la estructura de carpetas `be/`/`fe/` en el repositorio

### 3. Estándar de código (25 min)

- [ ] Copiar [`docs/estandar-codigo-template.md`](../../../../docs/estandar-codigo-template.md) a `CODING_STANDARDS.md` en la raíz del proyecto real
- [ ] Completar las secciones `[ ]` según el stack elegido
- [ ] Instalar linter + formatter, correr una vez para confirmar que no fallan por falta de config

### 4. Git y flujo colaborativo (25 min)

- [ ] `git init` (si no existe) + `git checkout -b develop` + push
- [ ] Activar branch protection en `main` y `develop`
- [ ] Cada integrante crea su primera `feature/*` desde `develop`

### 5. CI (20 min)

- [ ] Crear `.github/workflows/ci.yml` con el job de lint + test (ver [`docs/ci-cd-guia.md`](../../../../docs/ci-cd-guia.md))
- [ ] Abrir un PR de prueba con un error de lint intencional — confirmar que CI lo bloquea
- [ ] Corregir el error, confirmar que CI pasa, cerrar el PR de prueba sin mergear

### 6. Docker esqueleto (15 min)

- [ ] Verificar `docker --version` y `docker compose version` en cada máquina
- [ ] Crear `Dockerfile` esqueleto en `be/` y `fe/` (ver [`docs/docker-guia.md`](../../../../docs/docker-guia.md))

## Cierre del taller

Al terminar, el repositorio del proyecto real cumple el checklist completo de la sección
"📌 Entregable de la Semana" del `README.md` de esta semana, salvo el Sprint 0 (eso es el
siguiente bloque, en `3-proyecto/`).
