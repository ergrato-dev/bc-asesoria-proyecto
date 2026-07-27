# El Gate Docker de Entrega

## 🎯 Objetivos

- Entender qué significa que el gate Docker de la semana 9 sea "sin alternativa"
- Verificar el gate paso a paso: clon limpio, `.env`, `docker compose up`
- Saber qué hacer cuando algo no levanta

## 📋 Contenido

### 1. "Sin alternativa" significa exactamente eso

Docker viene creciendo gradualmente desde la semana 1 (ver
[`docs/docker-guia.md`](../../../docs/docker-guia.md)). Esta semana es donde esa progresión se
verifica de una vez, completa. No hay una opción B:

- ❌ No se acepta un proyecto que corre "en mi máquina" fuera de contenedores
- ❌ No se acepta un `docker-compose.yml` que solo levante la base de datos
- ❌ No se acepta "funciona si primero corro este script manual antes de `docker compose up`"
- ✅ Se acepta únicamente: clon limpio + `.env` desde `.env.example` + `docker compose up` = proyecto completo arriba

Si el gate no pasa, el Producto de esta semana queda topado — ver `rubrica-evaluacion.md`. No hay
negociación posible sobre este punto, sin importar cuánto código funcional tenga el resto del
proyecto.

### 2. Cómo verificarlo paso a paso

```bash
# 1. Clonar el repositorio en una carpeta completamente nueva
#    (o pedirle a un compañero de otro equipo que lo clone)
git clone <url-del-repo> verificacion-gate
cd verificacion-gate

# 2. Copiar el archivo de variables de entorno de ejemplo
cp .env.example .env
# Revisar que .env.example tenga TODAS las variables que el proyecto necesita
# (si falta una, el compose fallará o un servicio arrancará mal configurado)

# 3. Levantar todo con un solo comando
docker compose up

# 4. Verificar cada servicio por separado
docker compose ps          # todos los servicios en estado "running" o "healthy"
curl http://localhost:<puerto-backend>/health
curl http://localhost:<puerto-frontend>
```

El punto crítico: esto se ejecuta en una carpeta que **nunca tuvo** configuración manual previa.
Si el proyecto solo funciona porque alguien instaló algo a mano en su máquina hace tres sprints,
el gate no pasa.

### 3. Qué hacer si algo no levanta (debugging básico de Compose)

| Síntoma | Causa probable | Qué revisar |
|---|---|---|
| Un servicio se reinicia en bucle | Falta una variable de entorno o falla la conexión a otro servicio | `docker compose logs <servicio>` |
| Backend arranca antes de que la BD esté lista | Falta `depends_on` con `condition: service_healthy` | Healthchecks en `docker-compose.yml` (ver semana 7) |
| `docker compose up` pide algo manual | Hay un paso no documentado ni automatizado | Mover ese paso al `Dockerfile` o a un script que corra dentro del contenedor |
| Puerto ya en uso | Otro proceso local ocupa el puerto mapeado | Cambiar el mapeo en `docker-compose.yml` o liberar el puerto |
| Variable de entorno vacía en el contenedor | `.env.example` no la incluye o el nombre no coincide | Comparar `.env.example` contra lo que el código realmente lee |

```bash
# Comandos de diagnóstico más usados
docker compose logs -f <servicio>       # logs en vivo de un servicio
docker compose exec <servicio> sh       # entrar al contenedor a inspeccionar
docker compose config                   # ver el compose ya resuelto (variables interpoladas)
docker compose down -v && docker compose up --build   # reconstruir desde cero, sin caché de volúmenes
```

### 4. Reglas no negociables (recordatorio)

- Credenciales y secretos van en `.env`, nunca hardcodeados en `Dockerfile` ni en `docker-compose.yml`
- Cada `Dockerfile` documenta en comentario para qué existe cada capa (build vs. runtime)
- El Sprint Review final se demuestra sobre la versión containerizada, no sobre el entorno local

## 📚 Recursos Adicionales

Ver [`docs/docker-guia.md`](../../../docs/docker-guia.md) — checklist completo del gate en la
sección "Checklist de Verificación — Semana 9 (Gate de Entrega)".
