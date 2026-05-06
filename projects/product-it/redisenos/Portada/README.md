# Fase 2 — Portada

**Estado:** En diseño
**Última actualización:** 2026-05-06

---

## Contexto

Segunda fase del rediseño de MARCA 2026. Detalla los objetivos y requisitos para el rediseño de portada.

---

## Objetivos

**Simplificación y modernización:**
- Reducir contaminación visual.
- Modernizar el site y la imagen de marca.
- Mayor presencia audiovisual y formatos verticales.

**Experiencia de usuario:**
- Mejorar carga de página.
- Mejorar organización del contenido y navegabilidad.
- Prioridad a web mobile.

**Experiencia publicitaria:**
- Menos y mejores formatos publicitarios.
- Mejorar viewability y KPIs publicitarios.
- Nuevas opciones de patrocinio.

**Medición:**
- Revisión de eventos de medición (GA4, Marfeel, GFK, Comscore).
- Limpieza de eventos antiguos e inclusión de nuevas variables.

**KPIs objetivo:**
- Reducción del tiempo de carga y la tasa de rebote.
- Mejora del tiempo de permanencia y scroll depth.
- Mejora de interacciones sociales y recirculación.
- Desarrollo de la conversión hacia contenido de pago.
- Mejora de la satisfacción de usuarios.

---

## Descripción

### General

- Portada desktop: 1200px.
- Incluir botón "Subir arriba".
- Opción de volver a la posición previa en portada tras entrar en una noticia y volver atrás — dependencia con Navegación Continua.

**Plantillas de portada dinámicas según:**
- Tipo de agenda deportiva: días con muchos directos, grandes eventos (Mundial, Eurocopa, Super Bowl...).
- KPIs: si se necesita potenciar video, se incluyen más carruseles de video automáticamente.
- Publicidad: si se patrocina con formato premium, se reducen posiciones tradicionales.
- Días con menos tráfico (parones de Liga, etc.).

---

### Widgets y componentes

- Rediseño del Carrusel de Resultados.
- Nuevos widgets: clasificaciones, agenda, Últimas noticias, Más leídas, Videos, etc.

---

### Bloques y flexes

- **Bloque de personalización Mi MARCA:** preferencias del usuario al estilo apps.
- **Carrusel Stories.**
- **Agrupaciones contenido + ficha de equipo/jugador.**
- Posibilidad de mover flexes sin impactar posiciones de publicidad.
- Posibilidad de geolocalizar bloques, contenidos y streaming.
- Noticias/bloques patrocinables.
- Concepto apertura múltiple en modo carrusel: pendiente de valorar.

**Propuestas SEO sobre flexes:**

- **Redirecciones por navegador:** implementar redirecciones inteligentes (user-agent + geolocalización) que ajusten dinámicamente la URL destino según entorno (mobile, app, internacional...).
- **Flex de enlazado SEO de competiciones:** componente dinámico actualizable rápidamente desde CMS, con repositorio extenso de logos, para reforzar recirculación, autoridad semántica y crawl depth.
- **Noticias de última hora en contenidos agrupados:** sistema de disponibilidad automatizada para breaking news con agrupación en tres dimensiones (directos, breaking news, noticias top), para aumentar enlazado contextual y liberar espacio de portada. Requiere entidades estructuradas (equipos, jugadores, eventos).
- **Flexes automatizados con Marfeel:** dashboard con reglas actualizables por engagement, frescura, sección o CTR. Debe permitir ajuste editorial manual sin romper la automatización.
- **Carruseles modulares personalizables:** para top autores, top competiciones, jugadores, equipos, emisoras locales de Radio MARCA, eventos de MARCA Entradas, etc. Conectables a diferentes fuentes (CMS, Spreadsheet, CSV...).

---

### Cover content

**Elementos del cover content:**

