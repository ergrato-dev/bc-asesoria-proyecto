# bc-asesoria-proyecto — Asesoría Desarrollo, Codificación del Proyecto

Contexto operativo para Claude Code en este repo. Las convenciones de contenido pedagógico
(estructura de semana, formato de teoría/prácticas/proyecto, estándares de assets SVG, idioma
código/documentación) están en [`.github/copilot-instructions.md`](.github/copilot-instructions.md)
— no se duplican aquí, léelo antes de crear o editar contenido de una semana.

## Qué hace único a este repo frente a los demás `bc-*`

- **Single-track, 9 semanas fijas.** A diferencia de `bc-propuesta-tecnica` (dual-track
  cadena-formación/oferta-abierta) o `bc-aidev` (36 semanas en 5 etapas), aquí
  `bootcamp/week-XX-slug/` cuelga directo de `bootcamp/` — un README de semana enlaza a la raíz
  con `../../README.md` (2 niveles, no 3).
- **No hay caso de estudio ficticio compartido.** El proyecto real de cada equipo (ya diseñado el
  trimestre anterior) es el hilo conductor desde la semana 1 — `3-proyecto/` nunca usa un caso
  inventado. El contenido genérico (`1-teoria/`, `2-practicas/`) es de **proceso**, agnóstico de
  stack: no asumas FastAPI+React ni ningún lenguaje al escribir contenido nuevo, salvo que el
  ejemplo esté marcado explícitamente como ilustrativo.
- **Semana 1 está partida en dos mitades**, no es una semana de teoría normal: primera mitad =
  alistamiento acelerado (las 7 actividades originales del RAP comprimidas), segunda mitad = ya
  hay código (Sprint 0). No repartas el contenido de semana 1 como si fueran 5 días iguales.
- **Semanas 2-9 llevan tema de sprint concreto en el nombre de carpeta** (ej.
  `week-03-sprint_2_autenticacion_y_autorizacion`), no solo `sprint_N` genérico — el usuario pidió
  explícitamente que el nombre comunique la tarea esperada. Si agregas o renombras una semana,
  mantén ese patrón.
- **Docker es obligatorio y gradual, sin alternativa.** No es una herramienta más de la tabla —
  ver [`docs/docker-guia.md`](docs/docker-guia.md). El gate de la semana 9 (`docker compose up`
  end-to-end) es una condición de aprobación del Producto, no una nota opcional. No generes
  contenido que presente Docker como "una opción entre varias" para el entregable final.
- **Git flow con `develop`** (`feature/* → develop → main`) es una regla para los **proyectos
  reales de los equipos**, documentada en [`docs/git-workflow.md`](docs/git-workflow.md) — este
  propio repositorio de contenido, en cambio, sigue el mismo modelo simple de un solo `main` que
  usan los demás `bc-*` (ver `CONTRIBUTING.md`). No confundas ambos flujos al escribir ejemplos.

## Trazabilidad RAP

`docs/plan-curricular.md` es la fuente de verdad de qué saberes/criterios RAP cubre cada semana.
Cualquier `rubrica-evaluacion.md` nueva o editada debe alinearse con su tabla — usa el agente
`rap-trazabilidad-reviewer` para verificarlo, no lo hagas a ojo.

## Reglas que rompen fácil

- **Scope de commit**: `feat(week-NN)`/`fix(week-NN)` corto, nunca el slug completo de la
  carpeta — ver `CONTRIBUTING.md`.
- **Datos reales**: nunca usar datos reales de aprendices, instructores o proyectos
  institucionales en ejemplos — solo datos sintéticos (línea roja global del usuario).
- Antes de commitear cualquier cambio que mueva/renombre/cree carpetas de semana: correr
  `bash scripts/verificar-enlaces.sh` (o invocar la skill `verificar-estructura`).

## Skills y agentes de este repo

- `verificar-estructura` (skill) — corre la verificación mecánica de nombres de carpeta y
  enlaces relativos, más una checklist de lo que no se puede verificar automáticamente.
- `rap-trazabilidad-reviewer` (agente) — verifica que cada rúbrica semanal referencie el
  criterio RAP, saberes de proceso y estado Docker que le corresponden según
  `docs/plan-curricular.md`.
