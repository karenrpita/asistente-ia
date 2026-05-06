# Mundial 2026 — MARCA

**Descripción:** Cobertura editorial y producto digital del Mundial de Fútbol 2026. Portal con contenido editorial, datos deportivos en tiempo real, vídeo, patrocinios y publicidad programática en 4 ediciones.

**Estado:** Activo — en desarrollo
**Última actualización:** 2026-05-06
**Responsable de producto:** Karen Rodrigues Pita
**Confluence:** https://rcsuejira.atlassian.net/wiki/x/s36RAQ

---

## Contexto

Del 11 de junio al 19 de julio de 2026 se celebra el Mundial de Fútbol Masculino en EEUU, México y Canadá. El objetivo es tenerlo publicado el 1 de mayo de 2026. El proyecto abarca las 4 ediciones de MARCA, con especial foco en España, pero también México y USA (ambas versiones) por ser países organizadores.

Germán está trabajando en la Imagen Visual.

---

## Fechas clave

| Hito | Fecha |
|---|---|
| Publicación del portal/sección | 1 mayo 2026 |
| Pruebas Roba C (Lácer + aposteros) | 17 abril 2026 |
| Límite migraciones Xalok para el Mundial | 27 abril 2026 |
| Inicio del Mundial | 11 junio 2026 |
| Final del Mundial | 19 julio 2026 |

---

## Ediciones

El proyecto debe desplegarse en las 4 ediciones:
- España
- México
- USA — English
- USA — Español

Los patrocinios DFP cambiarán de una edición a otra (logo, enlaces y colores personalizados por edición).

**Nota ortográfica:** En México y USA-Español "America" y "video" no llevan tilde. En España, sí.

---

## Ámbito

- Web mobile
- Web desktop
- AMP
- Apps (muchas funcionalidades serán webview)

Todo será enlazable: títulos, cintillos, banderas, escudos, imágenes, nombres de selecciones, fechas, fases de grupos, eliminatorias…

---

## Componentes del producto

### Cuenta atrás (solo en Portada: mobile, desktop y APP)

- Con el logo del Mundial
- Se actualiza automáticamente con el tiempo restante para el inicio
- Patrocinado por DFP con geolocalización (distintos anunciantes según IP)
- Si se personaliza más allá del logo, geosegmentación en todo el bloque del widget
- En APP: el patrocinio iría directamente integrado ahí (si hay interés comercial)
- La carga del logo debe ser rápida (evitar problemas como con Luckia en el Mundial de Clubes)
- Enlace a la fase en la que están
- Se verán los Grupos + Selecciones con enlace a cada uno (48 selecciones = más grupos que en ediciones anteriores)
- Pendiente: tiempos de desarrollo para la personalización (para saber hasta cuándo puede venderlo Nacho)

Prototipo: https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=0%3A1&node-id=2031-77441

### Widget de portada y portadilla

Responsable: Franz Neuenschwander Barreto. Mobile, desktop y APP.

- Fecha y hora
- Indicador de directo visible
- Nombre completo + bandera en vertical; en desktop, mobile y apps la final se mostrará en horizontal (cambiar alto del widget en app). En desktop también semifinales en horizontal.
- Reducción del espacio del logo
- Rediseño completo del widget con opción de cuota de apuestas
- Ver posibilidad de widget con vídeo
- Patrocinio por DFP con geolocalización
- Pendiente: tiempos de desarrollo para la personalización

La diferencia entre portada y portadilla: en la portadilla no lleva la personalización con los enlaces (la portadilla en sí tendrá el enlazado).

Portada: https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=0%3A1&node-id=1-2
Portadilla: https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=0%3A1&node-id=153-8944

### Páginas de datos

Nuevo modelo de estructura a 1200px para que quepa el calendario del cuadro final. Posibilidad de tres columnas; en tablet, la columna izquierda se pone por encima del main content.

Incluir el include patrocinado por DFP. Publicidad ha encontrado problemas con estáticas (ej. Ceuta con calendario/clasificación), hay que revisarlo.

URLs de referencia:
- Resultados: https://www.marca.com/resultados/futbol/mundial.html
- Calendario: https://www.marca.com/futbol/mundial/calendario-interactivo.html
- Clasificación: https://www.marca.com/futbol/mundial/clasificacion.html
- Fase de grupos: https://www.marca.com/futbol/mundial/calendario/grupo-e.html
- Cuadro final: https://www.marca.com/futbol/mundial/calendario/octavos.html
- Estadísticas (Goles, Tarjetas, Asistencias, Pases, Paradas, Equipos): https://www.marca.com/futbol/mundial/goles.html

