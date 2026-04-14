# Central de Datos — MARCA

**Descripción:** Sistema de datos deportivos (estadísticas de equipos, jugadores y competiciones) con potencial SEO, de patrocinio y de fidelización de audiencia.

**Estado:** Activo — con base existente (captando ~10 millones de usuarios anuales). Pendiente de mejoras estructurales, ampliación de deportes e internacionalización.

## Contexto

La Central de Datos es un activo estratégico para cualquier web deportiva: captación, recirculación y patrocinio. En 12 meses ha captado ~10M de usuarios. Sin embargo, presenta deuda técnica significativa (JSON-LD incorrecto, arquitectura de URLs deficiente, limitado a fútbol de primer nivel).

## Áreas de mejora identificadas

### 1. Módulos de recirculación

- **Noticias:** integración de widgets de estadísticas automáticos o manuales según sección y tags del contenido. Widgets configurables: competiciones, equipos, jugadores.
- **Portada y portadillas:** módulos de datos clave, fichas de equipos en todas las tecnologías (ahora solo desktop), bloque de competiciones.
- **Directos:** widgets de recirculación durante partidos, fichas técnicas, alertas de eventos clave.
- **Carrusel de vídeos:** en páginas de CdD, vídeos relacionados por tags (ej: "Goles" → vídeos de goles de ese jugador).
- **Fantasy MARCA:** integrar datos de lesionados y alineaciones posibles para usuarios del Fantasy.

### 2. Optimización técnica del sistema actual

**JSON-LD:** no hay marcado actualmente. Necesario implementar:
- Propiedades específicas: `SportsEvent`, `SportsTeam`, `Athlete`
- Estandarización de datos para buscadores y asistentes de voz

**Arquitectura de URLs (problema crítico):**
- Los equipos están bajo `/resultados/` en lugar de bajo su sección propia. Ejemplo:
  - Actual: `marca.com/resultados/futbol/athletic/plantilla/C174.html`
  - Correcto: `marca.com/futbol/athletic/plantilla.html`
  - Carpetizado al cerrar temporada: `marca.com/futbol/athletic/plantilla/2023.html`
- Los jugadores están bajo `/resultados/futbol/jugadores/` en lugar de `/personaje/`:
  - Actual: `marca.com/resultados/futbol/jugadores/4b/c9/unai-simon/estadisticas/P212769.html`
  - Correcto: `marca.com/personaje/unai-simon/estadisticas.html`
  - Carpetizado: `marca.com/personaje/unai-simon/estadisticas/2023.html`

**Enlazado interno:** mejorar la relación entre entidades (ej: ficha de Leo Messi → Inter Miami, Selección Argentina, MLS) y enlazado desde noticias hacia la CdD.

**Fusión Ficha + Portadilla de contenidos:** unificar en una sola página con datos básicos (nombre, edad, posición, equipo actual, ex-equipos, competiciones) + biografía generada con IA + listado de noticias.

### 3. Nuevos datos y filtros

- Competiciones (no solo equipos/jugadores)
- Posiciones en el campo (porteros, defensas, medios, delanteros)
- Entrenadores, cuerpo técnico, presidentes/propietarios, estadios
- Palmarés de jugadores y equipos
- Histórico de lesiones
- Filtros avanzados por deporte, equipo, jugador y competición

### 4. Índice de valor propio (proyecto)

Crear un índice tipo Transfermarkt / Forbes con algoritmo propio:
- **Valor de equipos:** patrimonio neto + plantilla + trayectoria histórica y reciente
- **Valor de jugadores:** métricas individuales y colectivas, edad, club de formación, lesiones, contratos
- Potencial de patrocinio, branding y autoridad SEO

### 5. Expansión a otros deportes

- **Fútbol local y femenino:** Liga F, Primera Federación, Segunda, Tercera, Fútbol Sala
- **Baloncesto:** replicar lógica del fútbol (deporte de equipo, implementación más rápida)
- **Motor:** equipos, pilotos, rendimientos — alto interés en audiencias jóvenes
- **Tenis:** torneos, jugadores, superficies
- **NFL:** estadísticas detalladas por posición

### 6. Comparador y simulador

- **Modelo predictivo:** probabilidades de victoria basadas en ML y patrones históricos
- **Comparador:** página propia + widget integrable en fichas (ej: Lamine Yamal vs Vinicius; Yamal vs Messi en primeras temporadas)

### 7. Contenido editorial automatizado

- **Noticias automáticas:** cuando un jugador alcanza un hito (5 goles, asistencia récord…), crear noticia automática desde el CMS
- **Vídeos de estadísticas:** resumen audiovisual con infografías animadas post-partido, generados automáticamente por equipo y partido
- **Contenido para redes sociales:** infografías animadas de datos clave

### 8. Widgets interactivos

- **Quiz:** preguntas sobre el partido generadas desde CdD (ej: "¿Quién marcó más goles fuera de casa?")
- **Widgets de comparativa** integrables en artículos

## Internacionalización

Requiere hreflangs por edición en todas las páginas de CdD:
```
<link rel="alternate" Href="https://www.marca.com/mx/futbol/barcelona/plantel.html" hreflang="es-MX"/>
<link rel="alternate" Href="https://www.marca.com/futbol/barcelona/plantilla.html" hreflang="es"/>
<link rel="alternate" Href="https://www.marca.com/en/soccer/barcelona/players.html" hreflang="en"/>
<link rel="alternate" href="https://www.marca.com/us/futbol/barcelona/jugadores.html" hreflang="es-us"/>
```

Cada edición debe enlazar exclusivamente a su propia CdD (no mezclar enlazados). Al cambiar la bandera, llegar a la URL equivalente en la otra edición.

**México:** Liga MX, Liga MX Femenil, Liga de Expansión, Concachampions, Leagues Cup, MLB. Sin categorías inferiores españolas.

**USA (español):** MLS, NHL, MLB, NFL, NBA como prioridad. Enfocado al consumo de datos americano (drafts, trades, rachas, aforo, velocidad máxima, etc.).

**English:** Adaptación en inglés americano. NCAA con prioridad NFL/NBA. Estadísticas adaptadas al público americano (universidades, procedencia, etc.).

## API de datos disponible

**APIRD (API interna de Resultados Deportivos):**
- Clasificación: `sports/v1/classifications/current?site=2&type=10&tournament=0101`
- Calendario de equipo: `sports/v1/events/sport/multi/football/competitor/186?site=2`
- Partidos por jornada: `sports/v1/events/schedule/season/2023/tournament/0101/match-day/15?site=2`
- Datos previos partido: `sports/v1/events/01_0102_20231120_855_189/full?site=2`
- Estadísticas de club: `sports/v1/competitor-season-stats/sport/01/competitor/186/tournament/0101?site=2`

Además: feeds OPTA contratados (CSV/RSS) con información extensa de competiciones.

## Personas involucradas

- Damien Santiago (estrategia de audiencias)
- Pablo Caño (técnico)
- Equipo editorial por sección
