# Taller — Modelado de Dominio y Esquema en 20 Minutos

<!-- 📝 Instrucción: calentamiento guiado por el instructor, ANTES de aplicar la técnica al
     proyecto real. No es un caso de estudio del bootcamp — cualquier dominio simple sirve. -->

## Objetivo

Practicar la técnica de modelado de dominio → esquema → migración sobre un dominio pequeño y
conocido, en un tiempo acotado, antes de aplicarla — con más calma — al proyecto real del equipo
en `3-proyecto/`.

## Duración estimada

45 minutos (dentro del bloque de Ambiente de Formación).

## Dominio de calentamiento

Modela el dominio de un **sistema de préstamos de biblioteca**: una persona puede tener prestados
varios libros, cada préstamo tiene fecha de inicio y fecha límite de devolución, un libro no puede
prestarse si ya está prestado.

## Pasos

### 1. Identificar entidades y value objects (10 min)

- [ ] Lista los sustantivos del dominio: `Book`, `Member`, `Loan`, ...
- [ ] Marca cuáles son entidades (tienen identidad propia) y cuáles value objects
- [ ] Identifica si `Loan` es una entidad independiente o parte de un agregado

### 2. Relaciones y cardinalidad (10 min)

- [ ] Define la cardinalidad `Member`–`Loan` y `Book`–`Loan`
- [ ] Decide quién es dueño de la relación (¿`Loan` referencia a `Book` y `Member`, o al revés?)
- [ ] Identifica la regla de negocio que el esquema por sí solo no puede garantizar (`Book` no
      puede tener dos `Loan` activos simultáneos) — anota dónde se aplicaría esa validación (capa
      de servicio, no la base de datos)

### 3. Esquema mínimo (15 min)

- [ ] Dibuja o escribe las tablas/colecciones con sus columnas y tipos
- [ ] Marca claves primarias y foráneas
- [ ] Escribe, en pseudocódigo o en el lenguaje de migraciones de tu stack, la migración de `Loan`

### 4. Puesta en común (10 min)

- [ ] Compara tu esquema con el de otro equipo — discute diferencias de modelado (no hay una
      única respuesta correcta, pero sí decisiones mejor o peor justificadas)

## Cierre del taller

Con la técnica fresca, el equipo repite exactamente estos mismos pasos sobre el dominio real del
proyecto en `3-proyecto/` — ahí sí con el peso completo de la rúbrica de esta semana.
