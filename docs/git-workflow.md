# 🔀 Flujo de Git — `feature → develop → main`

Flujo obligatorio para todos los proyectos reales del bootcamp, desde la semana 1.

---

## 1. Ramas

| Rama | Propósito | Quién commitea directo |
|---|---|---|
| `main` | Release / checkpoint estable de cada sprint | Nadie — solo merge desde `develop` |
| `develop` | Integración del equipo, siempre desplegable | Nadie — solo merge desde `feature/*` vía PR |
| `feature/<slug>` | Una historia de usuario o tarea concreta | El aprendiz asignado a esa historia |

```
main      ●─────────────●─────────────●        (checkpoint fin de Sprint 1, Sprint 2, ...)
           \             \             \
develop     ●──●──●──●──●──●──●──●──●──●        (integración continua del equipo)
                \        \
feature/login    ●──●──●●
feature/user-crud          ●──●──●
```

---

## 2. Configuración Inicial (Semana 1)

```bash
git init
git checkout -b develop
git remote add origin https://github.com/<org>/<proyecto>.git
git push -u origin develop

# Proteger main y develop en GitHub:
# Settings → Branches → Add rule
#   main:    Require PR before merging, require status checks (CI) to pass
#   develop: Require PR before merging, require status checks (CI) to pass
```

---

## 3. Trabajar una Historia de Usuario

```bash
# 1. Partir siempre de develop actualizado
git checkout develop
git pull origin develop

# 2. Crear la rama feature (nombre en inglés, kebab-case, referencia el issue)
git checkout -b feature/user-authentication

# 3. Commits pequeños y frecuentes con Conventional Commits
git add .
git commit -m "feat(auth): add password hashing with bcrypt"
git commit -m "feat(auth): add login endpoint"
git commit -m "test(auth): add login endpoint unit tests"

# 4. Push y Pull Request contra develop (nunca contra main)
git push -u origin feature/user-authentication
# Abrir PR en GitHub: feature/user-authentication → develop
```

**Antes de abrir el PR**, sincroniza con `develop` para evitar conflictos grandes:

```bash
git checkout develop
git pull origin develop
git checkout feature/user-authentication
git merge develop
# resolver conflictos si aparecen, luego push
```

---

## 4. Conventional Commits

```
<tipo>(<alcance>): <descripción en inglés, imperativo, minúsculas>
```

| Tipo | Uso |
|---|---|
| `feat` | Nueva funcionalidad |
| `fix` | Corrección de bug |
| `docs` | Documentación (README, comentarios) |
| `style` | Formato, sin cambio de lógica |
| `refactor` | Reestructuración sin cambiar comportamiento |
| `test` | Pruebas nuevas o corregidas |
| `chore` | Mantenimiento (deps, configs) |
| `ci` | Cambios en pipelines de CI/CD |
| `perf` | Mejora de rendimiento |

```bash
feat(user): add user registration endpoint
fix(auth): correct token expiration check
docs(readme): add environment setup instructions
refactor(order): extract pricing logic into service
chore(deps): bump fastapi to 0.115.0
ci(actions): add lint step to pull request workflow
```

---

## 5. Pull Request → `develop`

Checklist mínimo antes de pedir revisión:

- [ ] La rama está actualizada con `develop` (sin conflictos)
- [ ] CI en verde (lint + test) — ver [`ci-cd-guia.md`](ci-cd-guia.md)
- [ ] El PR referencia el issue/historia (`Closes #12`)
- [ ] Al menos un compañero revisó y aprobó
- [ ] Sin código de debug, sin TODOs sueltos, sin credenciales hardcodeadas

Al aprobar: **squash and merge** o **merge normal** (definido por el equipo, consistente durante todo el proyecto) — nunca `--force` sobre `develop`.

---

## 6. Checkpoint de Sprint → `main`

Al cierre de cada sprint (fin de semana, tras el Sprint Review), si `develop` está estable:

```bash
git checkout main
git pull origin main
git merge --no-ff develop -m "chore(release): checkpoint sprint N"
git tag -a sprint-N -m "Checkpoint Sprint N"
git push origin main --tags
```

`main` es siempre la última versión estable demostrada al instructor. Nunca se le hace push
directo, nunca se le mergea una `feature/*` sin pasar por `develop`.

---

## 7. Errores Comunes a Evitar

| ❌ No hacer | ✅ Hacer en su lugar |
|---|---|
| `git push origin main` directo | PR a `develop`, checkpoint a `main` solo por merge |
| Rama `feature/*` creada desde `main` | Crear siempre desde `develop` actualizado |
| Commits `"fix"`, `"cambios"`, `"wip"` | Conventional Commits descriptivos |
| Un solo commit gigante por historia | Commits pequeños y frecuentes |
| Mergear PR con CI en rojo | Corregir antes de mergear, nunca saltarse el check |
