# 📏 Plantilla de Estándar de Código

<!-- 📝 Instrucción: cada equipo copia esta plantilla a la raíz de su proyecto real como
     CODING_STANDARDS.md y completa las secciones marcadas con [ ] según su stack elegido.
     No se borra ninguna sección — si algo no aplica, se escribe "No aplica" y se justifica. -->

## 1. Stack del Proyecto

| Capa | Tecnología elegida | Versión |
|---|---|---|
| Backend | [ ] | [ ] |
| Frontend | [ ] | [ ] |
| Base de datos | [ ] | [ ] |
| Contenedores | Docker + Docker Compose (obligatorio, sin alternativa) | — |
| Otros (colas, cache, etc.) | [ ] | [ ] |

---

## 2. Idioma

- Nomenclatura técnica (variables, funciones, clases, tablas, campos, ramas, commits): **inglés**
- Comentarios y documentación: **español**
- Ejemplo:

```python
# Calcula el total de la orden aplicando descuentos activos
def calculate_order_total(order: Order) -> Decimal:
    ...
```

---

## 3. Reglas de Nombrado

Completar según el stack — ejemplo de referencia (Python + TypeScript/React):

| Elemento | Convención | Ejemplo |
|---|---|---|
| Variables | `snake_case` (Python) / `camelCase` (TS) | `user_email` / `userEmail` |
| Funciones / métodos | `snake_case` (Python) / `camelCase` (TS) | `get_active_users()` / `getActiveUsers()` |
| Clases / componentes | `PascalCase` | `UserService`, `UserProfileCard` |
| Constantes | `UPPER_SNAKE_CASE` | `MAX_LOGIN_ATTEMPTS` |
| Atributos privados | prefijo `_` | `_internal_cache` |
| Archivos de componente (frontend) | `PascalCase.tsx` | `UserProfileCard.tsx` |
| Archivos utilitarios | `camelCase.ts` / `snake_case.py` | `formatDate.ts` / `date_utils.py` |
| Tablas (BD) | `snake_case`, plural | `users`, `order_items` |
| Campos (BD) | `snake_case` | `created_at`, `is_active` |
| Llave primaria | `id` | `id` |
| Llave foránea | `<tabla_singular>_id` | `user_id`, `order_id` |
| Ramas Git | `feature/kebab-case-slug` | `feature/user-authentication` |

> ✏️ **Completar:** si el stack elegido difiere (Go, Java, etc.), ajustar la tabla con la
> convención idiomática de ese lenguaje — no forzar `snake_case` de Python sobre Go, por ejemplo.

---

## 4. Documentación de Código

- Toda función pública con lógica de negocio no trivial lleva un comentario que responda:
  **¿Qué hace? ¿Para qué existe? ¿Qué impacto tiene si falla?**
- No documentar lo obvio (`# incrementa i en 1` sobre `i += 1`)
- Cabecera de archivo cuando el archivo tiene más de una responsabilidad clara:

```python
"""
Módulo: order_service.py
Qué: Lógica de negocio para creación y actualización de órdenes.
Para qué: Centraliza reglas de descuento e inventario fuera de los endpoints.
Impacto: Si falla, las órdenes pueden crearse sin validar stock disponible.
"""
```

---

## 5. Indentación y Formato

| Stack | Indentación | Line length | Formatter |
|---|:---:|:---:|---|
| Python | 4 espacios | 100 | `ruff format` / `black` |
| TypeScript/React | 2 espacios | 100 | `prettier` |
| Go | tabs (`gofmt`) | — | `gofmt` |
| Java | 4 espacios | 120 | `checkstyle` / IDE formatter |

> ✏️ **Completar** la fila del stack elegido si no está en esta tabla de referencia.

---

## 6. Estructura del Proyecto (API REST)

```
proyecto/
├── be/                    # Backend
│   └── app/
│       ├── models/        # ORM / entidades de dominio
│       ├── schemas/       # DTOs de entrada/salida (request/response)
│       ├── routers/       # Definición de endpoints, agrupados por dominio
│       ├── services/      # Lógica de negocio
│       └── utils/         # Utilidades transversales
├── fe/                    # Frontend
│   └── src/
│       ├── api/           # Llamadas a la API
│       ├── components/    # UI reutilizable
│       ├── pages/         # Una página por ruta
│       └── hooks/         # Lógica reutilizable de estado/efectos
├── docs/                  # Documentación técnica del proyecto
└── docker-compose.yml     # Levantamiento completo del entorno — obligatorio desde semana 6, ver docker-guia.md
```

---

## 7. Herramientas de Análisis Estático

- [ ] Linter configurado: ______
- [ ] Formatter configurado: ______
- [ ] Corre en pre-commit (recomendado) y/o en CI (obligatorio) — ver [`ci-cd-guia.md`](ci-cd-guia.md)

---

## 8. Checklist de Adopción (Semana 1)

- [ ] Este documento está completado y commiteado como `CODING_STANDARDS.md` en la raíz del proyecto real
- [ ] Linter y formatter instalados y corriendo localmente
- [ ] El equipo verificó que el linter falla ante una violación intencional (prueba real, no solo config)
