# Proyecto Semana 6 — Sprint 5: Integración Frontend-Backend

## 📋 Instrucciones

Con el patrón ya practicado (`2-practicas/01-taller-integracion-api-frontend/`), este entregable
cierra el Sprint 5 sobre el proyecto real del equipo:

1. Las **pantallas principales** del backlog consumiendo la API real, con carga/error manejados
2. El **frontend dockerizado** con multi-stage, y `docker compose up` levantando los tres servicios
3. El **Sprint Review** con el instructor (Criterio RAP-1: interpretación del backlog del sprint)

Completa `starter/entregable-s06-sprint-5-review.md` con tu equipo antes del Sprint Review.

## ❓ Preguntas Guía

- ¿Qué pantallas del backlog son "core" para demostrar en el Sprint Review y cuáles pueden quedar para el Sprint 6?
- ¿Qué endpoint del backend cambió de contrato durante la integración, y quién lo actualizó?
- ¿Qué pasa en la pantalla si el backend no responde? ¿Se probó de verdad, apagándolo?
- ¿Corre `docker compose up` en un clon limpio del repositorio, sin pasos manuales adicionales?

## ✅ Checklist de Cierre de Sprint 5

- [ ] `entregable-s06-sprint-5-review.md` completo
- [ ] Al menos las pantallas principales consumen la API real, no datos mock
- [ ] Estado de carga y error verificados manualmente (no solo el caso feliz)
- [ ] `fe/Dockerfile` multi-stage funcional
- [ ] `docker compose up` levanta `db`, `be` y `fe` juntos en un clon limpio
- [ ] Al menos una `feature/*` de integración mergeada a `develop`, con CI en verde y revisión de un compañero
- [ ] Sprint Review realizado con el instructor