Prototipos páginas de datos:
- Mobile: https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=4268%3A77724&node-id=4268-78877
- Desktop: https://www.figma.com/proto/nY8C0HR7hViNTWGndEXKV5/MARCA---Mundial-2026?page-id=4275%3A93498&node-id=4281-113549

### Especiales NIT

Enlazados en menú/miga de desktop y mobile:

- Selecciones: https://www.marca.com/futbol/mundial/selecciones.html
- Convocados: https://www.marca.com/futbol/mundial/2022/11/17/63761ac4e2704e2a5c8b45e8.html
- Camisetas: https://www.marca.com/futbol/mundial/camisetas-qatar-2022.html
- Sedes y estadios: https://www.marca.com/futbol/mundial/sedes.html
- Historia de los Mundiales: https://www.marca.com/futbol/mundial/historia.html
- Palmarés: https://www.marca.com/futbol/mundial/palmares.html

### Sección Mundial

URL de referencia: https://www.marca.com/futbol/mundial.html

- Cabecera personalizada
- Incluye el widget de Portada
- Migas editables
- Todos los CTs de esa sección tendrán la misma cabecera personalizada
- Patrocinable por DFP
- Todos los elementos enlazables
- Posibilidad de geolocalizar el Flex de apertura para meter un streaming según IP (ya se preparó para Francia, ver MUNDIFUTBO-285)
- Navegación continua: no meter el widget en la home en navegación continua para poder incluir un include patrocinado. El widget sí irá en la portadilla. Como Betfair en Fútbol. Ese include sería como el de Lexus en Tenis, sin meter la personalización del Mundial.

### Bloque de noticias del Mundial en portada (IP USA — España y English)

- Bloque cerrado dedicado a noticias del Mundial
- Cabecera especial con logo y diseño diferente
- Migas enlazables y editables
- Formato include + logo — se mantiene para Diego
- Patrocinio por DFP de una noticia diaria en la home — para Nacho
- Habría que trabajar la guía con Ana para integrar más el patrocinio en la noticia

### Hub de vídeo patrocinado

- Patrocinio integrado en el Hub de Vídeo (logo monocromático que se adapte al HUB — UXUI)
- Canal de la portada de MARCA TV, que encaje en la versión mobile y no choque con el "Ver Todo"
- Skin en desktop: Roba A. Su versión mobile también incluida.
- Opción de patrocinio por DFP integrado

UI Hub de vídeo: https://www.figma.com/design/Ep7e1F7oOMIPa4aQPUBcyi/MARCA-Hub-de-v%C3%ADdeos-Final?node-id=6700-60001

Prototipos Hub de vídeo:
- Desktop: https://www.figma.com/design/PhZCjHl30EVzoQeXid6jMQ/MARCA-TV?node-id=1808-268722
- Mobile: https://www.figma.com/design/PhZCjHl30EVzoQeXid6jMQ/MARCA-TV?node-id=1808-185877
- App: https://www.figma.com/design/mRxBhx7dCYF4c72SOk0FpW/MARCA---App-2024---UX--Prototipo-?node-id=13590-149840

---

## Patrocinios y publicidad

Modelo mixto: patrocinadores directos + publicidad programática DFP en espacios restantes.

### Posiciones de patrocinio activas

| Espacio | Formato | Responsable comercial | Notas |
|---|---|---|---|
| Cuenta atrás portada | DFP con geolocalización | Nacho | Distintos anunciantes por IP |
| Widget de partidos | DFP con geolocalización | Nacho | En portada y portadilla |
| CTs relacionados con el Mundial | DFP debajo del Mega | — | Sin franja en mobile |
| Hub de vídeo | DFP integrado con logo monocromático | — | En canal portada MARCA TV |
| Marcadores de portada | DFP de un anunciante distinto al de temporada | Carmen (APP) | Con posibilidad de cuota de apuestas |
| Noticia patrocinada en home | DFP una noticia diaria | Nacho | Dentro y fuera de la noticia |
| Calculadora | — | — | Pendiente |
| Bloque include + logo en home | — | Diego | Formato include |

Guía de patrocinios: https://www.figma.com/proto/cBu00Z0QbJCtDEumdx3MzI/Marca---Patrocinio-creatividad--logo-e-include-2025

