# KPIs de Negocio — MARCA

Actualizado: 2026-04-15

---

## KPIs principales

Toda decisión de producto debe evaluarse por su impacto en estas tres métricas:

| KPI | Descripcion | Por que importa |
|---|---|---|
| Usuarios | Usuarios únicos (diarios/mensuales) | Base de audiencia. Determina el valor publicitario y la relevancia del medio |
| Paginas vistas | Total de páginas vistas en el sitio | Directamente ligado a impresiones publicitarias e ingresos programáticos |
| Video views | Reproducciones de vídeo | KPI específico del negocio de vídeo. Ligado a acuerdos y monetización de vídeo |

---

## Metricas secundarias

Estas métricas no son el objetivo principal pero afectan directamente a los KPIs principales:

| Metrica | Relacion con KPIs |
|---|---|
| Tasa de rebote | Un rebote alto reduce páginas vistas y retención de usuarios |
| Tiempo en página | Indica calidad de la experiencia; baja retención = menos páginas vistas |
| Recirculacion interna | Usuarios que navegan a más de una noticia. Multiplica las páginas vistas por sesión |
| CTR en módulos de recirculación | Eficacia de los módulos para retener al usuario dentro de MARCA |
| Impresiones publicitarias | Derivado directo de páginas vistas |
| Fill rate y CPM | Eficacia de la publicidad. Determinan los ingresos reales por impresión |

---

## Regla de evaluacion

Ninguna decisión de producto o publicidad se toma sin responder:

> ¿Esta acción sube, baja o es neutra en usuarios, páginas vistas y video views?

Si una acción sube ingresos publicitarios pero baja páginas vistas o usuarios, el balance puede ser negativo para el negocio. El análisis debe ser conjunto.

---

## Estado actual

- No existe dashboard unificado de KPIs accesible al equipo de Producto.
- Los datos de partners publicitarios (Taboola, Seedtag) no tienen reporting directo.
- Las decisiones se toman sin datos suficientes en la mayoría de los casos.

**Accion pendiente:** Definir qué herramienta consolida estos KPIs y quién es responsable del reporting.

---

## KPIs de Publicidad

KPIs específicos del área publicitaria. Se evalúan de forma complementaria a los KPIs principales — una mejora en publicidad que dañe usuarios o páginas vistas es un resultado negativo.

---

### Viewability

Porcentaje de impresiones que son realmente vistas por el usuario (estándar IAB: al menos el 50% del anuncio visible durante al menos 1 segundo; para vídeo, 2 segundos).

Benchmark del sector: >70% en display, >80% en vídeo.

**Mejoras a corto plazo**
- Reposicionar los slots existentes más arriba en el viewport (above the fold) sin añadir nuevos formatos
- Eliminar o reducir slots con viewability consistentemente por debajo del 40%
- Revisar la velocidad de carga de las páginas: un scroll más lento antes de la carga mejora la exposición

**Mejoras a largo plazo**
- Rediseñar las plantillas de artículo para que los slots publicitarios queden integrados en el flujo de lectura natural
- Implementar lazy loading inteligente que cargue el anuncio justo cuando entra en viewport
- Establecer reporting automático de viewability por formato y sección para detectar degradaciones

---

### Completion rate en vídeo

Porcentaje de anuncios de vídeo (pre-roll, mid-roll) que se reproducen hasta el final o hasta el punto mínimo cobrable (generalmente el 100% para pre-roll corto, o el 30 segundos para mid-roll largo).

Benchmark del sector: >65% en pre-roll, >50% en mid-roll.

**Mejoras a corto plazo**
- Limitar la duración de pre-rolls a 15 segundos no saltables (reduce abandono)
- Reducir la frecuencia de mid-rolls en vídeos de menos de 3 minutos
- Revisar el orden de los anunciantes: los creativos más cortos o más relevantes para la audiencia deportiva primero

**Mejoras a largo plazo**
- Desarrollar targeting contextual por tipo de contenido (partido en directo vs. resumen vs. entrevista) para aumentar relevancia del anuncio
- Negociar con anunciantes formatos de vídeo nativos integrados en el player (branded content) con mayor tolerancia del usuario
- Crear un score de calidad de anuncio interno para priorizar creativos con mayor completion rate histórico

