# 🎓 Glosario — Semana 3

| Término | Definición breve |
|---|---|
| **Autenticación** | Proceso que verifica quién es el usuario (login) |
| **Autorización** | Proceso que verifica qué puede hacer un usuario ya autenticado |
| **Sesión** | Estado de autenticación guardado en el servidor, referenciado por una cookie en el cliente |
| **Token / JWT** | Credencial autocontenida (JSON Web Token) que el servidor no necesita guardar para validar |
| **Hash** | Resultado de una función de un solo sentido aplicada a la contraseña — no reversible |
| **Salt** | Valor aleatorio único por contraseña, incluido en el hash para evitar tablas precalculadas |
| **bcrypt / argon2** | Algoritmos de hashing lentos, diseñados específicamente para contraseñas |
| **Rol** | Categoría asignada a un usuario (ej. `admin`, `usuario`) que determina sus permisos |
| **RBAC** | Role-Based Access Control — modelo de autorización basado en roles |
| **401 Unauthorized** | Código HTTP: el request no está autenticado |
| **403 Forbidden** | Código HTTP: el request está autenticado pero sin permiso suficiente |
| **`.env` / `.env.example`** | Archivo de variables de entorno (nunca commiteado) y su plantilla pública sin valores reales |
| **Secreto** | Contraseña, clave de firma o credencial que nunca debe vivir en el código fuente |
