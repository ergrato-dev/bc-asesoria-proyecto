# Configuración del Entorno de Desarrollo

## 🎯 Objetivos

- Instalar y verificar localmente todas las herramientas del stack elegido
- Crear la estructura de carpetas del proyecto según estilo API REST

## 📋 Contenido

### 1. Instalación local (Criterio RAP-2)

Según el stack elegido en `03-seleccion-herramientas-desarrollo.md`:

- IDE (VS Code recomendado, con extensiones del stack)
- Runtime (Node, Python, Go, JDK — según corresponda)
- Motor de base de datos (PostgreSQL, MySQL, MongoDB) — local o vía Docker (ver `08-contenerizacion-gradual-docker.md`, esta semana solo se instala, no se dockeriza aún)
- Cuenta y CLI de GitHub

### 2. Estructura de carpetas — estilo API REST

Referencia (adaptar nombres de carpetas internas al stack, la separación `be`/`fe` se mantiene):

```
proyecto/
├── be/                    # Backend
│   └── app/
│       ├── models/        # Entidades de dominio
│       ├── schemas/       # DTOs de entrada/salida
│       ├── routers/       # Endpoints, agrupados por dominio
│       ├── services/      # Lógica de negocio
│       └── utils/
├── fe/                    # Frontend
│   └── src/
│       ├── api/
│       ├── components/
│       ├── pages/
│       └── hooks/
├── docs/                  # Documentación técnica del proyecto
└── docker-compose.yml     # Se completa gradualmente — ver 08-contenerizacion-gradual-docker.md
```

Ver estructura completa en [`docs/estandar-codigo-template.md`](../../../docs/estandar-codigo-template.md#6-estructura-del-proyecto-api-rest).

### 3. Verificación de la instalación

Cada integrante del equipo debe poder correr, sin errores:

```bash
# Ejemplo (adaptar al stack elegido)
node --version   # o python --version, go version, java --version
git --version
```

### 4. Aplicación al proyecto real

<!-- 📝 Instrucción: cada integrante verifica su propia instalación -->

- [ ] Todos los integrantes tienen el runtime instalado y verificado
- [ ] La estructura de carpetas `be/`/`fe/` existe en el repositorio
- [ ] El proyecto corre localmente con un "hello world" del stack elegido (aún sin lógica real)

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para guías de instalación oficiales por stack.
