# Taller — Cobertura de Pruebas Críticas

<!-- 📝 Instrucción: taller guiado por el instructor, en equipo, con el proyecto real a la vista.
     Sigue el orden exacto — cada paso depende del anterior. -->

## Objetivo

Identificar los 5 flujos más críticos del proyecto real y verificar (o dejar escrita) al menos
una prueba automatizada por cada uno. Es la aplicación práctica de `1-teoria/01-...md` sobre
código real, no un ejercicio de ejemplo.

## Duración estimada

90 minutos (dentro del bloque de Ambiente de Formación de 6h).

## Pasos

### 1. Identificar los 5 flujos críticos (20 min)

- [ ] Como equipo, listar los flujos del backlog cuyo fallo rompería la operación del proyecto (autenticación, creación de la entidad principal, cualquier flujo con dinero o datos sensibles, etc.)
- [ ] Priorizar y quedarse con exactamente 5 — si hay más candidatos, el resto queda anotado como deuda técnica en un issue
- [ ] Registrar los 5 en la tabla de la sección "Resultado del Taller" más abajo

### 2. Auditar cobertura actual (15 min)

- [ ] Para cada uno de los 5 flujos, revisar si ya existe una prueba automatizada (unitaria o de integración)
- [ ] Marcar cada flujo como `Cubierto` / `Parcial` / `Sin cobertura`

### 3. Escribir las pruebas faltantes (40 min)

- [ ] Para cada flujo `Sin cobertura` o `Parcial`, escribir al menos una prueba del caso feliz
- [ ] Para los flujos más sensibles (auth, dinero, permisos), agregar al menos un caso límite (entrada inválida, recurso inexistente, usuario sin permiso)
- [ ] Correr la suite completa y confirmar que pasa en CI

### 4. Manejo de errores (15 min)

- [ ] Revisar los endpoints de los 5 flujos críticos: ¿responden con el formato de error consistente definido en `1-teoria/01-...md`?
- [ ] Corregir los que aún devuelven un `500` genérico o un formato distinto al del resto de la API

## Resultado del Taller

| # | Flujo crítico | Cobertura antes | Prueba(s) agregada(s) | Cobertura después |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

## Cierre del taller

Al terminar, los 5 flujos críticos identificados tienen al menos una prueba automatizada corriendo
en CI, y sus endpoints responden errores con formato consistente. Esto alimenta directamente el
Sprint Review de `3-proyecto/`.
