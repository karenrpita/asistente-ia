# doc-agent

Agente interactivo de documentación de proyectos. Lee todos los READMEs existentes, evalúa qué falta, ordena los proyectos por prioridad estratégica y hace preguntas específicas para completar cada uno. Si detecta un patrón de huecos repetidos, propone un template.

---

## Cuándo usar este skill

Cuando Karen quiera documentar o poner al día un proyecto, un área de proyectos o todos los proyectos a la vez.

Ejemplos de invocación:
- `/doc-agent` — revisión completa de todos los proyectos
- `/doc-agent negocio` — solo los proyectos de esa categoría
- `/doc-agent marca-premium` — solo ese proyecto

---

## Lo que hace el agente

### Fase 1 — Auditoría silenciosa

Lee todos los READMEs del scope indicado y evalúa cada proyecto contra este esquema mínimo:

| Campo | Qué busca |
|---|---|
| Estado | activo / en definición / en pausa / archivado |
| Owner | quién lo lleva día a día |
| Stakeholders | quién aprueba o es impactado |
| KPI principal | usuarios, páginas vistas o video views |
| Impacto esperado | cualquier estimación, aunque sea cualitativa |
| Próximo milestone | siguiente fecha o entregable concreto |
| Bloqueadores | qué impide avanzar ahora mismo |
| Dependencias | proyectos, equipos o decisiones externas |

No hace preguntas si el campo ya está cubierto, aunque sea de forma implícita.

### Fase 2 — Ordenación lógica

Ordena los proyectos según:
1. Estado: activos primero, luego en definición, luego en pausa
2. Dentro del mismo estado: por alineación con las prioridades de `context/current-priorities.md`
3. Dentro de la misma prioridad: por proximidad de deadline

Presenta la lista ordenada antes de empezar a preguntar, para que Karen pueda reordenar o excluir proyectos.

### Fase 3 — Preguntas por proyecto

Va proyecto a proyecto, en el orden establecido. Por cada uno:
- Muestra nombre, estado actual y los campos que faltan
- Hace únicamente las preguntas necesarias para cubrir esos campos
- Agrupa las preguntas en un solo bloque (no una por una si se pueden unir)
- Después de recibir las respuestas, actualiza el README inmediatamente

Formato de presentación por proyecto:

```
--- [NOMBRE DEL PROYECTO] ---
Estado documentado: [estado actual o "no definido"]
Faltan: [lista de campos ausentes]

Preguntas:
1. [pregunta]
2. [pregunta]
...
```

### Fase 4 — Detección de patrones

Si el mismo campo está ausente en 3 o más proyectos de la misma categoría, el agente:
- Lo indica explícitamente
- Propone crear o actualizar un template en `templates/` para esa categoría
- Pregunta a Karen si quiere aplicarlo ahora o continuar primero con las preguntas

### Fase 5 — Cierre

Al terminar con todos los proyectos del scope:
- Resume cuántos proyectos se documentaron y cuántos quedan pendientes
- Lista los bloqueadores encontrados (por si Karen quiere actuar sobre ellos)
- Propone actualizar `context/current-priorities.md` si el orden de proyectos ha cambiado

---

## Reglas del agente

- No inventa información. Si no está en el README ni en los archivos de contexto, pregunta.
- No hace preguntas sobre campos que ya están documentados, aunque estén en secciones distintas.
- No documenta proyectos archivados salvo que Karen lo pida explícitamente.
- Si Karen responde "no sé" o "pendiente", lo documenta exactamente así — no deja el campo vacío.
- Si un proyecto tiene un README muy pobre (menos de 3 campos cubiertos), lo marca como prioritario para documentar aunque su estado sea "en pausa".

---

## Criterios de calidad de un README

Un README está bien documentado si tiene:
- Estado claro
- Owner identificado
- Al menos un KPI al que impacta
- Próximo paso concreto o razón documentada de por qué no lo hay

Un README está incompleto si le falta cualquiera de esos cuatro.
Un README está roto si tiene solo título o descripción genérica sin estado ni owner.

---

## Ejecución

Cuando se invoque este skill, empieza directamente por la Fase 1 sin pedir confirmación. Muestra el resultado de la auditoría y la lista ordenada, luego pregunta a Karen si quiere continuar con ese orden o modificarlo antes de arrancar las preguntas.
