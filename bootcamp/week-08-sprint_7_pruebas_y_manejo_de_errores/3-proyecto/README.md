# Proyecto Semana 8 — Sprint 7: Pruebas, Errores y Docker Optimizado

## 📋 Instrucciones

Con el taller de cobertura ya resuelto (`2-practicas/01-taller-cobertura-de-pruebas-criticas/`),
este entregable cierra el Sprint 7:

1. **Sprint Review** (Criterio RAP-1): qué se planificó, qué se construyó, demo y % de avance acumulado.
2. **Pre-checklist del gate de la semana 9**: verificación temprana de lo que la semana 9 exigirá
   sobre Docker, para no descubrirlo tarde.

Completa `starter/entregable-s08-sprint-7-review.md` con tu equipo.

## ❓ Preguntas Guía

- ¿Los 5 flujos críticos identificados en el taller ya tienen prueba automatizada corriendo en CI?
- ¿Qué endpoint todavía responde errores con un formato distinto al resto de la API?
- Si hoy clonaras el repo en una máquina limpia y corrieras `docker compose up`, ¿qué fallaría?

## ✅ Checklist de Cierre de Sprint 7

- [ ] `entregable-s08-sprint-7-review.md` completo
- [ ] Al menos un PR de esta semana revisado en code review y mergeado a `develop` con CI en verde
- [ ] Manejo de errores consistente verificado en los endpoints principales
- [ ] `Dockerfile`(s) con build multi-stage y `.dockerignore` aplicados
- [ ] CI corriendo pruebas contra la imagen Docker real
- [ ] Pre-checklist del gate de semana 9 revisado — cualquier ítem pendiente queda como tarea explícita para la semana 9, no como sorpresa
