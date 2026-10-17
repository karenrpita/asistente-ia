# GNP - Mundial Femenino 2027 (Brasil)

## 1. Identificación de la necesidad

- **Evento de captación con España como vigente campeona:** España ganó el Mundial Femenino 2023. El Mundial de Brasil 2027 (24 de junio - 25 de julio de 2027, 32 selecciones y 64 partidos en 8 sedes, según el calendario oficial publicado por FIFA) concentrará el interés de la audiencia española durante cinco semanas. Sin un producto específico, ese tráfico se queda en la competencia. KPI afectado: usuarios y páginas vistas.
- **Audiencia femenina y joven por debajo de objetivo:** el plan estratégico de MARCA (Frente 4, context/marca.md) fija abrir audiencia femenina y subir afinidad 16-34. El fútbol femenino es la vía más directa dentro del core de MARCA. KPI afectado: usuarios.
- **Vídeo sin un evento que lo empuje en verano 2027:** goles, resúmenes y highlights de la selección son el contenido de vídeo con más demanda en un torneo. KPI afectado: video views.
- **Riesgo de negocio:** en el Mundial 2026 el inventario de patrocinio (cuenta atrás, widget de partidos, marcadores, noticia patrocinada) se vendió con geolocalización por IP. Si los componentes no están listos con tiempo, Comercial no puede venderlos y se pierde el ingreso del evento. Riesgo de experiencia: un exceso de formatos degrada la navegación, principal queja actual de los usuarios.

## 2. Objetivo

- **Producto del Mundial publicado antes del arranque:** sección, portadilla, páginas de datos y especiales operativos con margen para posicionar en SEO y Discover, con el mismo esquema que el Mundial 2026. Responde a la necesidad 1.
- **Captar y retener audiencia femenina y joven:** contenido, datos y vídeo de la selección femenina con recirculación hacia el resto de MARCA. Medible con usuarios únicos de la sección y afinidad por género y edad (GfK) frente a la media de MARCA. Responde a la necesidad 2.
- **Aumentar video views durante el torneo:** integrar el Mundial en el Hub de Vídeos con canal propio y vídeo en el widget si es viable. Responde a la necesidad 3.
- **Paquete de patrocinio listo para vender y sin degradar la experiencia:** widget de resultados, carrusel de portada, cuenta atrás y resto de posiciones patrocinables por DFP con geolocalización, con tiempos de desarrollo cerrados para Comercial. Ningún formato puede hacer caer usuarios, páginas vistas ni video views. Responde al riesgo.
- **Frenos conocidos:**
  - **Datos deportivos:** la Central de Datos sitúa el fútbol femenino como expansión pendiente. Hay que confirmar que OPTA y APIRD dan cobertura completa del Mundial Femenino (resultados en vivo, alineaciones, estadísticas F9). Sin eso no hay widget, carrusel ni páginas de datos. Se sortea validando la cobertura antes de comprometer componentes.
  - **CMS:** las ediciones internacionales siguen en UEdit hasta completar la migración a Xalok. En el Mundial 2026 se fijó una fecha límite de migraciones para no tener que rehacer widgets. Se aplica el mismo criterio.
  - **Widgets de APP:** en el Mundial 2026 su desarrollo quedó bloqueado. Si no hay desarrollo nativo a tiempo, las funcionalidades de APP van por webview.
  - **Rendimiento de patrocinios:** carga lenta del logo patrocinado (caso Luckia en el Mundial de Clubes) y problemas de Publicidad con estáticas de datos (calendario y clasificación). Se exige carga rápida y revisión previa con Publicidad.

## 3. Descripción

El proyecto replica el modelo del Mundial 2026 adaptado a una competición de 32 selecciones y a la sede en Brasil (UTC-3, partidos en tarde y noche en España). Se divide en 4 fases:

- **Fase 1 - Definición y validación de datos:** cobertura de datos, componentes por edición, inventario comercial y calendario.
- **Fase 2 - Diseño:** imagen visual y adaptación de los prototipos del Mundial 2026.
- **Fase 3 - Desarrollo e integración:** componentes de portada, sección, datos, especiales, vídeo y patrocinio en web y APP.
- **Fase 4 - Operación durante el torneo y cierre:** seguimiento en directo, ajustes e informe final.

