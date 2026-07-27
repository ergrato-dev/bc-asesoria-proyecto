# Taller — Gate Docker y Cierre del Trimestre

<!-- 📝 Instrucción: taller guiado por el instructor, en equipo, con el proyecto real a la vista.
     El paso 1 es el más importante de todo el trimestre: si falla, todo lo demás espera. -->

## Objetivo

Verificar formalmente el gate Docker de entrega y cerrar la semana con el code review final, la
medición de avance y la demo integrada. Es la aplicación práctica de `1-teoria/01` a `1-teoria/03`
en un solo flujo continuo.

## Duración estimada

180 minutos (dentro del bloque de Ambiente de Formación de 6h).

## Pasos

### 1. Verificación del gate Docker (60 min) — sin alternativa

- [ ] Clonar el repositorio en una carpeta completamente nueva (o pedirle a un compañero de otro equipo que lo clone)
- [ ] Copiar `.env.example` a `.env` — sin editar valores a mano fuera de lo que el ejemplo ya documenta
- [ ] Ejecutar `docker compose up` desde esa carpeta limpia
- [ ] Verificar con `docker compose ps` que backend, frontend y base de datos están arriba, cada uno en su propio contenedor
- [ ] Probar el backend (`curl` o navegador) y el frontend en los puertos mapeados del contenedor
- [ ] Si algo falla: documentar el fallo exacto (`docker compose logs <servicio>`), corregirlo, y repetir el paso desde el clon limpio — no desde el repo ya "arreglado" en local

**No se avanza al paso 2 hasta que este paso esté en verde.** Es el gate — no hay parcial.

### 2. Code review final cruzado (45 min)

- [ ] Intercambiar repositorio con otro equipo (o asignar el review al instructor)
- [ ] Recorrer el repositorio completo con la checklist de `1-teoria/01-code-review-final-y-deuda-tecnica.md`
- [ ] Registrar cada hallazgo: bloqueante (se corrige hoy) o deuda técnica (se documenta)

### 3. Medición de avance (30 min)

- [ ] Revisar el backlog completo en GitHub Projects (todas las historias, no solo el Sprint 8)
- [ ] Calcular el % de historias "Hecho" sobre el total del backlog
- [ ] Si el resultado es menor a 90%, documentar qué falta y por qué

### 4. Resolución de hallazgos bloqueantes (30 min)

- [ ] Corregir lo que bloquea el gate o el 90% de avance
- [ ] Repetir el paso 1 si se tocó algo relacionado con Docker

### 5. Ensayo de la demo integrada (15 min)

- [ ] Levantar el proyecto con `docker compose up`
- [ ] Ejecutar el flujo end-to-end elegido, cronometrado
- [ ] Ajustar lo que no fluyó bien antes de la Sprint Review real

## Cierre del taller

Al terminar, el repositorio del proyecto real cumple el checklist completo de la sección
"📌 Entregable de la Semana" del `README.md` de esta semana. Lo que quede pendiente pasa a las 4
horas de Trabajo Autónomo, priorizando siempre lo que bloquea el gate sobre lo que no.
