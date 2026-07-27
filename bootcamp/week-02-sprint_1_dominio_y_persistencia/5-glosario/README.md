# 🎓 Glosario — Semana 2

| Término | Definición breve |
|---|---|
| **Dominio** | El área de negocio que el software modela — sus entidades, reglas y comportamientos |
| **Entidad** | Objeto del dominio con identidad propia que persiste en el tiempo (`User`, `Order`) |
| **Value Object** | Objeto del dominio definido solo por sus atributos, sin identidad propia (`Money`, `Address`) |
| **Agregado** | Grupo de entidades y value objects tratado como una unidad de consistencia |
| **Raíz de agregado** | Entidad por la que se accede a todo un agregado |
| **Esquema de datos** | Definición estructural de tablas/colecciones, columnas, tipos y relaciones |
| **Migración** | Cambio de esquema versionado, reproducible en cualquier entorno en el mismo orden |
| **Clave primaria** | Columna (o combinación) que identifica de forma única una fila |
| **Clave foránea** | Columna que referencia la clave primaria de otra tabla, materializando una relación |
| **ORM (Object-Relational Mapping)** | Capa que traduce entre objetos del código y filas de la base de datos |
| **Volumen persistente (Docker)** | Almacenamiento fuera del ciclo de vida del contenedor — sobrevive a `docker compose down` sin `-v` |
| **Sprint Review** | Ceremonia de cierre de sprint donde el equipo demuestra lo construido al instructor |
| **Definition of Done** | Conjunto de condiciones que un issue debe cumplir para pasar a `Hecho` (ver [`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md#5-definition-of-done)) |
