# Selección de Herramientas de Desarrollo

## 🎯 Objetivos

- Seleccionar el stack de desarrollo del proyecto real **hoy**, no en una semana futura
- Justificar la elección con base en el informe de diseño, no en preferencia sin fundamento

## 📋 Contenido

### 1. No hay tiempo de esperar

A diferencia de otros programas de formación que dejan la decisión de stack para semanas
posteriores, aquí se decide en esta primera sesión. El diseño ya está aprobado — el stack se
elige para construir ESE diseño, no al revés.

### 2. Criterios de selección (Criterio RAP-2)

| Pregunta | Por qué importa |
|---|---|
| ¿Qué tipo de arquitectura pide el diseño? (API REST, monolito, microservicios) | Define backend |
| ¿Qué tan interactiva es la UI requerida? | Define frontend (SPA vs renderizado tradicional) |
| ¿Qué modelo de datos tiene el dominio? (relacional, documentos) | Define motor de base de datos |
| ¿Con qué stack tiene experiencia real el equipo? | Reduce riesgo de perder semanas aprendiendo herramienta en vez de codificando |

### 3. Stacks de referencia (no obligatorios)

- **Backend**: FastAPI (Python), Express/NestJS (Node), Spring Boot (Java), Go
- **Frontend**: React, Next.js, Vue
- **Base de datos**: PostgreSQL, MySQL, MongoDB — según si el dominio es relacional o de documentos

> `proyecto-be_fastapi-fe_react` se usa como referencia de buenas prácticas de organización de
> código — no como stack impuesto. Cualquier combinación es válida si está justificada.

### 4. Aplicación al proyecto real

<!-- 📝 Instrucción: decidir en equipo, documentar la decisión y por qué -->

```markdown
## Stack elegido
- Backend: ___
- Frontend: ___
- Base de datos: ___

## Justificación
(2-3 líneas: por qué este stack sirve para el diseño aprobado)
```

Esta decisión va en `CODING_STANDARDS.md` (sección 1) — ver `05-estandares-de-codificacion.md`.

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para comparativas de stacks.