---

### Inventario de vídeo

Número total de impresiones de vídeo disponibles para monetizar. Depende directamente del volumen de video views y del número de slots por sesión de vídeo.

**Mejoras a corto plazo**
- Aumentar la distribución de contenido de vídeo en homepage y secciones de alta tráfico (sin crear fricción)
- Activar autoplay con sonido desactivado en los módulos de recirculación donde aún no esté habilitado
- Añadir un slot de pre-roll en los vídeos del hub que actualmente no lo tienen

**Mejoras a largo plazo**
- Aumentar la producción editorial de vídeo corto (60-90 segundos) para generar más sesiones de vídeo por usuario
- Construir el hub de vídeo como destino recurrente (newsletters, notificaciones push) para multiplicar sesiones de vídeo
- Explorar sindicación de contenido de vídeo externo (agencias, ligas) para aumentar inventario sin coste editorial

---

### Fill rate programático

Porcentaje de las solicitudes de anuncio (ad requests) que reciben una respuesta con anuncio real. Un fill rate bajo indica invendidos: inventario que no se está monetizando.

Benchmark orientativo: >85% en sitios de tráfico alto con header bidding activo.

**Mejoras a corto plazo**
- Revisar los pisos de precio (price floors) en los slots con mayor volumen de invendidos: bajar el floor puede recuperar demanda programática sin impactar CPM medio de forma relevante
- Activar más SSPs o DSPs en los slots con mayor volumen de invendidos
- Revisar la configuración de passback: cuando un slot queda invendido, debe servir un house ad o un formato alternativo en lugar de espacio en blanco

**Mejoras a largo plazo**
- Implementar header bidding completo si no está activo, o auditar la configuración actual con el equipo de ad tech
- Establecer acuerdos preferred deals o programmatic guaranteed con anunciantes recurrentes para garantizar cobertura mínima en fechas clave (LaLiga, Copa del Rey, eventos MARCA)
- Crear segmentos de audiencia propios (datos 1st party) para aumentar el valor del inventario remanente en open auction

---

### CPM medio

Coste por mil impresiones. Indicador de la calidad del inventario y la competitividad de la demanda programática.

**Mejoras a corto plazo**
- Segmentar el inventario por sección y contexto para comunicarlo mejor a los compradores (la sección de fútbol tiene más valor que una página genérica)
- Revisar que todos los slots tienen las categorías IAB correctamente definidas en el ad server
- Activar deal ID con los principales anunciantes de automoción, apuestas y banca (categorías de mayor CPM en medios deportivos españoles)

**Mejoras a largo plazo**
- Desarrollar una estrategia de datos 1st party que permita ofrecer segmentos verificados a los compradores (fans de Real Madrid, usuarios de Fantasy MARCA, etc.)
- Construir un paquete de patrocinio + programática para anunciantes que combinen ambas vías y justifiquen un CPM premium
- Auditar con el equipo de ad tech si existe discrepancia entre impresiones registradas en el ad server y en los DSPs (la discrepancia reduce el CPM percibido por el comprador)

---

### Patrocinios

Ingresos por acuerdos directos de patrocinio: secciones, competiciones, formatos especiales (liveticker, clasificaciones, galería). No dependen del tráfico directo pero su renovación sí está ligada a los KPIs de audiencia.

**Mejoras a corto plazo**
- Documentar el inventario de patrocinios activos: qué está vendido, a qué precio, hasta cuándo, y qué métricas se reportan al patrocinador
- Crear un one-pager de cada sección patrocinada con datos de audiencia actualizados (para facilitar renovaciones y nuevas ventas al equipo comercial)
- Identificar secciones de alto tráfico sin patrocinio activo como oportunidades inmediatas para el equipo de ventas

**Mejoras a largo plazo**
- Crear productos de patrocinio ligados al Mundial 2026 con visibilidad asegurada durante el torneo
- Desarrollar formatos de branded content nativo para patrocinadores que quieran ir más allá del logo en una sección
- Establecer un calendario de renovaciones con antelación suficiente para que comercial pueda negociar antes del fin de contrato

