# Vídeo vertical — reproductor propio vs. YouTube

**Descripción:** Definir la solución técnica para implementar vídeo vertical (formato Shorts/Reels) en la web y APP de MARCA, evaluando reproductor propio frente a embeber el feed de YouTube Shorts.

**Estado:** Investigación — pendiente de validar con IT y editorial antes de plantear MVP.

**Dependencias:** IT (Belén Gómez), equipo editorial de vídeo, integración existente con Dailymotion (ver [hub-videos](../hub-videos/README.md))

**Encaja con:** Hub de Vídeos, KPI de video views

**Contexto relevante:** el hub-videos ya registra que el vídeo vertical en México está parado por Caliente (ver status 2026-04-16 en [hub-videos](../hub-videos/README.md)). Esta investigación es para España/English, y aplica también cuando se retome MX.

---

## Objetivo

Decidir si el vídeo vertical de MARCA se sirve desde reproductor propio (Dailymotion, ya integrado) o desde un embed del feed de YouTube Shorts, y documentar por qué.

---

## Qué hace el resto del sector (investigación, agosto 2026)

### Reproductor propio — es la tendencia dominante

La mayoría de medios de referencia han migrado a reproductor propio para no ceder audiencia ni monetización a plataformas sociales:

**Deportivos:**
- **ESPN** — feed vertical propio estilo TikTok en su app (lanzado agosto 2025), construido in-house
- **Bleacher Report** — feed scrolleable propio integrado en la app

**Generalistas:**
- **New York Times** — pestaña "Watch" con ~20 vídeos verticales curados al día, reproductor propio. Consumo de vídeo duplicado en un año
- **Washington Post** — reproductor vertical propio desde 2015, ~50% de la producción diaria ya es vídeo vertical
- **CNN** — feed vertical propio en la app (lanzado nov. 2025), llamado "Shorts" pero con tecnología propia, no de YouTube
- **BBC, Bild, USA Today, Hearst, TIME, People, Trusted Media Brands** — feeds verticales on-site, según VideoWeek (dic. 2025)

**Motivo declarado por los ejecutivos del sector:** recuperar control sobre monetización y experiencia. Datos citados: eCPMs de display 3-5x más altos que el CPM tradicional en formato vertical inmersivo, mayor retención y frecuencia de visita.

**Proveedores tecnológicos usados por el sector** (para contexto, no todos aplicables a MARCA):
- **Dailymotion Vertical Player** — ya integrado en MARCA (SRT/IA). Soporta embed nativo vertical en web y apps, SDKs iOS/Android, Picture-in-Picture optimizado desde agosto 2025
- **JWX (ex-JW Player)** — producto de feed vertical swipeable, lanzado feb. 2026
- **Bytes (Media.net)** — infraestructura de feeds verticales tipo TikTok, usado por Time

### YouTube — no resuelve el caso de uso

**YouTube Player for Publishers (PfP), ya integrado en MARCA:** es un player estándar de YouTube personalizado para medios (prioridad de venta publicitaria, hosting/transcodificación), nacido en 2016 dentro de la Digital News Initiative. Está orientado a vídeo horizontal 16:9 y **no incluye ningún modo de feed vertical ni versión Shorts**.

**Embed de Shorts individuales:** técnicamente posible vía iframe estándar (`youtube.com/embed/ID`) forzando `aspect-ratio: 9/16` por CSS, pero es un vídeo suelto, no un feed.

**Embed de un feed tipo "mi pestaña de Shorts":** no existe una solución oficial de YouTube. Los únicos caminos son widgets de terceros (EmbedSocial, Curator, Flockler, Tagembed, Elfsight) que sincronizan vía la YouTube Data API y muestran una galería/carrusel — no el scroll infinito vertical de la app de YouTube.

**Ningún medio de referencia investigado (ESPN, CNN, NYT, Washington Post, Time) usa YouTube como base de su feed vertical on-site.** Todos han optado por tecnología propia o de terceros especializados.

---

## Opción recomendada: publicación dual (Dailymotion + YouTube)

En lugar de migrar el catálogo histórico o elegir una sola plataforma, el planteamiento con menos fricción dado el stack actual de MARCA es publicar en ambos destinos desde el momento de creación:

```
Producción del vídeo vertical (master propio)
        ↓
  Publicación simultánea (doble destino):
  → Dailymotion (vía API)  → sirve el reproductor vertical en marca.com / APP
  → YouTube (como hoy)     → sigue como canal de distribución/descubrimiento
```

