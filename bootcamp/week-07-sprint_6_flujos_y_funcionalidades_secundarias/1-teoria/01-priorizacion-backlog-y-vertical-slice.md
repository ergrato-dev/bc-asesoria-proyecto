# Priorización de Backlog Restante y Vertical Slice

## 🎯 Objetivos

- Priorizar el backlog restante del proyecto con criterio, no por orden de llegada
- Aplicar la técnica de vertical slice para completar casos de uso de punta a punta

## 📋 Contenido

### 1. La recta final del backlog (Criterio RAP-1)

Quedan 3 semanas de codificación (semanas 7, 8 y 9) antes del cierre con ≥90% de avance. A esta
altura el backlog restante casi nunca cabe completo — y forzarlo todo suele terminar en varias
historias a medias en vez de pocas historias terminadas. Priorizar ahora, con el informe de
diseño y el avance real como referencia, es la aplicación directa de RAP-1 en esta etapa del
proyecto.

### 2. Cómo priorizar sin perder tiempo

Una matriz simple de impacto vs. esfuerzo evita debates largos:

| | Esfuerzo bajo | Esfuerzo alto |
|---|---|---|
| **Impacto alto** | Entra primero al Sprint 6 | Evaluar si cabe — partirla en sub-tareas si es grande |
| **Impacto bajo** | Entra si sobra tiempo | Se recorta — candidata a "no incluida" documentada |

Criterios para ubicar cada historia:

- **Impacto**: ¿la usa el flujo principal del proyecto o es un caso borde poco frecuente?
- **Esfuerzo**: ¿depende de algo aún no construido, o se apoya en lo ya codificado en sprints 1-5?
- **Riesgo de dejarla a medias**: si no cabe completa esta semana, mejor no empezarla que dejarla rota

### 3. Vertical slice vs. horizontal

**Horizontal** (evitar en esta recta final): completar una capa entera para todas las historias
pendientes (ej. todos los endpoints de backend) antes de tocar la siguiente capa (frontend). El
riesgo: si el tiempo se agota, ninguna historia queda usable ni demostrable.

**Vertical slice** (el patrón de esta semana): completar una historia de punta a punta —
persistencia, lógica de negocio, endpoint, y su consumo en frontend — antes de empezar la
siguiente. El riesgo se reparte: si el tiempo se agota, lo que ya está hecho es demostrable en el
Sprint Review.

```
Horizontal:  [DB: todo] → [API: todo] → [FE: todo]     ← nada usable hasta el final
Vertical:    [DB+API+FE de la Historia A] → [Historia B] → ...   ← cada slice es demostrable
```

### 4. Qué recortar sin culpa

- Historias "nice to have" sin impacto en el flujo core del proyecto
- Historias con dependencias técnicas que aún no están resueltas y no se resuelven esta semana
- Documenta la decisión en el issue (label o comentario) — un recorte silencioso genera confusión
  en el Sprint Review y en el cierre de la semana 9

### 5. Aplicación al proyecto real

<!-- 📝 Instrucción: aplicar en el Sprint Planning breve del inicio de la semana -->

- [ ] Backlog restante listado completo en GitHub Projects (nada fuera del tablero)
- [ ] Matriz impacto/esfuerzo aplicada a cada historia pendiente
- [ ] Historias del Sprint 6 movidas a `Sprint Actual`, cada una viable como vertical slice esta semana
- [ ] Historias recortadas, documentadas con el motivo (comentario o label en el issue)

## 📚 Recursos Adicionales

Plantillas de Sprint Planning y Sprint Review en
[`docs/guia-github-projects.md`](../../../docs/guia-github-projects.md). Ver `5-glosario/README.md`
para los términos usados esta semana.