---

### Invendidos en programática

Porcentaje del inventario publicitario que no recibe ninguna puja y queda sin monetizar. Los invendidos generan coste de oportunidad y, si se rellenan con espacios en blanco, dañan la experiencia de usuario.

**Mejoras a corto plazo**
- Mapear qué slots, secciones y franjas horarias concentran más invendidos (el problema suele ser muy desigual)
- Configurar house ads o contenido propio (promoción de Fantasy MARCA, Radio MARCA) como fallback en los slots con mayor tasa de invendidos
- Revisar si los slots con más invendidos tienen problemas técnicos de configuración (tamaños no estándar, tiempos de respuesta altos)

**Mejoras a largo plazo**
- Reducir el número de slots en las páginas con mayor tasa de invendidos: menos inventario de menor calidad puede generar más ingresos que mucho inventario mal monetizado
- Explorar acuerdos de backfill con redes publicitarias de garantía (Google Ad Exchange como backfill de último nivel)
- Usar los invendidos como oportunidad de autopromoción medida: newsletters, suscripción MARCA+, app — con tracking para evaluar si generan valor equivalente al CPM de mercado

---

### RPM de sesión

Ingresos reales generados por cada mil sesiones. Es el KPI más honesto de monetización porque combina fill rate, CPM, páginas por sesión y viewability en un solo número. Si el CPM sube pero el fill rate cae, el RPM lo captura. Si mejora la recirculación, el RPM lo refleja.

Fórmula orientativa: (ingresos totales / sesiones totales) × 1000.

**Mejoras a corto plazo**
- Cruzar el RPM por sección: portada y noticias probablemente tienen RPM muy distinto. Actuar primero donde el gap es mayor
- Medir el impacto de cada cambio de publicidad en RPM, no solo en CPM o fill rate aislados
- Establecer una línea base mensual para detectar degradaciones rápido

**Mejoras a largo plazo**
- Usar el RPM como KPI de aprobación para cualquier cambio de publicidad: ningún formato nuevo se implementa sin proyección de impacto en RPM
- Segmentar el RPM por tipo de usuario (recurrente vs nuevo, logado vs anónimo) para priorizar inversión en los segmentos más rentables
- Construir el dashboard de RPM por sección, dispositivo y franja horaria como herramienta de decisión permanente

---

### Páginas por sesión (como KPI de monetización)

Cada página adicional por sesión multiplica directamente las impresiones disponibles y el RPM. En un sitio con media de 1,2-1,5 páginas por sesión, doblarla equivale a doblar el inventario sin aumentar usuarios.

**Mejoras a corto plazo**
- Auditar los módulos de recirculación actuales: qué CTR tienen, dónde están colocados, si están activos en todos los dispositivos
- Activar recirculación contextual al final de cada noticia (artículos relacionados por tema, no solo por fecha)
- Reducir la tasa de rebote en portada mejorando la presentación de los titulares y el acceso a contenido en un clic

**Mejoras a largo plazo**
- Rediseñar la experiencia de artículo para que invite a continuar leyendo (siguiente noticia automática, módulos de recirculación en mitad del texto, no solo al final)
- Construir secciones de destino con contenido agrupado (Mundial 2026, LaLiga en directo) que aumenten la profundidad de sesión de forma natural
- Implementar notificaciones push y newsletters segmentadas para traer de vuelta a usuarios que ya salieron

---

### Porcentaje de inventario addressable

Qué porcentaje de las impresiones tienen datos de usuario (1st party o 3rd party) que permiten targeting. En un sitio con mucho tráfico anónimo de portada, este porcentaje suele ser muy bajo, y es una causa directa de CPMs bajos en open auction. El inventario sin dato se vende a una fracción del precio del inventario targetizado.

**Mejoras a corto plazo**
- Medir qué porcentaje del tráfico actual está logado o tiene cualquier dato 1st party asociado
- Activar el registro en los productos que ya tienen base de usuarios: Fantasy MARCA, newsletters, Radio MARCA
- Configurar la pasarela de registro con fricción mínima (login con Google, sin formulario largo)