UI posiciones de patrocinio: https://www.figma.com/proto/cBu00Z0QbJCtDEumdx3MzI/Marca---Patrocinio-creatividad--logo-e-include-2025?page-id=0%3A1&node-id=134-44077

### Reglas de geolocalización

- Los patrocinios DFP cambiarán según IP: distintos anunciantes por edición y/o por región
- Puede haber patrocinadores distintos no solo por edición o IP, sino también dentro de la Edición España

### Patrocinadores actuales

| Patrocinador | Formato | Estado | IP |
|---|---|---|---|
| LG | Widget cuenta atrás | En validación | ES |
| Luckia | Widget de partidos | En validación | ES |
| Skechers | Power Ranking (logo integrado) | Mockup en preparación | ES |
| Lácer | Roba C | Pruebas 17 abril | ES |
| Aposteros (x2) | Roba C | Pruebas 17 abril | ES |

En edición España (IPs restantes): autopubli del Power Ranking.

---

## Power Ranking

Estadística propia de MARCA para evaluar el rendimiento de cada jugador por partido. El cálculo va en back-end (no en front) para proteger las ponderaciones y hacer el dato reutilizable en fichas de jugadores, páginas de estadísticas, etc.

Patrocinado por Skechers. Desarrollo casi terminado: front desktop y mobile cerrado (NIT), widget Top 5 para noticias listo.

URL de prueba: https://www.marca.com/multimedia/graficos/futbol/2026/powerranking_b/pruebaindex13absmin.html

### Fuente de datos y procesado

- Fuente: fichero F9 de OPTA (estadísticas por partido)
- Servicio de procesado: OPTA Transformer — http://10.24.65.12/UESportResults/ueOPTATransformer
- El cálculo se actualiza durante el partido y hasta 2 días después de su finalización, conforme OPTA atribuye estadísticas a cada jugador
- Los torneos en los que se calcula y almacena el Power Ranking se limitan por configuración
- Una vez finalizado el encuentro, además del dato por partido se calcula la puntuación acumulada del jugador en el torneo
- Ambos valores (por evento y acumulado) se añaden al APIRD en documentos de MongoDB

### Fórmula de cálculo (4 fases)

**1. RAW SCORE**
Se multiplican los stats estadísticos por los factores de la tabla de pesos según la demarcación del jugador (portero, defensa, medio, delantero). El valor bruto resultante se promedia con todos los valores alcanzados y se multiplica por un factor corrector. Se suman los puntos de base del jugador por participar en el partido.

**2. BONUS**
El Raw Score se bonifica por conceptos clave: goles, asistencias de gol y resultado favorable del partido.

**3. MALUS**
Al Raw Score + Bonus se aplican penalizaciones por conceptos perjudiciales: tarjetas rojas, penalties cometidos o fallados, derrota en el encuentro.

**4. TECHO Y SUELO**
La puntuación final no puede superar 10 ni bajar de 3.

### Endpoints de acceso

Dato por partido (full event):
```
https://api.unidadeditorial.es/sports/v1/events/01_0101_20260503_176_954/full?site=2
```

Stats por partido:
```
https://api.unidadeditorial.es/sports/v1/event-stats/event/01_0101_20260503_176_954?site=2
```

Power Ranking acumulado por equipo:
```
http://shr-apird-private-api.pro.int.gcp.web.uelan.es:20626/sports/v1/competitor-season-stats/sport/01/competitor/186/tournament/0101?site=2
```

Clasificación general por Power Ranking (paginada, orden asc/desc):
```
https://api.unidadeditorial.es/sports/v1/power-ranking/sport/01/tournament/0101/season/2025?site=2
```

### Datos por jugador

- Nombre corto y largo (ej. Mbappé / Kylian Mbappé)
- ID del jugador
- URL imagen del jugador
- Selección/país (nombre corto y largo): ESP / España
- URL bandera del país
- Equipo (nombre corto y largo): RMA / Real Madrid
- Posición general: Portero / Defensa / Centrocampista / Delantero
- Posición específica: lateral derecho, mediocentro, extremo, etc.
- Minutos jugados
- Titular: sí / no
- Edad o fecha de nacimiento
- Altura
- Peso

### Datos por jugador y partido

Todos los atributos estadísticos de la tabla de pesos + seis nuevos con su valor numérico.

### Tabla de pesos por posición

