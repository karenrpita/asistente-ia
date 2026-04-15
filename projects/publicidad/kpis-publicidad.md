# KPIs de Publicidad — MARCA

Actualizado: 2026-04-15

KPIs específicos del área publicitaria. Se evalúan de forma complementaria a los KPIs principales — una mejora en publicidad que dañe usuarios o páginas vistas es un resultado negativo.

---

## Viewability

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

## Completion rate en vídeo

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

## Inventario de vídeo

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

## Fill rate programático

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

## CPM medio

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

## Patrocinios

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

## Invendidos en programática

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

## RPM de sesión

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

## Páginas por sesión (como KPI de monetización)

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

## Porcentaje de inventario addressable

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

## Frecuencia media por usuario

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

## Ratio ingresos directos vs programática

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

## Tasa de usuarios registrados / logados

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

## Referencias

- KPIs principales de negocio: [context/kpis-negocio.md](../../context/kpis-negocio.md)
- Contexto general de publicidad: [README.md](README.md)
