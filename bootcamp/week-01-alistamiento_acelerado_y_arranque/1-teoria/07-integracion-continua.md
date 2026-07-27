# Integración Continua (CI)

## 🎯 Objetivos

- Configurar un workflow de GitHub Actions que corra lint + test en cada Pull Request
- Activar branch protection para que CI en rojo bloquee el merge

## 📋 Contenido

### 1. Por qué CI desde la semana 1

Sin CI, un PR con código roto puede llegar a `develop` y bloquear a todo el equipo. El check
automático es el mínimo "Definition of Done" antes de que un humano revise el PR.

### 2. Workflow mínimo

Backend y frontend, cada uno con su job condicional. Plantilla completa y explicada en
[`docs/ci-cd-guia.md`](../../../docs/ci-cd-guia.md).

```yaml
on:
  pull_request:
    branches: [develop, main]
jobs:
  backend:
    steps: [checkout, setup runtime, lint, format --check, test]
  frontend:
    steps: [checkout, setup runtime, lint, test, build]
```

### 3. Required status checks

Sin este paso, CI corre pero no bloquea nada. En GitHub: **Settings → Branches → Branch
protection rules**, marcar los jobs como required check para `develop` y `main`.

### 4. Aplicación al proyecto real

<!-- 📝 Instrucción: crear el workflow y probarlo con un error intencional -->

- [ ] `.github/workflows/ci.yml` creado, corre lint + test en cada PR
- [ ] `develop` y `main` exigen el check de CI antes de mergear
- [ ] Prueba real: un PR con un error de lint fue bloqueado por CI

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para documentación oficial de GitHub Actions.
