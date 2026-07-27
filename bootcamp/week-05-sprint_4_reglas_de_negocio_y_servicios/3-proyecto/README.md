# Proyecto Semana 5 — Sprint 4: Reglas de Negocio y Servicios

## 📋 Instrucciones

Con la técnica ya practicada (`2-practicas/01-taller-extraccion-de-reglas-de-negocio/`), este
bloque cierra el Sprint 4 sobre el proyecto real:

1. **Codificación del sprint**: capa de servicios, validaciones de dominio, excepciones de
   negocio, sobre las historias de usuario movidas a "Sprint Actual" en el Sprint Planning.
2. **Sprint Review**: cierre formal del sprint con el instructor, documentando avance,
   demo y estado de Docker.

Completa `starter/entregable-s05-sprint-4-review.md` con tu equipo al final de la semana.

## ❓ Preguntas Guía

- ¿Qué reglas de negocio estaban implícitas en las historias del Sprint 4 y no se habían identificado antes del Sprint Planning?
- ¿Qué endpoints heredados del Sprint 3 tenían lógica de negocio mezclada con el controlador, y cómo quedaron después de extraerla a servicios?
- ¿Los tests de reglas de negocio pasan igual dentro del contenedor Docker que en local?

## ✅ Checklist de Cierre de Sprint 4

- [ ] `entregable-s05-sprint-4-review.md` completo
- [ ] Capa de servicios separada de los endpoints, verificada en code review
- [ ] Al menos una `feature/*` mergeada a `develop` con CI en verde
- [ ] Tests de reglas de negocio pasan contra el backend containerizado (no solo en local)
