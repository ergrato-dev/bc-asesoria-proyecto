# Interpretación del Informe de Diseño

## 🎯 Objetivos

- Identificar los documentos que componen el informe de diseño del trimestre anterior
- Extraer de ellos un plan de trabajo de construcción, no solo leerlos

## 📋 Contenido

### 1. ¿Qué es el informe de diseño?

Es el conjunto de evidencias que tu equipo produjo y aprobó el trimestre anterior:

- **Anteproyecto**: problema, justificación, alcance
- **Arquitectura**: componentes del sistema, capas, tecnologías propuestas
- **Casos de uso**: interacciones entre actores y sistema
- **Historias de usuario**: `Como <rol>, quiero <acción> para <beneficio>`, con criterios de aceptación

Este informe **ya está aprobado** — esta semana no se rediseña, se interpreta para construir.

### 2. De diseño a plan de trabajo

Interpretar el informe de diseño para definir un plan de trabajo (Criterio RAP-1) significa
responder tres preguntas por cada historia de usuario:

1. **¿Qué construye?** (una entidad de dominio, un endpoint, una pantalla, una regla de negocio)
2. **¿De qué depende?** (otra historia debe estar lista antes — ej. no hay login sin usuarios)
3. **¿En qué sprint entra?** (ver `02-planificacion-agil-scrum-sprints.md`)

Esto convierte una lista de historias sueltas en un backlog ordenado por dependencias técnicas.

### 3. Aplicación al proyecto real

<!-- 📝 Instrucción: completar en equipo, con el informe de diseño real a la vista -->

- Lista todas las historias de usuario del informe de diseño
- Marca las que son "core" (sin ellas el sistema no tiene sentido) vs "secundarias"
- Identifica dependencias técnicas entre ellas (diagrama simple, papel o Miro)

### 4. Errores comunes

- ❌ Tratar el informe de diseño como sugerencia y empezar a codificar algo distinto
- ❌ No identificar dependencias — intentar construir login antes que el modelo de usuario
- ❌ Confundir "requisito no funcional" (ej. tiempo de respuesta) con historia de usuario

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para guías de refinamiento de backlog.
