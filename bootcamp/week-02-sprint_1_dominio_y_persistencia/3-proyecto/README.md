# Proyecto Semana 2 — Sprint 1: Dominio y Persistencia

## 📋 Instrucciones

Con la técnica practicada en `2-practicas/01-taller-modelado-de-dominio/`, este sprint construye
sobre el proyecto real:

1. El **modelo de dominio** del alcance de este sprint (Criterio RAP-1, aplicado al backlog real)
2. El **esquema de datos y migraciones** que persisten ese modelo
3. El servicio `db` en `docker-compose.yml`, con volumen persistente
4. Al menos un PR de `feature/*` revisado y mergeado a `develop`, con CI en verde (Criterios RAP-3 y RAP-4)
5. El **Sprint Review**, que cierra formalmente el sprint

Completa `starter/entregable-s02-sprint-1-review.md` con tu equipo al final de la semana.

## ❓ Preguntas Guía

- ¿Qué entidades del backlog priorizado (semana 1) tienen menos dependencias y por eso arrancan primero este sprint?
- ¿Qué reglas de negocio del dominio **no** puede garantizar el esquema de base de datos por sí solo, y en qué capa del código sí se van a validar?
- ¿Qué migración tendría que revertirse (`downgrade`) si una decisión de modelado cambia a mitad de sprint?
- ¿El servicio `db` de `docker-compose.yml` conserva los datos si el equipo hace `docker compose down` sin `-v`?

## ✅ Checklist de Cierre del Sprint 1

- [ ] `entregable-s02-sprint-1-review.md` completo
- [ ] Modelo de dominio del alcance del sprint documentado (entidades, relaciones, cardinalidad)
- [ ] Migraciones aplicables desde una base de datos vacía, sin pasos manuales
- [ ] `docker compose up db` levanta la base de datos con volumen persistente
- [ ] Al menos una `feature/*` mergeada a `develop`, revisada por un compañero, con CI en verde
- [ ] El commit sigue Conventional Commits, referencia el issue de la historia