### 3.1. Fase 1 - Definición y validación de datos

- **Qué se hace y con qué criterio:** validar con IT y Datos Deportivos que OPTA y APIRD cubren el Mundial Femenino 2027: calendario, resultados en vivo, alineaciones, estadísticas por partido y jugadora, y fichero F9 para el Power Ranking. Definir la adaptación de cada componente a las 4 ediciones (España, México, USA English y USA Español), incluidos horarios y ortografía por edición (en México y USA Español "America" y "video" sin tilde). Cerrar con Comercial qué posiciones se venden y por qué IP. Fijar la fecha límite de entrega para que Comercial pueda vender, como se pidió en el Mundial 2026.
- **Tecnologías y superficies:** APIRD, feeds OPTA, Xalok y UEdit, DFP.
- **Calendario:** 4T 2026 - enero 2027.
- **Resultado:** matriz de componentes por edición y superficie, inventario comercial cerrado, calendario de entregas y GNP sin pendientes de definición interna.

### 3.2. Fase 2 - Diseño

- **Qué se hace y con qué criterio:** imagen visual propia del Mundial Femenino, con logo y colores. Partir de los Figma del Mundial 2026 para no rediseñar desde cero: cuenta atrás, widget de portada y portadilla, páginas de datos a 1200px, sección y posiciones de patrocinio. Adaptar el cuadro final a 32 selecciones y 8 grupos. Incluir logo patrocinado monocromático en el Hub de Vídeos.
- **Tecnologías y superficies:** Figma. Web desktop y mobile, APP.
- **Calendario:** febrero - marzo 2027.
- **Resultado:** prototipos validados de cada componente en mobile, desktop y APP, y guía de patrocinio aplicada.

### 3.3. Fase 3 - Desarrollo e integración

- **Qué se hace y con qué criterio:**
  - **Cuenta atrás en portada:** se actualiza sola, enlaza a la fase en curso y a grupos y selecciones, patrocinio DFP con geolocalización.
  - **Widget de resultados (portada y portadilla):** fecha, hora, indicador de directo, selección con bandera, partidos destacados (final y semifinales en horizontal), opción de cuota de apuestas y patrocinio DFP con geolocalización. Portadilla sin la personalización de enlaces.
  - **Carrusel de resultados en portada:** marcadores del día enlazados a cada partido y patrocinables por un anunciante distinto al de temporada. Se reutiliza el componente de marcadores del Mundial 2026.
  - **Sección Mundial Femenino:** cabecera personalizada, migas editables, widget de portada, todos los elementos enlazables, patrocinable por DFP, flex de apertura geolocalizable para streaming.
  - **Páginas de datos:** resultados, calendario (unificado entre el interactivo y el de OPTA), clasificación por grupos, cuadro final y estadísticas (goles, tarjetas, asistencias, paradas), con include patrocinado.
  - **Especiales NIT:** selecciones, convocatorias, sedes y estadios, historia del Mundial Femenino y palmarés, enlazados desde menú y miga.
  - **Vídeo:** canal del Mundial Femenino en el Hub de Vídeos y en la portada de MARCA TV, con patrocinio integrado. Valorar vídeo dentro del widget.
  - **Patrocinio:** noticia patrocinada diaria en home (dentro y fuera de la noticia), bloque include + logo, posiciones del widget, cuenta atrás y marcadores. Geolocalización por edición e IP, incluidos varios patrocinadores dentro de la edición España.
  - **Power Ranking:** se incluye. Reutiliza el cálculo en back-end del Mundial 2026 con datos F9 de OPTA. Hay que validar la tabla de pesos para fútbol femenino. El front se hará previsiblemente desde NIT, como en el Mundial 2026.
  - **SEO:** datos estructurados en especiales, desplegable de fases como enlace href en el HTML, fases finales arrastrables a portada.
  - **Analítica:** marcado de todos los componentes y posiciones patrocinadas.
- **Tecnologías y superficies:** Xalok (y UEdit en las ediciones no migradas), APIRD y OPTA, DFP, Hub de Vídeos, web desktop y mobile, AMP, APP iOS y Android (webview donde no haya nativo).
- **Calendario:** abril - mayo 2027. Publicación objetivo en la primera quincena de mayo de 2027, con el mismo margen que el Mundial 2026 (publicado seis semanas antes del inicio).
- **Resultado:** URL de sección bajo /futbol/ (estructura a validar con SEO), portadilla, páginas de datos, especiales NIT, componentes de portada y posiciones de patrocinio en producción.

