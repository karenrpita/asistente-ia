# Mundial 2026 — MARCA

**Descripción:** Cobertura editorial y producto digital del Mundial de Fútbol 2026 dentro del ecosistema MARCA. Portal con contenido editorial, datos deportivos en tiempo real, vídeo y espacios publicitarios patrocinados.

**Estado:** Activo — en desarrollo
**Última actualización:** 2026-04-15
**Responsable de producto:** Karen Rodrigues Pita

---

## Contexto

El Mundial 2026 es el evento deportivo más relevante del año y una oportunidad estratégica para MARCA en tres frentes: captación de audiencia nueva, fidelización de usuarios existentes y monetización a través de patrocinios y publicidad programática.

El proyecto se articula dentro del medio existente (marca.com) con una sección especial para el Mundial, gestionada íntegramente desde Xalok como CMS editorial.

## KPIs asociados

| Métrica | Impacto esperado |
|---|---|
| Usuarios | Alto — evento de captación masiva |
| Páginas vistas | Alto — cobertura en vivo, resultados, especiales |
| Video views | Medio-alto — vídeos de goles, resúmenes, highlights |

---

## Fechas clave

| Hito | Fecha |
|---|---|
| Pruebas Roba C (Lácer + aposteros) | 17 abril 2026 |
| Límite migraciones Xalok para el Mundial | 27 abril 2026 |
| Lanzamiento del portal/sección | Antes del 11 junio 2026 |
| Inicio del Mundial | 11 junio 2026 |
| Final del Mundial | julio 2026 |

---

## Stack tecnológico

- **CMS:** Xalok (gestión editorial completa: creación, publicación y flujo de contenidos)
- **Integraciones:** API de datos deportivos (resultados, fixture, estadísticas en tiempo real)
- **Publicidad:** Ad server (GAM — Google Ad Manager) + publicidad programática

---

## Tipos de contenido

- Noticias y artículos de cobertura periodística
- Resultados, fixture y tabla de posiciones en tiempo real
- Vídeos: goles, resúmenes, highlights
- Contenido de marca (branded content, notas patrocinadas)

---

## Audiencia

Modelo mixto B2B/B2C:
- **B2C:** aficionados al fútbol (España, México, USA y audiencia global hispanohablante)
- **B2B:** marcas y patrocinadores con presencia en el producto (4-10 patrocinadores directos)

---

## Modelo de patrocinios y publicidad

Modelo mixto: patrocinadores directos con acuerdos cerrados + publicidad programática en espacios restantes.

### Patrocinadores y widgets activos

| Patrocinador | Formato | Estado | IP |
|---|---|---|---|
| LG | Widget cuenta atrás | En validación | ES |
| Luckia | Widget de partidos | En validación | ES |
| Skechers | Power Ranking (logo integrado) | Mockup en preparación | ES |
| Lácer | Roba C | Pruebas 17 abril | ES |
| Aposteros (x2) | Roba C | Pruebas 17 abril | ES |

- En edición España (IPs restantes): autopubli de Power Ranking.
- Pendiente: confirmar si hay que rehacer los widgets para UEdit tras las migraciones de Xalok.

---

## Productos y funcionalidades

### Power Ranking
- Patrocinado por Skechers (integración de logo en mockup, Nacho Delgado lo presenta al cliente).
- **Estado del desarrollo (casi terminado):**
  - Front en desktop y mobile: casi cerrado (NIT)
  - Mockup con logo Skechers: en preparación
  - Dato en campos para directos finalizados y crónicas: listo
  - Widget para noticias con Top 5 por partido: listo

### Micrositios de patrocinadores
- Entregable principal del proyecto.
- Espacios dedicados o branded hubs para cada patrocinador dentro de la cobertura del Mundial.
- Pendiente: definir estructura, URLs y alcance por patrocinador.

### Fans United
- En curso: pruebas con el registro de usuarios.

---

## Dependencias

| Dependencia | Impacto | Estado |
|---|---|---|
| Migraciones Xalok (deadline 27 abril) | Si no llegan a tiempo, puede ser necesario rehacer widgets para UEdit | Crítico |
| App — widgets del Mundial | El inicio del desarrollo está pendiente de arrancar | Bloqueado |

---

## Personas involucradas

| Nombre | Rol | Implicación |
|---|---|---|
| Karen Rodrigues Pita | Head of Product | Responsable del producto |
| Nacho Delgado | (editorial / desarrollo) | Power Ranking y presentación a Skechers |
| Belen Gomez | Project Manager (IT) | Dependencias técnicas y entregas |
| Javier | Product Manager | Coordinación editorial |
