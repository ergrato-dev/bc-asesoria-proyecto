# Taller — Diseño de Autenticación y Autorización

<!-- 📝 Instrucción: taller guiado por el instructor, en equipo. Se resuelve el diseño en papel/
     documento ANTES de codificar sobre el proyecto real — evita reescribir el modelo a medio
     sprint por una decisión no discutida. -->

## Objetivo

Fijar, por escrito, el modelo de autenticación y autorización del proyecto real antes de escribir
el primer commit del sprint. Es la aplicación práctica de `1-teoria/01-modelos-de-autenticacion.md`.

## Duración estimada

60 minutos (dentro del bloque de Ambiente de Formación, después de la teoría).

## Pasos

### 1. Elegir el modelo (15 min)

- [ ] Decidir sesión con cookie o token (JWT), usando la tabla comparativa de `1-teoria/01`
- [ ] Escribir en una frase la razón de la elección (no "porque sí" — referencia al stack o al
      tipo de cliente que consume la API)

### 2. Diseñar el hashing (10 min)

- [ ] Confirmar la librería de hashing disponible en el stack elegido (bcrypt/argon2 o equivalente)
- [ ] Definir el *cost factor*/parámetros por defecto
- [ ] Escribir el flujo de registro: dónde se hashea, qué se guarda, qué nunca se guarda

### 3. Diseñar la tabla de roles (20 min)

- [ ] Listar los roles reales del proyecto (mínimo 2: ej. `usuario`, `admin`)
- [ ] Por cada endpoint protegido del backlog de este sprint, anotar qué rol(es) puede acceder

```markdown
| Endpoint | Rol(es) permitido(s) |
|---|---|
| POST /auth/login | público |
| GET /users/me | cualquier autenticado |
| DELETE /users/:id | admin |
```

### 4. Diseñar el manejo de errores (10 min)

- [ ] Confirmar que credenciales inválidas responden igual sin importar si falló el usuario o la
      contraseña (ver `1-teoria/01`)
- [ ] Definir qué código HTTP corresponde a "no autenticado" (401) vs "autenticado sin permiso" (403)

### 5. Checklist de secretos (5 min)

- [ ] `.env.example` actualizado con la variable de la clave de sesión/firma (ver `1-teoria/03`)
- [ ] Confirmar que `.env` sigue en `.gitignore`

## Cierre del taller

El diseño resultante (modelo, hashing, tabla de roles, manejo de errores) es la base directa del
Sprint Planning de `1-teoria/02-sprint-planning-aplicado.md` y de la codificación en
`3-proyecto/`. No se codifica auth sobre el proyecto real sin haber pasado por este taller.