### 3.4. Fase 4 - Operación durante el torneo y cierre

- **Qué se hace y con qué criterio:** seguimiento diario de rendimiento técnico (carga de widgets y logos, estatificación de datos en directo) y de KPIs. Ajustes rápidos en portada según el avance de España. Informe final de Analítica como los de Qatar 2022 y Mundial 2026, comparando con el Mundial Femenino 2023.
- **Tecnologías y superficies:** todas las anteriores. Herramientas de analítica.
- **Calendario:** 24 de junio - finales de agosto de 2027. Inauguración el 24 de junio (Brasil, Maracaná) y final el 25 de julio de 2027 en el Maracaná.
- **Resultado:** informe final de impacto en usuarios, páginas vistas, video views e ingresos de patrocinio.

## 4. Ámbito (Web, Apps, Mobile...)

- **CMS:** Xalok en la edición España. En las ediciones internacionales, UEdit o Xalok según el estado de la migración en esa fecha.
- **Web desktop:** sección, portadilla, cuenta atrás, widget, carrusel de portada, páginas de datos a 1200px, especiales y patrocinios.
- **Web mobile:** los mismos componentes adaptados. Sin franja de patrocinio debajo del Mega.
- **AMP:** noticias del Mundial con enlazado a la sección y a las páginas de datos.
- **App iOS:** widget y carrusel de resultados, sección y patrocinio integrado. Webview donde no haya desarrollo nativo. Se coordina con el proyecto de widget de resultados en vivo (Live Activities).
- **App Android:** igual que iOS. Coordinación con Now bar.
- **Ediciones:** las 4 ediciones: España, México, USA English y USA Español. Los patrocinios DFP cambian por edición (logo, enlaces y colores).
- **Newsletters:** sin desarrollo. Se puede usar contenido del Mundial en las existentes.
- **Notificaciones push:** sin desarrollo. Uso editorial de las existentes en partidos de España y fases finales.
- **Feeds y sitemaps:** inclusión de la sección, las páginas de datos y los especiales.
- **Publicidad:** DFP con geolocalización en cuenta atrás, widget, carrusel y marcadores, noticia patrocinada, include + logo, Hub de Vídeos y CTs del Mundial. Programática en el resto.
- **Analítica:** marcado de componentes, posiciones patrocinadas y cuadro de mando del evento.
- **Fuera de ámbito:** integraciones de terceros nuevas (Fans United, GolStats, Dizplai), que llevarían GNP propio, y desarrollos nuevos de newsletters o push.

## 5. Alcance / requisitos

- **Volumen:** 32 selecciones, 8 grupos, 64 partidos y 8 sedes: Belo Horizonte, Brasilia, Fortaleza, Porto Alegre, Recife, Río de Janeiro, Salvador y São Paulo (todas con estadios del Mundial 2014). Componentes: cuenta atrás, widget de portada y portadilla, carrusel de resultados, sección, 5 páginas de datos, 5 especiales NIT, canal en Hub de Vídeos, Power Ranking y paquete de patrocinio. Despliegue en 4 ediciones.
- **Criterios de calidad:** todo enlazable (títulos, cintillos, banderas, nombres de selección, fechas, fases). Datos en directo estatificados y refrescados durante y hasta unos 30 minutos después de cada partido. Logos patrocinados con carga rápida.
- **Requisitos técnicos:** reutilizar los componentes del Mundial 2026 parametrizados por competición, sin desarrollar componentes nuevos. Horarios mostrados según la zona horaria de cada edición.
- **Requisitos SEO:** sección y especiales publicados con antelación para posicionar, datos estructurados en especiales, fases como enlaces href, artículos divididos para Discover.
- **Requisitos analíticos:** eventos en widget, carrusel, cuenta atrás y posiciones patrocinadas. Informe final comparable con el Mundial Femenino 2023 y el Mundial 2026.
- **Requisitos de negocio:** inventario patrocinable con geolocalización por edición e IP. Tiempos de desarrollo de la personalización comunicados a Comercial antes de la venta. Ningún formato puede hacer caer usuarios, páginas vistas ni video views.

