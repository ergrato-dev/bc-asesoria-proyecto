# ⚙️ Guía de CI/CD Básico

Alcance de la semana 1: **integración continua** (lint + test automáticos en cada PR). No se
exige despliegue continuo — si el proyecto lo requiere, es una extensión opcional posterior.

---

## 1. Por qué CI desde la semana 1

Sin CI, un PR con código roto puede llegar a `develop` y bloquear a todo el equipo. El check
automático es el `Definition of Done` mínimo antes de que un humano revise el PR.

---

## 2. Workflow Mínimo (GitHub Actions)

Crear `.github/workflows/ci.yml` en el proyecto real del equipo (no en este repo de bootcamp):

```yaml
name: CI

on:
  pull_request:
    branches: [develop, main]

jobs:
  backend:
    if: hashFiles('be/**') != ''
    runs-on: ubuntu-24.04
    defaults:
      run:
        working-directory: be
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-python@v5
        with:
          python-version: "3.12"
      - run: pip install -r requirements.txt   # o: pip install uv && uv sync
      - run: ruff check .                       # lint
      - run: ruff format --check .              # formato
      - run: pytest                             # tests

  frontend:
    if: hashFiles('fe/**') != ''
    runs-on: ubuntu-24.04
    defaults:
      run:
        working-directory: fe
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: "24"
      - run: corepack enable && pnpm install --frozen-lockfile
      - run: pnpm lint
      - run: pnpm test
      - run: pnpm build
```

Adapta el nombre de comandos al linter/test runner real del stack elegido — la estructura
(checkout → instalar deps → lint → test → build) es la misma para cualquier stack.

---

## 3. Activar como Required Check

1. En GitHub: **Settings → Branches → Branch protection rules**
2. Regla para `develop` y `main`: **Require status checks to pass before merging**
3. Selecciona los jobs `backend` / `frontend` del workflow

Con esto, un PR con CI en rojo **no puede mergearse**, sin importar quién lo apruebe.

---

## 4. Tabla de Comandos por Stack (referencia)

| Stack | Lint | Format | Test |
|---|---|---|---|
| Python (ruff) | `ruff check .` | `ruff format --check .` | `pytest` |
| Python (flake8+black) | `flake8` | `black --check .` | `pytest` |
| TypeScript/React (eslint+prettier) | `pnpm lint` | `pnpm format:check` | `pnpm test` |
| Go | `go vet ./...` | `gofmt -l .` | `go test ./...` |
| Java (Spring Boot) | `mvn checkstyle:check` | — | `mvn test` |

---

## 5. Checklist de Verificación (Semana 1)

- [ ] `.github/workflows/ci.yml` existe en el repo del proyecto real
- [ ] El workflow corre lint + test en cada PR contra `develop` y `main`
- [ ] `develop` y `main` tienen branch protection con el CI como required check
- [ ] Se hizo una prueba real: un PR con un error de lint intencional fue bloqueado por CI
