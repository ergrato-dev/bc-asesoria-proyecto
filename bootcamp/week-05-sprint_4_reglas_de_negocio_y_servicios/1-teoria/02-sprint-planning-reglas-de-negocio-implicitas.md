# Sprint Planning: Reglas de Negocio Implícitas

## 🎯 Objetivos

- Ejecutar el Sprint Planning del Sprint 4 en 30-45 minutos
- Detectar reglas de negocio que las historias de usuario no dejan explícitas

## 📋 Contenido

### 1. Por qué esto no quedó cubierto en el diseño original (Criterio RAP-1)

El informe de diseño y el backlog describen **qué** hace el sistema, no siempre **todas las
condiciones** bajo las que lo hace. Una historia como "Como cliente, quiero cancelar mi pedido"
no dice qué pasa si el pedido ya fue cancelado, si ya fue enviado, o si han pasado más de 24
horas. Esas reglas existen en el negocio real aunque no estén escritas — encontrarlas es parte
del trabajo de este sprint, no un vacío del diseño anterior.

### 2. Señales de una regla de negocio implícita

- **Adjetivos sin cuantificar**: "varios intentos", "poco tiempo", "varios días" — ¿cuántos, exactamente?
- **Estados no mencionados**: ¿qué pasa si la operación se repite sobre algo que ya cambió de estado?
- **Unicidad no mencionada**: ¿puede repetirse el mismo dato dos veces?
- **Límites de negocio**: montos mínimos/máximos, plazos, cantidades — casi nunca están en la historia tal cual

### 3. Técnica rápida: "¿y si...?"

Para cada historia del Sprint 4, antes de codificar, pregunta en voz alta con el equipo:

- ¿Y si el usuario repite la misma acción dos veces?
- ¿Y si el recurso ya no está en el estado que la historia asume?
- ¿Y si el dato que se envía ya existe?
- ¿Y si el usuario no tiene el rol/permiso que la historia da por hecho?

Cada respuesta que no sea "no aplica" es una regla de negocio que hay que documentar antes de
codificar, no descubrir a mitad del sprint.

### 4. Aplicación al Sprint Planning (30-45 min)

<!-- 📝 Instrucción: aplicar en equipo, con el backlog del Sprint 4 a la vista -->

- [ ] Repasar las historias movidas de `Backlog` a `Sprint Actual`
- [ ] Para cada historia, aplicar la técnica "¿y si...?" y anotar las reglas encontradas
- [ ] Añadir las reglas encontradas como criterios de aceptación adicionales del issue — no se asumen en silencio
- [ ] Si hay duda sobre una regla, validarla con el Product Owner del equipo antes de codificar, no después

## 📚 Recursos Adicionales

Ver [`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md) para la plantilla de
Sprint Planning y ceremonias ágiles, y `5-glosario/README.md` para el vocabulario de esta semana.