Dailymotion tiene API de subida programática (`developers.dailymotion.com/docs/upload-videos`) que permite automatizar este flujo dual, comparable a la integración ya existente con YouTube.

### Pregunta de desbloqueo previa

¿Existe hoy un archivo maestro de los Shorts en algún sitio interno (editor de vídeo, DAM, servidor de producción) antes de subirlos a YouTube, o el flujo actual es "se edita y se sube directo a YouTube" sin dejar copia propia?

- **Si existe master interno:** no es una migración, es añadir Dailymotion como segundo destino de publicación. El archivo ya existe en la infraestructura propia.
- **Si no existe master:** no se debe descargar el vídeo desde YouTube para republicarlo (viola sus Términos de Servicio). Solo se podría recuperar localizando el archivo original en el editor/NLE de producción. Si no existe, ese contenido histórico se queda solo en YouTube.

### Lo que esta opción no resuelve

Las vistas que ya tiene el contenido histórico en YouTube no se trasladan a la métrica de video views de MARCA — ese impacto ya está perdido para el pasado. La ganancia real empieza con el contenido nuevo publicado en Dailymotion desde el lanzamiento.

---

## Pasos para arrancar

1. **Verificar con producción/editorial** dónde vive el archivo maestro de los Shorts hoy — determina si hay catálogo histórico recuperable o si el cambio aplica solo hacia adelante
2. **Validar con IT (Belén Gómez)**: capacidad de automatizar subida dual vía API de Dailymotion en el momento de publicación, y estado real de la integración con Dailymotion ya en marcha (ticket NP-754, proyecto SRT/IA en hub-videos)
3. **Definir el modelo de publicación**: autopublicación en ambos destinos o YouTube como paso manual/opcional según edición
4. **Revisar el caso de México** una vez validado en España/English — recordar que está parado por Caliente

---

## KPIs de seguimiento

| KPI | Línea base | Objetivo tras lanzamiento |
|---|---|---|
| Video views de contenido vertical propio (Dailymotion) | Medir antes de lanzar | Crecimiento sobre línea base |
| Ratio media plays / PV en contenido vertical | Ver ratios actuales en hub-videos | Comparar con benchmark de English (~20% abril 2025) |
| eCPM de vídeo vertical vs. horizontal | — | Referencia sector: 3-5x superior |

---

## Personas involucradas

- Karen Rodrigues Pita — Product Owner
- Belén Gómez — Project Manager IT (dependencia técnica, integración Dailymotion)
- Equipo editorial de vídeo — origen de los masters, flujo de producción

---

## Fuentes de la investigación (agosto 2026)

- [ESPN to launch TikTok-style video feed in new app](https://awfulannouncing.com/espn/tiktok-video-feed-new-app.html)
- [ESPN App Launch: Personalized Show, Video Feed Among New Features](https://www.sportico.com/business/media/2025/espn-app-launch-sportscenter-tiktok-feed-ai-video-feeney-1234867398/)
- [Publishers Turn to On-Site Vertical Video to Build Stickier Audience Relationships — VideoWeek](https://videoweek.com/2025/12/01/publishers-turn-to-on-site-vertical-video-to-build-stickier-audience-relationships/)
- [Media Briefing: Publishers turn to vertical video to compete with creators and grow ad revenue in 2026 — Digiday](https://digiday.com/media/media-briefing-publishers-turn-to-vertical-video-to-compete-with-creators-and-grow-ad-revenue-in-2026/)
- [How Tiktok inspired the New York Times vertical video strategy — Press Gazette](https://pressgazette.co.uk/publishers/broadcast/how-tiktok-inspired-the-new-york-times-vertical-video-strategy/)
- [JWX bets publishers can fight social with swipeable vertical video](https://ppc.land/jwx-bets-publishers-can-fight-social-with-swipeable-vertical-video/)
- [Dailymotion Vertical Player — developer docs](https://developers.dailymotion.com/docs/vertical-player)
- [Dailymotion — Upload videos API](https://developers.dailymotion.com/docs/upload-videos)
- [Digital News Initiative: Introducing the YouTube Player for Publishers](https://www.blog.google/outreach-initiatives/google-news-initiative/digital-news-initiative-introducing/)
- [How to embed YouTube Shorts — Document360](https://docs.document360.com/docs/embed-youtube-shorts)
