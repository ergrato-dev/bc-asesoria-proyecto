# Definición de Estándares de Codificación

## 🎯 Objetivos

- Completar un `CODING_STANDARDS.md` propio del proyecto real
- Instalar formateadores y herramientas de análisis estático del stack elegido

## 📋 Contenido

### 1. Por qué documentar el estándar antes de codificar (Criterio RAP-3)

Sin un estándar escrito, cada integrante nombra variables, tablas y archivos a su criterio — el
código se vuelve inconsistente desde el primer sprint. El estándar se define una vez, en la
semana 1, y se aplica el resto del trimestre.

### 2. Qué debe cubrir el estándar

- Idioma: nomenclatura técnica en **inglés**, comentarios en **español**
- Reglas de nombrado: variables, funciones, clases, tablas, campos (ver plantilla completa)
- Indentación y longitud de línea por stack
- Documentación de código: cuándo comentar (¿qué? ¿para qué? ¿impacto?) y cuándo no

### 3. Plantilla lista para usar

No se redacta desde cero — se completa [`docs/estandar-codigo-template.md`](../../../docs/estandar-codigo-template.md), que ya trae la estructura y ejemplos de referencia para varios stacks.

### 4. Herramientas de análisis estático

| Stack | Linter | Formatter |
|---|---|---|
| Python | ruff / flake8 | ruff format / black |
| TypeScript/React | eslint | prettier |
| Go | go vet | gofmt |
| Java | checkstyle | IDE formatter |

### 5. Aplicación al proyecto real

<!-- 📝 Instrucción: completar en equipo, con el stack ya decidido -->

- [ ] `CODING_STANDARDS.md` completado en la raíz del repositorio (a partir de la plantilla)
- [ ] Linter y formatter instalados y corriendo localmente
- [ ] Prueba real: el linter falla ante una violación intencional (no solo config sin probar)

## 📚 Recursos Adicionales

Ver `4-recursos/webgrafia/README.md` para documentación oficial de linters por stack.