**Mejoras a largo plazo**
- Construir una estrategia de datos 1st party: qué datos se recogen, cómo se activan en el ad server, cómo se ofrecen a los compradores
- Crear incentivos de registro ligados a contenido o funcionalidades exclusivas (estadísticas avanzadas, alertas de resultados, Fantasy premium)
- Explorar la creación de segmentos de audiencia propios vendibles como deal ID (fans de clubes concretos, consumidores de vídeo, usuarios de alta frecuencia)

---

### Frecuencia media por usuario

Número de veces que un mismo usuario ve el mismo anuncio en una sesión o en un período de tiempo. Demasiada frecuencia quema el inventario: los compradores pagan menos por impresiones que ya vieron los mismos usuarios. Muy poca frecuencia puede indicar falta de demanda.

**Mejoras a corto plazo**
- Revisar si hay frequency capping configurado en el ad server y en qué límite está por defecto
- Comparar el CPM de las primeras impresiones por usuario vs las impresiones de alta frecuencia: el diferencial indica cuánto daño hace el exceso
- Ajustar los caps por formato: los formatos más intrusivos (interstitial, skin) necesitan caps más agresivos

**Mejoras a largo plazo**
- Establecer una política de frequency capping por defecto para todos los formatos, revisable trimestralmente
- Usar los datos de frecuencia para argumentar ante los anunciantes que el inventario de MARCA tiene alcance real, no solo impresiones repetidas
- Explorar modelos de compra por reach único en lugar de por impresiones para anunciantes de branding

---

### Ratio ingresos directos vs programática

Porcentaje de ingresos publicitarios que vienen de venta directa (patrocinios, campañas gestionadas) frente a programática (open auction, deals). Un ratio muy alto de programática expone los ingresos a fluctuaciones de mercado y temporalidades.

**Mejoras a corto plazo**
- Medir el ratio actual si no está documentado: es el punto de partida para cualquier decisión estratégica
- Identificar 3-5 anunciantes actuales de programática con gasto alto que podrían convertirse en acuerdos directos más estables
- Crear un paquete de venta directa específico para el Mundial 2026 con garantía de visibilidad

**Mejoras a largo plazo**
- Establecer un objetivo de ratio (por ejemplo, 30% directo / 70% programática) como meta estratégica del área de negocio
- Desarrollar un equipo o proceso de venta directa más activo para categorías con alto CPM (apuestas, automoción, banca)
- Construir productos publicitarios propios (branded content, newsletters patrocinadas, especiales editoriales) que no dependan de la programática

---

### Tasa de usuarios registrados / logados

Porcentaje de usuarios que acceden con una identidad conocida. Es la base del inventario addressable y del CPM premium. También es el punto de entrada a modelos de suscripción o freemium en el futuro.

**Mejoras a corto plazo**
- Medir la tasa actual de logins activos sobre el total de usuarios únicos mensuales
- Activar un CTA de registro contextual en los momentos de mayor intención (final de artículo largo, acceso a estadísticas, Fantasy MARCA)
- Simplificar el flujo de registro: login social (Google, Apple) como opción principal

**Mejoras a largo plazo**
- Construir una propuesta de valor clara para el usuario registrado: qué recibe a cambio de darse de alta
- Integrar los registros de todos los productos MARCA (Fantasy, newsletters, Radio) en un único perfil de usuario unificado
- Explorar un modelo freemium ligero: contenido premium o sin publicidad para usuarios registrados como incentivo

---

## KPIs de vídeo y plataforma OTT

MARCA tiene potencial de convertirse en una plataforma de vídeo deportivo (OTT o semi-OTT) con inventario propio de contenido original y cedido. Esta sección recoge los KPIs y las acciones necesarias para construir ese stock y monetizarlo.

---

### Stock total de vídeo

Número total de vídeos disponibles en el catálogo, diferenciando entre contenido original (producido por MARCA) y contenido cedido o sindicado (agencias, clubes, ligas, partners).