| Stat | Portero | Lateral | Central | CDM | CAM | Extremo | Delantero |
|---|---|---|---|---|---|---|---|
| Goals | 0 | 0.05 | 0.05 | 0.05 | 0.10 | 0.15 | 0.30 |
| Goals (outside box) | 0 | 0 | 0 | 0.01 | 0.02 | 0.03 | 0.05 |
| Goals (penalties) | 0 | 0 | 0 | 0 | 0.01 | 0.02 | 0.05 |
| Assists | 0 | 0.05 | 0.02 | 0.05 | 0.20 | 0.15 | 0.10 |
| Penalties Saved | 0.15 | 0 | 0 | 0 | 0 | 0 | 0 |
| Clean Sheets | 0.25 | 0.15 | 0.20 | 0.05 | 0 | 0 | 0 |
| Games Won | 0.05 | 0.05 | 0.05 | 0.05 | 0.05 | 0.05 | 0.05 |
| Shots on Target | 0 | 0 | 0 | 0.02 | 0.05 | 0.10 | 0.15 |
| Saves | 0.30 | 0 | 0 | 0 | 0 | 0 | 0 |
| Interceptions | 0.05 | 0.10 | 0.15 | 0.15 | 0.05 | 0 | 0 |
| Tackles | 0.05 | 0.10 | 0.15 | 0.10 | 0.05 | 0.03 | 0 |
| Blocks | 0.05 | 0.10 | 0.15 | 0.05 | 0 | 0 | 0 |
| Clearances | 0.05 | 0.10 | 0.20 | 0.05 | 0 | 0 | 0 |
| Duels Won | 0.05 | 0.10 | 0.15 | 0.10 | 0.05 | 0.05 | 0.05 |
| Dribbles Completed | 0 | 0.03 | 0.01 | 0.02 | 0.10 | 0.15 | 0.10 |
| Crosses/Corners Successful | 0 | 0.10 | 0 | 0.05 | 0.05 | 0.10 | 0 |
| Aerial Won | 0.05 | 0.10 | 0.15 | 0.10 | 0 | 0 | 0 |
| Passes Successful | 0.05 | 0.10 | 0.10 | 0.10 | 0.10 | 0.05 | 0.05 |
| Possession Won | 0.05 | 0.10 | 0.10 | 0.10 | 0.05 | 0 | 0 |
| Touches | 0.05 | 0.05 | 0.05 | 0.05 | 0.05 | 0.05 | 0.05 |
| Catches | 0.10 | 0 | 0 | 0 | 0 | 0 | 0 |
| Possession Lost | -0.05 | -0.05 | -0.05 | -0.05 | -0.10 | -0.10 | -0.10 |
| Yellow Cards | -0.05 | -0.05 | -0.05 | -0.05 | -0.05 | -0.05 | -0.05 |
| Goals Conceded | -0.20 | -0.10 | -0.10 | -0.05 | 0 | 0 | 0 |
| Games Lost | -0.05 | -0.05 | -0.05 | -0.05 | -0.05 | -0.05 | -0.05 |
| Penalty Miss | 0 | 0 | 0 | 0 | -0.05 | -0.05 | -0.10 |
| Penalty Conceded | -0.10 | -0.05 | -0.05 | -0.05 | 0 | 0 | 0 |
| 2nd Yellow Cards | -0.10 | -0.10 | -0.10 | -0.10 | -0.10 | -0.10 | -0.10 |
| Own Goals | -0.15 | -0.10 | -0.10 | -0.10 | -0.05 | -0.05 | -0.05 |
| Red Cards | -0.20 | -0.20 | -0.20 | -0.20 | -0.20 | -0.20 | -0.20 |

Stats eliminados (no disponibles):
- Chances Created, Saving Catches, Keeper Sweeper Accuracy, Big Chance Missed, Errors Leading to Goals

Stats nuevos por incluir (sin peso definido aún):
- Total Fouls Conceded, Key Passes, GK Successful Distribution, Penalty Saved, Total Fouls Won, Winning Goal

### Datos por partido

- Equipo local
- Equipo visitante
- Campo localVsVisitante (ej. España - Francia)
- Fecha (YYYY-MM-DD)
- Hora (HH:MM)
- Estado del partido (Finalizado / En juego / Aplazado…)

### Actualización y rendimiento