## 6. Aspectos pendientes de definir

- **Cobertura de datos OPTA y APIRD:** Falta: confirmar que hay datos en vivo y estadísticas del torneo. Por qué no se cierra aún: depende del contrato y del proveedor. Decide: IT y Datos Deportivos (Belen Gomez).
- **Logo e imagen oficial del torneo:** Falta: identidad oficial de FIFA. Por qué no se cierra aún: depende de su publicación. Bloquea la cuenta atrás y el widget. Decide: Diseño (Germán), cuando FIFA la publique.
- **Inventario comercial y patrocinadores:** Falta: posiciones a vender y anunciantes por IP. Por qué no se cierra aún: depende de la venta. Decide: Comercial (Nacho Arcos).
- **Tabla de pesos del Power Ranking:** Falta: validar si los pesos por posición del Mundial 2026 sirven para fútbol femenino. Por qué no se cierra aún: depende de la cobertura F9 de OPTA del torneo. Decide: Producto, Datos Deportivos y NIT.

## 7. Ejemplos / prototipos

- **Mundial 2026 MARCA:** [README del proyecto](../mundial-2026/README.md) - Base funcional, técnica y comercial de este GNP.
- **Confluence Mundial 2026:** https://rcsuejira.atlassian.net/wiki/x/s36RAQ - Documentación completa del proyecto de referencia.
- **Prototipo cuenta atrás:** https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=0%3A1&node-id=2031-77441 - Base para la cuenta atrás.
- **Prototipo widget de portada:** https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=0%3A1&node-id=1-2 - Base para el widget y el carrusel de portada.
- **Prototipo portadilla:** https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=0%3A1&node-id=153-8944 - Base para la portadilla.
- **Páginas de datos mobile:** https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=4268%3A77724&node-id=4268-78877 - Estructura de resultados, calendario y clasificación.
- **Páginas de datos desktop:** https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=4275%3A93498&node-id=4281-113549 - Modelo a 1200px con cuadro final.
- **Guía de patrocinios:** https://www.figma.com/proto/cBu00Z0QbJCtDEumdx3MzI/Marca---Patrocinio-creatividad--logo-e-include-2025 - Formatos de logo e include.
- **Hub de Vídeos UI:** https://www.figma.com/design/Ep7e1F7oOMIPa4aQPUBcyi/MARCA-Hub-de-v%C3%ADdeos-Final?node-id=6700-60001 - Integración del patrocinio en el canal del Mundial.
- **Sección Mundial actual:** https://www.marca.com/futbol/mundial.html - Referencia de cabecera, migas y estructura de sección.

## 8. Equipos implicados

- **SEO:** estructura de URLs, datos estructurados, enlazado de fases y estrategia Discover - responsable: Damián Santiago y Gonzalo.
- **IT/Desarrollo:** componentes, integración de datos, estatificación y despliegue por edición - responsable: Belen Gomez (PM IT), Jose Antonio Aguilera (Tecnología).
- **Producto:** definición, priorización, coordinación y GNP - responsable: Karen Rodrigues Pita, con Javier Rodriguez Diez en la coordinación y Franz Neuenschwander Barreto en el widget de portada y portadilla.
- **Diseño/UX:** imagen visual y adaptación de prototipos - responsable: Germán (imagen visual), equipo UX/UI.
- **Contenido/Editorial:** cobertura, especiales NIT, convocatorias, vídeo y noticias patrocinadas. Interlocutor para todo lo editorial del proyecto - responsable: Emilio (responsable editorial).
- **Analítica:** marcado, seguimiento y informe final - responsable: Jorge Alia.
- **Audiencias/Redes:** distribución en redes y vertical con vuelta a MARCA, foco en audiencia femenina y 16-34 - responsable: Alberto Benítez.
- **Publicidad/Comercial:** venta de patrocinios, definición del producto publicitario y revisión de formatos en estáticas - responsable: Nacho Arcos (venta de patrocinios), Carmen (producto publicitario), Diego (include + logo), Ana (guía de integración en noticia).
- **Marketing/Newsletters:** promoción del especial y uso en newsletters existentes - responsable: por confirmar.
- **QA:** validación de componentes, geolocalización de patrocinios y datos en directo - responsable: departamento de QA.
