# Proyecto Semana 4 — Sprint 3: API CRUD de Entidades Core

## 📋 Instrucciones

Con el patrón de diseño de endpoints resuelto en `2-practicas/01-taller-diseno-de-endpoints-rest/`,
este entregable cierra el Sprint 3 sobre el proyecto real:

1. Codificar el CRUD completo de las entidades core del backlog (las que correspondan a este
   sprint según `docs/plan-curricular.md`), siguiendo el patrón de `1-teoria/01-diseno-de-endpoints-rest.md`
2. Verificar que la API responde dentro del contenedor Docker, configurada por `.env`
3. Cerrar el sprint con el Sprint Review (plantilla en `starter/entregable-s04-sprint-3-review.md`)

## ❓ Preguntas Guía

- ¿Qué entidades core quedaron sin CRUD completo y por qué (bloqueo, dependencia, alcance)?
- ¿Los DTOs de entrada/salida de cada endpoint fueron revisados por el compañero que hizo el code review, o solo el código?
- ¿La API responde igual dentro del contenedor que en local, o hubo que ajustar algo en el `.env`?

## ✅ Checklist de Cierre de Sprint 3

- [ ] `entregable-s04-sprint-3-review.md` completo
- [ ] CRUD de cada entidad core del sprint codificado (crear, listar paginado, obtener, actualizar, eliminar)
- [ ] DTOs de entrada/salida separados del modelo de dominio en cada endpoint
- [ ] Al menos un PR de `feature/*` mergeado a `develop`, revisado por un compañero, con CI en verde
- [ ] API respondiendo en el puerto mapeado del contenedor Docker, config por variables de entorno
- [ ] Sprint Review realizado con el instructor