Estaticar datos para evitar sobrecarga. La estatificación se refresca durante y después de los partidos (hasta ~30 minutos después o hasta que no haya nuevos datos). El Power Ranking por partido se calcula aplicando los pesos por posición del jugador. Se quiere también: media de la competición por jugador y por partido, y sumatorio por jugador en la competición.

---

## Fans United

Proveedor externo que aportaría funcionalidades diferenciales de interacción con el usuario:
- Vinculado al Mundial
- Widget dentro de los contenidos
- Incluye registro
- Fans United entrega todo hecho

Se está haciendo una prueba con un partido de la Champions. Si funciona, se hace un GNP separado para el desarrollo de Fans United.

---

## Peticiones SEO

- Mejorar los datos estructurados de los especiales
- Dividir artículos a nivel editorial para aprovechar en Discover
- En mobile: el desplegable de cambio de fase como enlace href en el HTML (actualmente es un desplegable con JSON, como en Qatar 2022)
- Ver si cada fase final puede arrastrarse como widget a portada para dar autoridad desde la home a la estática
- SEO hará otro GNP con peticiones adicionales

Ticket Analítica: https://rcsuejira.atlassian.net/servicedesk/customer/portal/1/ANALITISD-2581

---

## Requisitos en GNP

Pendiente meter los siguientes requisitos:

- Geobloqueo del Flex con streaming (solo visible por IP)
- GolStats: confirmar si la prueba funcionó y si se incluye el servicio dentro del proyecto
- Dizplai u otro: confirmar si necesita integración técnica
- Calendario: unificar el interactivo y el de OPTA

Items comerciales para GNP:
- Noticia patrocinada (dentro y fuera)
- Widget con enlaces a páginas + cuotas de apuestas (Codere o Luckia) + lógica de horarios según IP
- Cuenta atrás
- Marcadores
- Include
- Calculadora

---

## Pendientes de definir

- Puede haber patrocinadores distintos no solo por edición/IP, sino también dentro de la Edición España
- Pedir informe de Analítica como el de Qatar 2022: MARCA - Informe Final Mundial Qatar 2022
- Logo del Mundial: sin confirmar
- UI del widget: pendiente
- UI posiciones de patrocinio: a falta de un pequeño ajuste de color
- Tiempos de desarrollo para personalización de cuenta atrás y widget (para Nacho)
- En APP: si hay interés comercial en el patrocinio, habría que hacerlo directamente en la APP

---

## Stack tecnológico

- CMS: Xalok
- Publicidad: DFP (Google Ad Manager) + publicidad programática
- Datos deportivos: API en tiempo real (OPTA + datos propios)
- Power Ranking: cálculo en back-end, dato consumible desde múltiples secciones

---

## KPIs asociados

| Métrica | Impacto esperado |
|---|---|
| Usuarios | Alto — evento de captación masiva |
| Páginas vistas | Alto — cobertura en vivo, resultados, especiales |
| Video views | Medio-alto — vídeos de goles, resúmenes, highlights |

---

## Equipos implicados

| Equipo / Persona | Rol en el proyecto |
|---|---|
| Karen Rodrigues Pita | Head of Product — responsable del producto |
| Javier Rodriguez Diez | Product Manager — coordinación |
| Luis Fernando Tapia Vaca | — |
| Nacho Delgado | Comercial — venta de patrocinios |
| Franz Neuenschwander Barreto | Producto — widget de portada/portadilla |
| Germán | Imagen Visual |
| Jose Antonio Aguilera | Tecnología |
| Carmen | APPs |
| Diego | Bloque de noticias patrocinadas en home |
| Ana | Guía de integración de patrocinio en noticia |
| Belen Gomez | Project Manager (IT) |
| Publicidad | Patrocinios y formatos |
| Analítica | Informe de seguimiento |
| SEO | Optimización de especiales |
| UX/UI | Prototipos y diseño |
| QA | Validación |
| Marketing | — |

---

## Dependencias

| Dependencia | Impacto | Estado |
|---|---|---|
| Migraciones Xalok (deadline 27 abril) | Si no llegan a tiempo, puede ser necesario rehacer widgets para UEdit | Crítico |
| Logo del Mundial | Bloqueante para cuenta atrás y widget | Sin confirmar |
| App — widgets del Mundial | Inicio de desarrollo pendiente | Bloqueado |
| GolStats | Si se integra, requiere GNP | Pendiente confirmar |
| Fans United | Prueba en Champions, GNP separado si se confirma | En evaluación |
