# Seguridad Básica de Credenciales

## 🎯 Objetivos

- Nunca guardar un secreto (contraseña, clave de firma de token, credencial de BD) en el código fuente
- Usar variables de entorno y un `.env.example` como contrato del equipo

## 📋 Contenido

### 1. Por qué esta semana, y no antes

El Sprint 1 (dominio y persistencia) ya usaba credenciales de base de datos. Este sprint es donde
aparece el primer secreto **generado por el proyecto** — la clave con la que se firman las
sesiones o los tokens JWT — así que es el punto natural para dejar la disciplina fija antes de
que existan más.

### 2. La regla no negociable

- ❌ Ninguna contraseña, clave de firma, API key o cadena de conexión hardcodeada en el código,
  en `docker-compose.yml` ni en el `Dockerfile` (ver [`docs/docker-guia.md`](../../../docs/docker-guia.md))
- ✅ Todo secreto vive en variables de entorno, cargadas desde un archivo `.env` que **nunca** se
  commitea (debe estar en `.gitignore` desde la semana 1)
- ✅ El repositorio sí incluye `.env.example`, con las mismas claves y valores de ejemplo/vacíos,
  para que cualquier compañero sepa qué variables necesita sin exponer ninguna real

```text
# .env.example — sí se commitea
DATABASE_URL=postgresql://user:password@localhost:5432/app_db
AUTH_SECRET_KEY=change-me-in-local-env
```

```text
# .env — NUNCA se commitea, cada integrante tiene el suyo
DATABASE_URL=postgresql://real_user:real_password@localhost:5432/app_db
AUTH_SECRET_KEY=<valor generado localmente, distinto por entorno>
```

### 3. Qué hacer si un secreto ya se commiteó por error

No basta con borrarlo en el siguiente commit — sigue en el historial de Git. Rotar el secreto
(generar uno nuevo) y avisar al equipo es obligatorio; limpiar el historial es un paso adicional,
no un sustituto de rotar.

### 4. Aplicación al proyecto real

<!-- 📝 Instrucción: verificar en equipo antes de abrir el primer PR de este sprint -->

- [ ] `.env` está en `.gitignore` (confirmar, no asumir)
- [ ] `.env.example` existe y está actualizado con las variables que usa auth (clave de sesión/JWT)
- [ ] `git log -p` sobre los archivos de configuración no muestra ningún secreto real
- [ ] El code review de cada PR de este sprint revisa explícitamente que no haya secretos nuevos

## 📚 Recursos Adicionales

Ver [`docs/docker-guia.md`](../../../docs/docker-guia.md#reglas-no-negociables) — la misma regla
de "credenciales solo en `.env`" ya aplica ahí desde la semana 2.
