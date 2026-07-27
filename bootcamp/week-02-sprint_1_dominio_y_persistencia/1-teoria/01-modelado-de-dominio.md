# Modelado de Dominio

## 🎯 Objetivos

- Identificar las entidades, atributos y relaciones del dominio real del proyecto
- Distinguir entidad, value object y agregado antes de tocar el esquema de base de datos
- Producir un modelo de dominio verificable contra el informe de diseño y el backlog

## 📋 Contenido

### 1. Por qué modelar antes de crear tablas

El error más común del Sprint 1 es abrir el editor de la base de datos y empezar a crear tablas
directamente. El modelo de dominio (qué existe, cómo se relaciona, qué reglas tiene) se piensa
**antes** que el esquema — el esquema es una traducción del modelo, no al revés. Si el modelo
cambia a mitad de sprint, el esquema tiene que seguirlo, nunca al contrario.

### 2. Vocabulario mínimo

| Concepto | Definición breve |
|---|---|
| **Entidad** | Algo con identidad propia que persiste en el tiempo (`User`, `Order`) — dos entidades con los mismos atributos son distintas si su identidad lo es |
| **Value Object** | Algo definido solo por sus atributos, sin identidad propia (`Money`, `Address`) — dos con los mismos valores son intercambiables |
| **Agregado** | Grupo de entidades y value objects que se tratan como una unidad de consistencia (`Order` + sus `OrderItem`) |
| **Raíz de agregado** | La entidad por la que se accede a todo el agregado — ninguna otra parte del sistema modifica el agregado saltándose la raíz |

No hace falta implementar Domain-Driven Design táctico completo para un proyecto de bootcamp —
basta con nombrar bien qué es entidad y qué es value object antes de decidir tablas o colecciones.

### 3. De historia de usuario a entidad

Cada historia de usuario del backlog (semana 1) menciona sustantivos del dominio. Ese es el punto
de partida:

```
Como cliente, quiero agregar productos a mi carrito para comprarlos después.
                          ↑            ↑
                     entidad Product   entidad/agregado Cart (raíz: Cart, contiene CartItem)
```

Extrae todos los sustantivos del backlog antes de nombrar la primera tabla. Si dos historias
usan el mismo sustantivo con significado distinto, es una señal de que falta una conversación con
el Product Owner del equipo, no un problema técnico.

### 4. Relaciones y cardinalidad

Para cada par de entidades relacionadas, define la cardinalidad explícitamente (`1:1`, `1:N`,
`N:M`) y quién es dueño de la relación. Una relación `N:M` sin definir casi siempre esconde una
entidad implícita (ej. `Enrollment` entre `Student` y `Course`) — nómbrala si tiene atributos
propios (fecha de inscripción, calificación).

### 5. Aplicación al proyecto real

<!-- 📝 Instrucción: completar en equipo, con el backlog del Sprint 1 a la vista -->

- [ ] Lista de entidades y value objects del alcance de este sprint (no todo el backlog completo)
- [ ] Relaciones y cardinalidad entre ellos, documentadas en `3-proyecto/`
- [ ] Agregados identificados donde aplique — no todo el modelo necesita agregados explícitos

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para referencias de Domain-Driven Design y `4-recursos/ebooks-free/README.md` para el minibook de DDD.
