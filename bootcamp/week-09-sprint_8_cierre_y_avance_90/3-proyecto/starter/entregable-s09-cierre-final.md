<!-- 📝 Instrucción: completar con tu equipo y tu proyecto real. No dejar secciones vacías —
     donde algo no aplique, justificar por qué, no dejar en blanco. El gate Docker no es opcional:
     si no pasa, decirlo explícitamente, no maquillarlo. -->

# Cierre del Trimestre — [Nombre de tu Proyecto]

## 1. Gate Docker de Entrega — sin alternativa

**Checklist obligatorio** (copiado de [`docs/docker-guia.md`](../../../../docs/docker-guia.md#checklist-de-verificación--semana-9-gate-de-entrega)):

- [ ] `git clone` limpio + `cp .env.example .env` + `docker compose up` levanta el proyecto completo
- [ ] Backend, frontend y base de datos corren cada uno en su propio contenedor
- [ ] No hay ningún proceso corriendo fuera de Docker para que el proyecto funcione
- [ ] El Sprint Review final se demuestra sobre la versión containerizada, no sobre el entorno local del aprendiz

**Resultado del gate**: ☐ Pasa &nbsp;&nbsp; ☐ No pasa

**Evidencia** (quién verificó, cuándo, en qué máquina — idealmente alguien fuera del equipo):
...

**Si no pasa**: qué falla exactamente (`docker compose logs`), y el plan concreto para corregirlo
antes de la Sprint Review final.
...

## 2. Avance del Proyecto

| Métrica | Valor |
|---|---|
| Historias totales del backlog | |
| Historias en estado "Hecho" | |
| % de avance | |

**Meta:** ≥90%. Si el resultado es menor, explicar qué falta y por qué:
...

## 3. Code Review Final

**Alcance revisado**: (todo el repositorio / módulos específicos si aplica, justificar)

**Hallazgos bloqueantes corregidos esta semana**:
- ...

**Hallazgos NO bloqueantes** → ver sección 4 (Deuda Técnica).

## 4. Deuda Técnica Documentada para el Siguiente Trimestre

| Qué | Por qué no se resolvió | Impacto | Prioridad |
|---|---|---|---|
| | | | |

<!-- Mínimo 1 fila real. Un proyecto sin ningún pendiente honesto es sospechoso, no ejemplar. -->

## 5. Demo Integrada

- **Flujo demostrado**: ...
- **Se ejecutó sobre contenedores**: ☐ Sí &nbsp;&nbsp; ☐ No (si "No", el gate no pasa — ver sección 1)
- **Caso de error mostrado**: ...

## 6. Hand-off al Siguiente Trimestre

- **Qué queda por codificar**: ...
- **Qué queda por documentar**: ...
- **Qué queda por implementar/desplegar**: ...
- **Riesgos o bloqueos conocidos**: ...

## 7. Roles del Equipo (Sprint 8)

| Integrante | Rol |
|---|---|
| | Scrum Master |
| | Product Owner |
| | Dev |
| | QA |