Es el KPI de base: sin stock suficiente no hay plataforma de vídeo.

**Mejoras a corto plazo**
- Auditar el catálogo actual: cuántos vídeos activos hay, qué antigüedad tienen, cuántos tienen views reales y cuántos están sin distribuir
- Activar acuerdos con agencias de contenido deportivo ya disponibles en el mercado (Reuters Sport, AP Sports, beIN Sports clips, Sportradar) para aumentar el stock de forma inmediata sin coste editorial
- Reutilizar el archivo propio: clips de entrevistas antiguas, resúmenes históricos, momentos icónicos de MARCA — con packaging editorial mínimo tienen valor de consumo

**Mejoras a largo plazo**
- Establecer acuerdos de sindicación con LaLiga, Real Madrid TV, Atlético de Madrid, selección española y federaciones nacionales
- Crear una línea de producción de contenido original corto (60-90 segundos) con formato fijo: dato del día, análisis exprés, predicción de partido
- Explorar acuerdos de co-producción con otros medios del grupo RCS para amortizar el coste de contenido original

---

### Tasa de crecimiento del catálogo

Número de vídeos nuevos añadidos por semana o por mes, separando originales y cedidos. Sin un ritmo de publicación constante, el catálogo envejece y la plataforma pierde recurrencia.

**Mejoras a corto plazo**
- Establecer un mínimo de publicación semanal por categoría (resultados, entrevistas, análisis) aunque sea con producción básica
- Definir responsabilidades editoriales claras: quién produce, quién edita, quién publica y en qué plazo desde el evento
- Crear plantillas de producción de vídeo corto que reduzcan el tiempo de edición a menos de 30 minutos por pieza

**Mejoras a largo plazo**
- Construir un calendario editorial de vídeo alineado con el calendario deportivo (pretemporada, LaLiga, Champions, Copa, Mundial 2026)
- Invertir en herramientas de edición automatizada (IA para highlights, subtitulación automática, clipping de partidos) para aumentar el volumen sin escalar el equipo
- Desarrollar una estrategia de contenido evergreen que no dependa del directo: rankings históricos, especiales de jugadores, documentales cortos

---

### Video views por vídeo (rendimiento de catálogo)

Vistas medias por vídeo publicado. Un catálogo grande con views bajas indica distribución deficiente o contenido poco relevante. Un catálogo pequeño con views altas indica que hay demanda pero falta stock.

**Mejoras a corto plazo**
- Identificar los 20 vídeos con más views del último mes: qué tienen en común (formato, duración, temática, momento de publicación)
- Revisar la distribución actual: los vídeos aparecen en la home, en las noticias relacionadas, en el hub de vídeo. ¿Están todos los puntos de entrada activos?
- Mejorar los thumbnails y títulos de los vídeos más estratégicos: en plataformas de vídeo el CTR del thumbnail es determinante

**Mejoras a largo plazo**
- Implementar recomendación algorítmica de vídeo basada en el comportamiento del usuario (qué vio antes, qué temática consume)
- Distribuir el contenido de vídeo en canales externos (YouTube, redes sociales) con link de vuelta a MARCA para aumentar el alcance sin canibalizar las views propias
- Crear series de vídeo con continuidad (formato episódico) que generen hábito de consumo y retorno

---

### Duración media de sesión de vídeo

Tiempo total que un usuario pasa consumiendo vídeo en una sola visita. Indica si los usuarios se quedan a ver más de un vídeo o si salen tras el primero. Es el equivalente al "binge watching" de una OTT.

**Mejoras a corto plazo**
- Activar autoplay del siguiente vídeo relacionado al terminar el que se está viendo
- Reducir la fricción entre vídeos: el reproductor no debe volver a la página de artículo entre vídeo y vídeo si el usuario está en el hub
- Construir listas de reproducción temáticas (todos los goles de Vinicius esta temporada, resúmenes de la jornada) que incentiven el consumo en cadena

