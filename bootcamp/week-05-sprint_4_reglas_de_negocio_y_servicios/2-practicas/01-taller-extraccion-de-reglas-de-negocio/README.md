# Taller — Extracción de Reglas de Negocio y Diseño de Servicios

<!-- 📝 Instrucción: taller guiado por el instructor, en equipo. Primero se practica la técnica
     con ejemplos aislados, después se aplica al proyecto real. Sigue el orden exacto. -->

## Objetivo

Practicar la técnica de extracción de reglas de negocio y separación en capa de servicios
**antes** de tocar el código real del proyecto — es la aplicación práctica de `1-teoria/01` y
`1-teoria/02` en un solo flujo continuo.

## Duración estimada

120 minutos (dentro del bloque de Ambiente de Formación).

## Pasos

### 1. Identificación de reglas implícitas (20 min)

Aplica la técnica "¿y si...?" de `1-teoria/02` a estas tres historias de usuario aisladas
(ejemplos genéricos, no del proyecto de nadie en particular):

- "Como cliente, quiero cancelar mi pedido."
- "Como usuario, quiero registrarme con mi correo electrónico."
- "Como administrador, quiero aprobar solicitudes de reembolso."

- [ ] Para cada historia, escribe al menos 2 reglas de negocio implícitas que encontraste
- [ ] Para cada regla, escribe qué pasaría si el sistema **no** la aplicara

### 2. Separación de capas en código existente (25 min)

- [ ] Elige un endpoint ya construido en el Sprint 3 de tu proyecto real
- [ ] Marca en el código (comentario o resaltado) qué parte es: protocolo/validación de entrada, regla de negocio, acceso a datos
- [ ] Si las tres están mezcladas en un mismo bloque, anota exactamente dónde empieza y termina cada una

### 3. Diseño de servicio, solo firma (25 min)

Sin implementar todavía: para una de las reglas encontradas en el paso 1, escribe únicamente la
firma de la función de servicio que la aplicaría (nombre + parámetros + qué excepción de dominio
podría lanzar). Ver el ejemplo ilustrativo de `1-teoria/01` como referencia de formato.

- [ ] Firma de servicio escrita para al menos una regla
- [ ] Nombre de la excepción de dominio asociada, si aplica

### 4. Excepciones de dominio (20 min)

- [ ] Define al menos 2 nombres de excepción de dominio para las reglas del paso 1 (ej. `OrderAlreadyCancelledError`)
- [ ] Para cada una, decide (sin implementar) a qué código HTTP se mapearía en el endpoint

### 5. Aplicación al proyecto real (30 min)

Ahora sí, sobre el backlog real del Sprint 4 del equipo:

- [ ] Aplicar la técnica "¿y si...?" a las historias reales movidas a "Sprint Actual"
- [ ] Documentar las reglas encontradas como criterios de aceptación adicionales en los issues
- [ ] Diseñar (firma + excepción) al menos un servicio real antes de empezar a codificarlo

## Cierre del taller

Al terminar, el equipo tiene: la técnica practicada con ejemplos aislados, al menos un endpoint
real del Sprint 3 con las capas identificadas, y el diseño de al menos un servicio real listo
para codificar en el bloque de Trabajo Autónomo.
