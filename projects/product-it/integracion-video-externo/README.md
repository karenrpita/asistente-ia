# Integración automática de vídeo externo

**Descripción:** Automatizar la ingesta de contenido de vídeo de fuentes externas (agencias, clubs, ligas) para aumentar el stock del hub sin coste editorial incremental.

**Estado:** Propuesta — pendiente de validación con IT

**Dependencias:** IT (Belén Gómez), acuerdos comerciales con agencias

**Encaja con:** Hub de Vídeos, estrategia OTT, KPI de stock total de vídeo

---

## Objetivo

Pasar de un modelo de publicación manual de vídeo externo a un pipeline automático que ingeste, clasifique y publique contenido de agencias y partners sin intervención editorial en cada pieza.

El resultado esperado es multiplicar el stock disponible de vídeo (especialmente para las ediciones English y México, donde la cobertura propia es limitada) sin aumentar el equipo.

---

## Por qué es rápido

- El estándar de distribución de vídeo entre agencias y medios es MRSS (Media RSS): un feed XML que las agencias ya generan. No requiere desarrollo de API personalizado.
- AP ya está integrada como fuente. El proceso de ingesta ya existe en alguna forma — se trata de automatizarlo y replicarlo.
- Si Xalok soporta ingesta de MRSS (validar con IT), el MVP es casi 100% configuración.
- Si Xalok no lo soporta nativamente, el MVP es un script ligero (cron job) que lee el feed y crea los CT Vídeo vía la API del CMS. Desarrollo estimado: 3-5 días de un desarrollador.

---

## Fuentes prioritarias

### Fase 1 — MVP (activar en 2-4 semanas)

| Fuente | Tipo | Estado | Acción necesaria |
|---|---|---|---|
| AP Sports | Agencia | Existe pero probablemente manual | Automatizar la ingesta existente |
| Reuters Sport | Agencia | Mencionada como objetivo en hub-videos | Activar acuerdo y configurar feed MRSS |
| UEFA / LaLiga | Federación / Liga | Sin acuerdo activo | Verificar si tienen feed de distribución de clips |

### Fase 2 — Expansión

| Fuente | Tipo | Valor principal |
|---|---|---|
| Sportradar | Agencia | Highlights de competiciones con menor cobertura editorial |
| beIN Sports clips | TV/agencia | Clips de ligas internacionales (Premier, Bundesliga, Serie A) |
| Real Madrid TV / Atlético TV | Clubs | Contenido oficial de los clubs más seguidos por la audiencia |
| Agencias grupo RCS (La Gazzetta) | Grupo | Intercambio sin coste adicional — explorar con dirección |

---

## Arquitectura del pipeline

```
Feed MRSS de agencia
        ↓
  Ingesta automática (cron cada 15-60 min)
        ↓
  Mapeo de metadatos:
  - Título → campo título CT Vídeo
  - Descripción → campo texto CT Vídeo
  - Tags de agencia → tags editoriales MARCA
  - Categoría deportiva → sección MARCA
  - Thumbnail → imagen destacada
        ↓
  Cola de revisión opcional (o autopublicación directa)
        ↓
  Publicación en CT Vídeo de Xalok
        ↓
  Distribución automática al hub y secciones
```

### Decisión clave: ¿revisión humana o autopublicación?

- **Autopublicación:** máxima velocidad, mínima carga editorial. Requiere buenas reglas de filtrado (no publicar todo, solo lo relevante).
- **Cola de revisión:** un editor aprueba en un clic antes de publicar. Añade 5-10 minutos de latencia pero evita publicaciones incorrectas.

Recomendación para el MVP: cola de revisión ligera. Cuando el sistema lleve 2-3 semanas funcionando y el equipo confíe en las reglas de filtrado, se puede pasar a autopublicación en categorías confiables.

---

## Reglas de filtrado (MVP)

No todo el contenido de una agencia es relevante para MARCA. El sistema debe filtrar automáticamente:

- Incluir solo vídeos con tags o categorías en la lista de deportes cubiertos por MARCA
- Excluir contenido marcado como "restricted" o con derechos geográficos que excluyan España
- Excluir vídeos con duración inferior a 20 segundos o superior a 30 minutos (fuera de los rangos útiles)
- Priorizar contenido relacionado con LaLiga, Champions, selección española, fútbol americano (para English)

---

## Metadatos y SEO

Aplicar desde el primer día las reglas de titulación del CT Vídeo del hub:

- Título reformateado según guía SEO: `[Equipo 1] - [Equipo 2]: [descripción del clip] | [Competición]`
- Thumbnail: usar el que envía la agencia si es de calidad; si no, marcar para revisión
- Tags: mapear los tags de la agencia a los tags editoriales de MARCA (crear tabla de equivalencias)
- Texto: usar la descripción de la agencia como base, limitada a 80 palabras

---

## Alcance del MVP

Lo mínimo que tiene que funcionar para considerar el proyecto lanzado:

1. Feed MRSS de AP automatizado (ya existe el acuerdo — es automatizar lo que hoy es manual)
2. Feed MRSS de Reuters configurado y activo
3. Cola de revisión operativa en el CMS
4. Reglas de filtrado básicas aplicadas
5. Publicación automática al hub una vez aprobado

Todo lo demás (Fase 2, autopublicación, IA para titulación) es expansión posterior.

---

## Lo que no entra en el MVP

- Integración con clubs o ligas (requiere negociación más larga)
- Generación automática de títulos con IA (proyecto SRT/IA ya existe por separado — pueden convergir en Fase 2)
- Distribución a redes sociales
- Personalización por edición (España vs English vs México) — se puede añadir en Fase 2

---

## Pasos para arrancar

1. **Validar con IT** si Xalok tiene módulo de ingesta MRSS nativo o si requiere desarrollo → Belén Gómez
2. **Confirmar estado del acuerdo con Reuters** y si tienen feed MRSS disponible → equipo comercial / Damien
3. **Revisar cómo funciona hoy la ingesta de AP** — documentar el proceso actual antes de automatizarlo
4. **Definir la tabla de mapeo de tags** (agencia → MARCA) — tarea editorial, no técnica
5. **Construir el MVP** con IT una vez validado el punto 1

---

## KPIs de seguimiento

| KPI | Línea base | Objetivo a 30 días de lanzamiento |
|---|---|---|
| Vídeos publicados por semana | Medir antes de lanzar | +50% sobre la línea base |
| Tiempo desde ingesta hasta publicación | Manual: horas | Automático: <30 minutos |
| Porcentaje de vídeos autopublicados vs rechazados en cola | — | >80% aprobados (indica buenas reglas de filtrado) |
| Video views del contenido de agencia | — | Medir y comparar con contenido propio |

---

## Personas involucradas

- Karen Rodrigues Pita — Product Owner
- Belén Gómez — Project Manager IT (dependencia técnica)
- Damien Santiago — Estrategia de audiencias y fuentes de vídeo
- Equipo editorial de vídeo — Definición de reglas de filtrado y mapeo de tags