- Marcador
- Pastilla En Directo
- Pastilla Contenido Premium (signwall/paywall)
- Foto / Video (con pie de foto, firma, icono de vídeo, autoplay + PiP, posibilidad de GIF o MP4 breve en bucle)
- Streaming
- Player de audio con reproducción transversal
- Kicker, antetítulo, título, firma, localización, fecha
- Comentar, compartir, guardar
- Patrocinio (solo logo / logo + texto / logo + texto + cuota apuestas)
- Reacciones/valoraciones bajo registro
- Duración / tiempo de lectura
- Relacionados (opción línea de tiempo vertical para directos)
- Foto/escudo/logo de competición para cover principal en agrupación de contenido

**Tipos de cover content por CT:**

| Tipo | Diferenciación |
|------|---------------|
| Noticia | Estándar |
| Directo | Icono / color / texto en kicker |
| Opinión | Foto de autor |
| Noticia especial / Coverage | Mayor presencia de imagen |
| Álbum | — |
| Videoct | Icono de video |
| Especial NIT | — |
| Contenido native (publicidad) | Fondo diferenciado |

**Casos especiales:**
- Foto de autor para Opinión.
- Enlaces en Directo a Estadísticas/Alineación.
- Enlaces en Crónica a Resumen/Estadísticas/Ficha.
- Estadísticas de jugador/partido/equipo en crónicas.

**Nuevas funcionalidades:**
- Player de vídeo vertical.
- Player de audio con reproducción activa mientras el usuario navega por el site (Radio MARCA).

---

### Peticiones de publicidad (TBD)

- Mantener posiciones de BC; valorar nuevas posiciones/agrupaciones.
- Mantener formatos pequeños (cintas y posiciones 300x100 / 320x100).
- Nueva propuesta Brand Day Affinity (topscroll + midscroll): venta simultánea, primeras ventas programáticas sin formatos intermedios.
- Aumentar tamaño del player de vídeo para mejorar viewability.
- Posibilidad de desactivar PIP por IP/edición mediante keyvalue desde GAM.
- Afiliación – Bazar: 3 posiciones + bloque de 8 aprobadas antes de la NC.
- Posiciones de marketing.
- Patrocinios de la NC: posibilidad de colores corporativos o dinámicos.
- Posibilidad de servir vídeo inread cuando no hay midscroll (petición programática).
- Viewability objetivo: mayor al 85%.
- Rediseño flexible para agilizar cambios publicitarios.
- Posibilidad de cambiar fondos bajo petición de anunciante para BD (automatizado, mobile).
- Valorar sticky billboard en desktop.

---

## Alcance y entregables

Objetivo: despliegue completo del cambio de portada. Se valorará hacerlo de forma progresiva según avances y necesidades.

Restricción: no hacer cambios antes del Mundial, principalmente por dependencias de publicidad.

Calendario de fases UX/UI y definición de producto: `Calendario Rediseño MARCA 2026.xlsx`

---

## Requisitos técnicos

**SEO:**
- JSON-LD: centralizar gestión en CMS con repositorio de variables para optimización ágil y escalable.
- Metadatos: mantener y optimizar title, description, og:image, hreflang desde configuración avanzada de CMS.
- Redundancia de enlaces: eliminar duplicados dentro de cada bloque (imagen + titular + resumen → 1 solo enlace). Auditar enlazado interno.
- Performance y refresh: mejorar tiempos de caché, estabilidad, velocidad de carga y peso de imágenes.

**Analítica:**
- Revisión, unificación y limpieza de eventos de portada.
- Ticket de referencia: [ANALITISD-2544](https://rcsuejira.atlassian.net/browse/ANALITISD-2544)

**Apps:**
- Garantizar que los cambios en backend/JSON no afecten a la home de apps.

---

## Pendientes de definición

- Análisis de datos de analítica.
- UX Research: benchmark, heurístico, mapas de calor.
- Propuestas IT.
- Presentación de prototipos.
- Capa visual.
- Requisitos/propuestas de publicidad y programática.
- Guía de etiquetado de Analítica.
- Benchmark UX.

---

## Equipos implicados

- UX/UI
- SEO
- Publicidad
- Analítica
- QA
- Producto
