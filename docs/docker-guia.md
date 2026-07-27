# 🐳 Guía de Contenerización Gradual (Docker)

Docker es la única herramienta de contenerización de este bootcamp — **sin alternativa**. A
diferencia del lenguaje, framework o base de datos (que cada equipo elige según su diseño), esto
no es una decisión abierta. La entrega del 90% de avance en la semana 9 **debe** poder levantarse
completa con `docker compose up`.

---

## Por qué gradual, no todo de una vez

Dockerizar el proyecto completo en la semana 1, antes de tener código, es trabajo desechable y
resta horas al arranque de codificación (ver `bootcamp/week-01-.../README.md`). La
contenerización crece junto con el código: cada sprint agrega al `docker-compose.yml` exactamente
lo que ese sprint construyó, nunca más.

---

## Progresión por Semana

| Semana | Qué se dockeriza | Entregable Docker verificable |
|---|---|---|
| 1 | Docker/Docker Compose instalado. `Dockerfile` esqueleto de backend y frontend (aún no funcional) | `docker --version` y `docker compose version` corren en la máquina de cada aprendiz |
| 2 — Sprint 1 (dominio y persistencia) | Servicio `db` en `docker-compose.yml`, con volumen persistente | `docker compose up db` levanta la base de datos |
| 3 — Sprint 2 (auth) | Backend dockerizado (`Dockerfile` funcional), conectado a `db` por red de compose | `docker compose up db be` levanta backend + BD |
| 4 — Sprint 3 (API CRUD core) | API responde dentro del contenedor, config por variables de entorno (`.env`) | Endpoints responden en el puerto mapeado del contenedor, no en local |
| 5 — Sprint 4 (reglas de negocio) | Servicios/reglas de negocio corren igual dentro y fuera del contenedor | Tests contra el backend containerizado pasan |
| 6 — Sprint 5 (integración FE-BE) | Frontend dockerizado (`Dockerfile` multi-stage: build → servidor estático/Nginx) | `docker compose up` levanta backend + frontend + BD juntos |
| 7 — Sprint 6 (flujos secundarios) | Healthchecks, `depends_on` con condición, red interna | `docker compose up` sin errores de orden de arranque |
| 8 — Sprint 7 (pruebas y errores) | Imágenes optimizadas (multi-stage, `.dockerignore`), CI corre contra imágenes reales | Imagen final sin dependencias de desarrollo; build de CI usa las mismas imágenes |
| 9 — Sprint 8 (cierre 90%) | **Gate de entrega** | `docker compose up`, en un clon limpio, levanta el proyecto completo end-to-end sin pasos manuales adicionales |

---

## Estructura Esperada (desde la semana 6 en adelante)

```
proyecto/
├── be/
│   ├── Dockerfile
│   └── .env.example
├── fe/
│   ├── Dockerfile
│   └── .env.example
├── docker-compose.yml
└── .dockerignore
```

---

## Reglas No Negociables

- ❌ No se acepta un entregable de semana 9 que corra solo "en mi máquina", fuera de contenedores
- ❌ No se acepta un `docker-compose.yml` que solo levante la base de datos, dejando backend/frontend en local
- ✅ `docker compose up` debe funcionar sobre un clon limpio del repositorio + `.env` copiado de `.env.example`
- ✅ Credenciales y secretos van en `.env`, nunca hardcodeados en `Dockerfile` ni en `docker-compose.yml`
- ✅ Cada `Dockerfile` documenta en comentario para qué existe cada capa (build vs runtime)

---

## Checklist de Verificación — Semana 9 (Gate de Entrega)

- [ ] `git clone` limpio + `cp .env.example .env` + `docker compose up` levanta el proyecto completo
- [ ] Backend, frontend y base de datos corren cada uno en su propio contenedor
- [ ] No hay ningún proceso corriendo fuera de Docker para que el proyecto funcione
- [ ] El Sprint Review final se demuestra sobre la versión containerizada, no sobre el entorno local del aprendiz

---

## Recursos

- [Docker Compose — documentación oficial](https://docs.docker.com/compose/)
- [Dockerfile best practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
- Referencia de patrón real: `docker-compose.yml` de `proyecto-be_fastapi-fe_react` (servicios `db`, `be`, `fe`, `mailpit`, healthchecks, red interna aislada)