**Mejoras a largo plazo**
- Construir un hub de vídeo con experiencia de navegación propia, separada del flujo de noticias, pensada para el consumo de vídeo continuo
- Desarrollar contenido de larga duración (20-45 minutos) para usuarios con alta intención de consumo: documentales, entrevistas en profundidad, especiales de competición
- Estudiar la viabilidad de una sección de vídeo en directo o semi-directo con contenido exclusivo (ruedas de prensa, entrenamientos abiertos, análisis post-partido)

---

### Tasa de retorno al hub de vídeo

Porcentaje de usuarios que vuelven al hub de vídeo en los 7 o 30 días siguientes a su primera visita. Es el indicador de si se está construyendo un hábito de consumo de vídeo en MARCA, clave para justificar la inversión en contenido original.

**Mejoras a corto plazo**
- Activar notificaciones push específicas para usuarios que ya han consumido vídeo: alertas de nuevo contenido de sus temáticas
- Crear una newsletter semanal de vídeo: los 5 mejores vídeos de la semana, con acceso directo al player
- Medir la tasa actual: sin línea base no se puede gestionar el KPI

**Mejoras a largo plazo**
- Lanzar una identidad de marca para el hub de vídeo de MARCA como destino específico, diferenciado del medio de noticias
- Explorar la creación de contenido exclusivo para el hub que no se distribuye en el resto del site (genera razón de visita)
- Evaluar si un modelo de acceso premium al catálogo de vídeo (MARCA+ o similar) tiene viabilidad dado el volumen y calidad del stock

---

### Coste por vídeo producido y ROI de contenido

Coste medio de producción por vídeo original frente a las views generadas. Permite identificar qué formatos tienen mejor retorno y dónde escalar la inversión.

**Mejoras a corto plazo**
- Documentar el coste real actual de producción de vídeo por tipo de pieza (sin este dato no hay decisión posible)
- Clasificar el catálogo en tres niveles de producción: básico (redactor + teléfono), medio (equipo + edición), premium (producción completa)
- Priorizar el nivel básico para aumentar volumen rápido y medir qué temáticas funcionan antes de invertir en producción mayor

**Mejoras a largo plazo**
- Establecer un umbral mínimo de views por vídeo para justificar el coste de cada nivel de producción
- Calcular el CPM equivalente del contenido original propio (ingresos publicitarios generados por ese vídeo / coste de producción) para compararlo con el coste de contenido cedido
- Usar el ROI por formato para construir el presupuesto de vídeo del año siguiente con criterio, no solo por intuición editorial

---

### Acuerdos de contenido cedido activos

Número de fuentes externas desde las que se recibe contenido de vídeo de forma recurrente (agencias, clubes, ligas, federaciones, otros medios). Cuantas más fuentes activas, más robusto es el stock frente a eventos imprevistos o limitaciones de producción propia.

**Mejoras a corto plazo**
- Mapear todos los acuerdos de contenido de vídeo activos: qué se recibe, con qué frecuencia, en qué condiciones de uso
- Identificar los gaps más obvios: si no hay acuerdo con ninguna agencia de noticias deportivas, es la primera prioridad
- Revisar si los acuerdos existentes se están aprovechando al 100% o hay contenido disponible que no se publica

**Mejoras a largo plazo**
- Negociar acuerdos de contenido con los clubes más seguidos por la audiencia de MARCA (Real Madrid, Barcelona, Atlético) — muchos tienen canales propios con material cedible
- Explorar acuerdos de reciprocidad con medios internacionales del grupo RCS (La Gazzetta dello Sport, Corriere della Sera) para intercambio de contenido deportivo
- Desarrollar un proceso estandarizado de ingesta, metadatado y publicación de contenido cedido que reduzca el tiempo entre recepción y publicación a menos de 2 horas

---

## Referencias

- Contexto de negocio: [context/work.md](work.md)
- Objetivos Q2 2026: [context/goals.md](goals.md)
- Publicidad y su impacto en métricas: [projects/publicidad/README.md](../projects/publicidad/README.md)
- Hub de vídeos: [projects/product-it/hub-videos/README.md](../projects/product-it/hub-videos/README.md)
- Integración automática de vídeo externo: [projects/product-it/integracion-video-externo/README.md](../projects/product-it/integracion-video-externo/README.md)
