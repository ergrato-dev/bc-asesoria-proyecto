---
name: verificar-estructura
description: Verifica que la estructura del bootcamp (nombres de carpeta week-NN-slug, enlaces relativos de navegación, navegación anterior/siguiente, trazabilidad RAP en rúbricas) sea consistente con el contenido real. Usar antes de commitear cualquier cambio que mueva, renombre o cree carpetas de semana, o cuando se sospeche de un enlace roto.
allowed-tools: Bash(scripts/verificar-enlaces.sh) Bash(bash scripts/verificar-enlaces.sh) Read Grep
---

# Verificar estructura del bootcamp

Repo single-track, 9 semanas fijas (`bootcamp/week-01-...` a `week-09-...`), sin split de etapas
ni de oferta-abierta/cadena-formación — a diferencia de otros repos `bc-*` del catálogo, aquí un
enlace a la raíz desde un README de semana es siempre `../../README.md` (2 niveles, no 3).

## Qué hacer

1. Correr el script mecánico primero:

   ```bash
   bash scripts/verificar-enlaces.sh
   ```

   Verifica automáticamente:
   - Que toda carpeta bajo `bootcamp/` siga `week-NN-slug` (NN de 2 dígitos, slug en minúsculas,
     puede contener dígitos — ej. `week-09-sprint_8_cierre_y_avance_90`).
   - Que todo enlace relativo `[texto](ruta)` en cualquier `.md` del repo resuelva a un archivo o
     carpeta real (ignora URLs http/mailto y contenido dentro de bloques ` ``` `, que suelen ser
     ejemplos de plantilla, no enlaces reales).
   - Que cada `bootcamp/week-XX/README.md` tenga una sección "Navegación".

   Falso positivo conocido y aceptado: URLs con paréntesis anidados tipo `(book)`. Si el script
   reporta algo distinto a eso, es un enlace roto real.

2. Lo que el script **no** puede verificar (revisar a mano, es juicio de contenido):
   - Que cada `rubrica-evaluacion.md` referencie el criterio RAP correcto según la tabla de
     trazabilidad en [`docs/plan-curricular.md`](../../docs/plan-curricular.md) — usar el agente
     `rap-trazabilidad-reviewer` para esto, no lo hagas a ojo.
   - Que el "Estado Docker esperado" de cada semana (misma tabla) coincida con lo que
     [`docs/docker-guia.md`](../../docs/docker-guia.md) describe para esa semana.
   - Que la tabla "Contenido por Semana" del `README.md` raíz siga sincronizada con los temas
     reales de cada `week-XX/README.md`.

3. Regla de profundidad de `../` para enlaces de navegación:
   - Archivo en `bootcamp/week-NN.../README.md` → raíz del repo: `../../README.md` (2 niveles).
   - Mismo archivo → `docs/algo.md`: `../../docs/algo.md`.
   - Archivo dentro de una subcarpeta de semana (`1-teoria/`, `2-practicas/practica-NN/`,
     `3-proyecto/`, `4-recursos/*`, `5-glosario/`) → suma un nivel más por cada subcarpeta de
     profundidad antes de aplicar las reglas anteriores.

Si el script encuentra problemas, corrígelos y vuelve a correrlo hasta que imprima
`OK: sin problemas detectados.` antes de dar por cerrado el cambio.
