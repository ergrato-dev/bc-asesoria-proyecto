# Proyecto Semana 3 — Sprint 2: Autenticación y Autorización

## 📋 Instrucciones

Con el diseño ya fijado (`2-practicas/01-taller-diseno-de-autenticacion/`), este bloque es
codificación pura sobre el proyecto real: login funcional, hashing de contraseñas y control de
acceso por rol en al menos los endpoints protegidos que el backlog de este sprint exige.

Completa `starter/entregable-s03-sprint-2-review.md` con tu equipo al cierre de la semana.

## ❓ Preguntas Guía

- ¿El endpoint de login responde igual (mismo mensaje, mismo código HTTP) ante usuario inexistente
  y contraseña incorrecta?
- ¿Qué endpoint del backlog de este sprint quedó sin protección de rol y por qué?
- ¿El backend levanta junto con la base de datos usando `docker compose up db be`, o solo corre
  "en tu máquina"?

## ✅ Checklist de Cierre del Sprint 2

- [ ] Login funcional: valida credenciales, hashea/verifica contraseña con bcrypt/argon2 o equivalente
- [ ] Al menos un mecanismo de sesión/token operativo end-to-end
- [ ] Control de acceso por rol aplicado a los endpoints protegidos del backlog de este sprint
- [ ] `.env.example` actualizado, ningún secreto hardcodeado (ver `1-teoria/03`)
- [ ] Al menos una `feature/*` por historia de auth, cada una mergeada a `develop` con PR revisado y CI en verde
- [ ] `docker compose up db be` levanta backend + base de datos sin pasos manuales adicionales
- [ ] Sprint Review completado en `starter/entregable-s03-sprint-2-review.md`
