---
tags: [#area/trabajo, #tema/marca, #tema/seo, #tema/negocio, #tema/estrategia]
created: 2026-04-13
updated: 2026-10-17
---

# MARCA — Business Strategy

> [!abstract] En una línea
> MARCA gana en fidelidad y pierde en alcance. Lidera páginas vistas, sesiones por usuario y rebote, pero es **3º en usuarios únicos de GfK** (12,16 M en agosto de 2026, frente a 15,31 M de AS). La estrategia se ordena por un solo objetivo: **captar usuarios nuevos, sobre todo en móvil, y monetizar mejor la fidelidad que ya tenemos.**

## Índice

1. [[#1. Contexto]]
2. [[#2. KPIs — el marcador]]
3. [[#3. Cómo atacarlo]]
4. [[#4. Playbook por KPI]]
5. [[#5. Anexo — contexto operativo]]

---

## 1. Contexto

**MARCA** es el principal medio deportivo de España, de **Unidad Editorial**. Cubre también entretenimiento y salud, opera subdominios de apuestas y entradas, y tiene ediciones en España, México y USA (inglés y español). ~200 empleados en MARCA, ~1.200 en Unidad Editorial. Competidores: **AS, Mundo Deportivo, Sport**.

**Cómo se mide el negocio.** GfK (España) y Comscore (México) son los medidores oficiales: con ellos Dirección reporta y Publicidad vende campañas y mide cuota. SEO opera con GSC como fuente de verdad, pero el marcador que importa es GfK.

**El diagnóstico, con datos (GfK agosto 2026, vertical deportivo web):**

| | MARCA | AS | Mundo Deportivo |
|---|---|---|---|
| Usuarios únicos | **12,16 M (3º)** | 15,31 M | 12,47 M |
| UU mobile | **10,90 M** | 14,21 M | 11,7 M |
| Páginas vistas | **921 M** (1,8× AS) | 517 M | 235 M |
| Sesiones por usuario | **31** | 13 | 8 |
| Rebote | **36%** | 53% | 56% |

- **El problema es el alcance, no la fidelidad.** Todo el hueco con AS está en móvil; en desktop MARCA lidera y en la app arrasa (1,51 M frente a 0,5 M).
- **AS también nos gana en deportivo.** En el Mundial (julio de 2026), el mayor pico deportivo del año, AS creció +13,0% y MARCA +9,8%: la distancia pasó de −1,8 M a −2,5 M, y en agosto a −3,1 M. La explicación de "AS gana por el contenido no deportivo" ya no basta.
- **Mundo Deportivo crece todos los meses** y en agosto adelanta a MARCA, que cae a 3º en 9 de 17 CCAA.
- **El 57% de la distancia con AS está en cuatro CCAA:** Cataluña (−638 mil), Madrid (−508 mil), C. Valenciana (−364 mil) y Andalucía (−267 mil). Cataluña, C. Valenciana y Murcia están por debajo de la media de penetración de forma estructural, lo que encaja con la **imagen promadridista y poco plural** de la marca.
- **MARCA no llega a los jóvenes:** índice de afinidad de 55-71 en 16-24 años y de 74-108 en 25-34. No hay dato por género.
- **La mayor caída de SEO de su historia** empezó el **7 de julio de 2025** (−80% en Discover) y sigue sin causa identificada. Ver [[muvera]].

**Restricciones con las que hay que jugar:**
- **Redacción como cuello de botella:** frena la adopción de estrategias SEO y no propone proyectos. Las vías de crecimiento no deben depender de ella.
- **Deuda técnica y opacidad de infraestructura:** desarrollo lento, poca autonomía y sin visibilidad de si se bloquea algo a Google.
- **Decisiones sin datos ni medición:** CMP rediseñado sin UX, redirección por IP en portada sin medir, sin dashboard unificado de KPIs.
- **Monetización desconectada de la audiencia:** CPMs bajos atribuidos a "inventario de baja calidad".
- **Bloqueo corporativo de bots de IA:** si incluye `Google-Extended`, MARCA puede quedar fuera de AI Overviews.
- **Deportistas** que ya no necesitan a los medios, y web con imagen envejecida frente a apps de resultados, plataformas audiovisuales y redes.

---

## 2. KPIs — el marcador

> **Regla de decisión.** Ninguna acción se aprueba sin responder: _¿sube, baja o es neutra en usuarios, páginas vistas y video views, **y en el consumo por usuario** (páginas vistas, video views y permanencia por usuario)?_ Una mejora de ingresos que baje usuarios o páginas vistas puede ser negativa para el negocio. El análisis es siempre conjunto.

### North Star: usuarios únicos GfK

Es el único KPI oficial en el que MARCA no lidera, y el que usan Dirección y Publicidad.

| | Hoy (ago. 2026) | Objetivo propuesto |
|---|---|---|
| UU GfK MARCA | 12,16 M · 3º | **Corto plazo:** recuperar el 2º puesto (> 12,47 M de MD). **Medio plazo:** recortar a AS por debajo de −1,8 M (distancia de junio de 2026) |
| Distancia con AS | −3,14 M | Por debajo de −1,8 M |
| Serie anual de UU MARCA | 12,0 – 14,8 M (ago-25 → ago-26) | Suelo por encima de 13 M fuera de picos |

> Los objetivos son propuesta de trabajo, no metas oficiales aprobadas por Dirección. Cerrar con [[gema-monjas|Gema Monjas]].

### Dos familias de KPI, las dos principales

Los KPIs de MARCA se leen siempre en dos familias. Las dos son principales, aunque fuera del equipo solo se miren las de volumen.

| | Volumen: cuánto | Consumo por usuario: cómo |
|---|---|---|
| Qué mide | Tamaño de la audiencia y del inventario | Intensidad y calidad del consumo |
| KPIs | Usuarios · Páginas vistas · Video views · Impresiones publicitarias | Páginas vistas por usuario · Video views por usuario · Sesiones por usuario · Permanencia (tiempo por usuario y por sesión) · Impresiones por usuario y por sesión · Páginas por sesión · Rebote · Scroll · Recirculación |
| Depende del calendario | **Sí.** Sube con una final de Champions y baja en un parón de selecciones | **No.** Al ir por usuario, aísla el efecto del calendario |
| Qué problema señala | Captación: SEO, Discover, redes, eventos, medición | Producto, contenido y experiencia: recirculación, portada, player, publicidad, CMP |

**Por qué el consumo por usuario es principal.** Un dato de volumen solo dice que el tráfico ha subido o bajado. El dato por usuario dice si la estrategia funciona con independencia de lo que pase en el calendario. Por eso es lo primero que se revisa al evaluar un proyecto, una estrategia o una caída de tráfico.

**Lectura cruzada** (aplicar siempre al revisar un proyecto o una caída):

| Volumen | Consumo por usuario | Diagnóstico | Dónde mirar |
|---|---|---|---|
| ↓ | = | Problema de **captación** o de calendario | Discover, SEO, redes, eventos, medición |
| = | ↓ | Problema de **producto o contenido**: entra la misma gente y consume menos | Recirculación, portada, player, carga, publicidad, CMP |
| ↑ | ↓ | **Pico de baja calidad**: llegan usuarios de paso que diluyen el consumo | Origen del tráfico nuevo (Discover viral, evento) y si se retiene |
| ↓ | ↓ | Problema **estructural** | Las dos cosas a la vez |
| ↑ | ↑ | La estrategia funciona | Documentar qué la explica para replicarlo |

> [!example] Ejemplo real: el Mundial de 2026
> En julio, los usuarios únicos subieron a 14,75 M (máximo del año), pero las páginas vistas por usuario bajaron de 84 en junio a 70. El Mundial trajo usuarios nuevos de menor consumo. En agosto, con menos usuarios (12,16 M), las páginas vistas por usuario vuelven a 76. Mirando solo el volumen, julio parece el mejor mes; por usuario, fue el de menor consumo.

### Cuadro de mando

**1. Volumen**

| KPI | Hoy (ago. 2026) | Objetivo | Fuente |
|---|---|---|---|
| Usuarios únicos | 12,16 M (AS 15,31 M) | Ver North Star | GfK |
| UU mobile | 10,90 M (AS 14,21 M) | Cerrar la mitad del hueco (−1,6 M) | GfK |
| Páginas vistas | 921 M · máx. 1.128 M (jun.) | No bajar mientras crece el alcance | GfK / Marfeel |
| Video views | Sin línea base consolidada | Por definir | Player / ad server |
| Impresiones publicitarias | Sin dato consolidado | Crecer con páginas vistas y fill rate | Ad server |

**2. Consumo por usuario**

| KPI | Hoy | Objetivo | Fuente |
|---|---|---|---|
| Páginas vistas por usuario | **76** (AS 34 · MD 19) · jun. 84 · jul. 70 | Mantener ≥ 75 fuera de picos; vigilar que no caiga en picos | GfK (PV / UU) |
| Video views por usuario | Sin medir | Línea base primero | Player / analítica |
| Sesiones por usuario | **31** (AS 13 · MD 8) | Mantener | GfK |
| Permanencia (tiempo por usuario y por sesión) | Sin línea base en el vault | Línea base y mejora | GfK / Marfeel |
| Páginas por sesión | 1,2-1,5 (estimado) | Subir con recirculación | Marfeel |
| Impresiones por usuario y por sesión | Sin medir | Subir sin dañar permanencia ni rebote | Ad server |
| Rebote | **36%** (AS 53%) | Mantener < 40% | GfK |
| Scroll medio | Sin línea base | Línea base | Marfeel |
| Recirculación interna y CTR de módulos | Sin medir | Línea base y mejora por módulo | Marfeel |
| Métricas de Portada | Sin línea base | Clics a noticia, scroll y flexes | Marfeel |

**3. Alcance y penetración** (empujan la North Star)

| KPI | Hoy | Objetivo | Fuente |
|---|---|---|---|
| Penetración nacional (universo 4+) | 29,1% | Por definir | GfK + EGM |
| Penetración Cataluña / C. Valenciana / Murcia | 24,6% / 25,1% / 25,7% | Llegar a la media (29,1%) ≈ **+0,55 M UU** | GfK |
| Afinidad 16-24 / 25-34 | 55-71 / 74-108 | Índice ≥ 100 en 25-34 | GfK (pedir dato actual a Analítica) |
| Tráfico de Discover | −80% desde jul. 2025 | Recuperar el nivel previo al 7-7-2025 | GSC |
| Redes y subdominios medidos | < 50% de las redes agregadas en Comscore | 100% de redes y subdominios atribuidos | Comscore / GfK |

**4. Vídeo y monetización**

| KPI | Hoy | Objetivo | Fuente |
|---|---|---|---|
| Completion rate | Sin medir | > 65% pre-roll · > 50% mid-roll | Ad server |
| Tasa de retorno al hub (7/30 días) | Sin medir | Línea base primero | Analítica |
| RPM de sesión | Sin línea base por sección | KPI de aprobación de cualquier cambio publicitario | Ad server |
| Fill rate programático | Sin dato | > 85% | Ad server |
| Viewability | Sin dato | > 70% display · > 80% vídeo | Ad server |
| Inventario addressable / usuarios logados | Sin medir | Por definir | CMP / login |
| Ratio directo vs. programática | Sin documentar | Referencia: 30% / 70% | Negocio |

### Estado de la medición

- No existe dashboard unificado de KPIs accesible a Producto.
- Taboola y Seedtag no tienen reporting directo.
- La mayoría de decisiones se toman sin datos suficientes.
- **Acción pendiente:** decidir qué herramienta consolida el cuadro de mando y quién lo reporta. El primer paso es el Looker de penetración de [[gfk-estrategia-audiencias]].

---

## 3. Cómo atacarlo

**Principio rector:** cada euro y cada hora van primero a lo que suma **usuarios nuevos** (alcance). La fidelidad ya es una fortaleza: se protege y se monetiza, pero no es donde está el hueco.

### Prioridades

| # | Frente | KPI que mueve | Impacto en UU | Depende de Redacción | Horizonte |
|---|---|---|---|---|---|
| 1 | Alcance móvil en grandes eventos y recuperar Discover | UU mobile, distancia con AS | Muy alto | Parcial | Ya |
| 2 | Medición: que cuente todo lo que ya tenemos | UU medidos | Alto, casi sin coste | No | Ya |
| 3 | Local: Cataluña, C. Valenciana y Murcia | Penetración por CCAA | +0,55 M | No | 3-6 meses |
| 4 | Edad y género: verticales y humor joven | Afinidad 16-34 | Alto | No (externalizado) | 6-12 meses |
| 5 | Vídeo como canal de captación | Video views, UU | Medio | Parcial | 6-12 meses |
| 6 | Monetizar la fidelidad | RPM, CPM, addressable | — (ingresos) | No | Continuo |
| 7 | Habilitadores: Redacción, IA, infraestructura | Todos | Indirecto | Sí | Continuo |

### Frente 1 — Alcance móvil en grandes eventos y Discover

**Objetivo:** que el próximo pico deportivo cierre la distancia con AS en lugar de abrirla.
- Diagnosticar por qué AS capta más lectores nuevos en los picos: Discover, redes, búsqueda y portada móvil, comparando julio de 2026 canal a canal.
- Cerrar la causa de la caída del 7-7-2025 en Discover ([[muvera]]) y revisar la sanción manual de junio de 2025.
- Preparar un protocolo de "modo competición" para eventos (Champions, Mundial, Clásicos): cobertura, Discover, redes y portada móvil coordinados.
- **KPI:** UU mobile, distancia con AS en el mes del evento, tráfico de Discover.

### Frente 2 — Medición: que cuente todo lo que ya tenemos

**Objetivo:** subir los UU medidos sin crear audiencia nueva.
- Agregar en Comscore las redes sociales que faltan (hoy no está ni la mitad).
- Confirmar que GfK atribuye a MARCA cada subdominio y cada dominio nuevo (verticales, MARCANET) antes de lanzarlos.
- Eliminar o medir la redirección por IP de portada: hoy contamina los datos e impide diagnosticar caídas.
- Montar el Looker de penetración sobre el universo GfK 4+ ([[gfk-estrategia-audiencias]]).
- **KPI:** UU GfK y Comscore, % de redes y subdominios agregados.

### Frente 3 — Local: Cataluña, C. Valenciana y Murcia

**Objetivo:** llevar las tres CCAA a la media de penetración (≈ +0,55 M UU; Cataluña sola es una quinta parte del hueco con AS).
- **MARCANET** (opción ágil, arranca ya): web con secciones por equipo escrita por pequeños creadores (2.000-10.000 seguidores, 50/50), en dominio propio y WordPress. Piloto con Barça, Espanyol, Girona, Valencia, Villarreal, Levante, Elche, Murcia y Cartagena; después Primera y Segunda, y México. Interlocutor: [[miguel-senovilla]].
- **Radios locales de [[radio-marca]]** (opción máxima): franquicias por plaza, frenadas por Legal. Se sigue empujando y se alimentan entre sí.
- Corregir la percepción promadridista con cobertura plural de los equipos de esas plazas.
- **KPI:** penetración e índice por CCAA (media de 3 meses), distancia con AS en Cataluña.

### Frente 4 — Edad y género: verticales y humor joven

**Objetivo:** subir la afinidad en 16-34 y abrir audiencia femenina.
- **Verticales deportivos propios primero**, con identidad propia (no "MARCA Running"): running, ciclismo, naturaleza, fitness, moda deportiva y economía del deporte.
- **Polideportivo externalizado** en subdominio (tenis, NBA, motor), donde hoy casi no hay cobertura.
- **No deportivo después**, en subdominios: lotería, viajes, tecnología, música. Precedentes: [[tiramillas]], [[cuidateplus]].
- **Humor para jóvenes** ([[marca-toons]]): sucesor de los Marcatoons, producido fuera con revenue share, pensado para cortes verticales.
- **KPI:** afinidad por franja de edad, UU por vertical, UU atribuidos por GfK a cada subdominio.

### Frente 5 — Vídeo como canal de captación

**Objetivo:** que el vídeo traiga usuarios nuevos, no solo views dentro de la web.
- Hoy: autoplay en contenidos, streaming en Portada y hub de vídeo (julio de 2025). YouTube no tiene estrategia.
- Estrategia de YouTube y vertical (TikTok, Shorts) con vuelta a MARCA, priorizando ediciones internacionales.
- Stock: acuerdos de contenido cedido y reutilización del archivo; ritmo mínimo de publicación.
- **KPI:** video views, completion rate, retorno al hub, UU que llegan desde vídeo externo.

### Frente 6 — Monetizar la fidelidad

**Objetivo:** que 921 M de páginas vistas y 31 sesiones por usuario se paguen como inventario premium.
- Revisar el CMP con UX: un consentimiento bajo degrada el inventario y explica parte de los CPMs bajos.
- Registro y datos 1st party (Fantasy, newsletters, Radio) para subir el inventario addressable.
- RPM de sesión como KPI de aprobación de cualquier cambio publicitario.
- Más venta directa y patrocinios ligados a audiencia (apuestas, automoción, banca).
- **KPI:** RPM, CPM por posición, fill rate, viewability, % addressable, ratio directo/programática.

### Frente 7 — Habilitadores

- **Redacción:** un responsable por proyecto (el coordinador, no el redactor), planificación diaria e informes automáticos con IA. Ellos proponen; SEO aporta y analiza.
- **IA en búsqueda:** comprobar en `robots.txt` qué user-agents se bloquean y separar `Google-Extended` del bloqueo general si se quiere estar en AI Overviews.
- **Infraestructura:** monitorización de rastreo para detectar a tiempo cualquier bloqueo a Googlebot.
- **Deportistas:** alianza con [[condor-media]] / [[straikr]] para recuperar el contacto directo con deportistas en España, México y USA.

---

## 4. Playbook por KPI

Acciones a corto y largo plazo por métrica. Sirven para ejecutar los frentes de la sección 3.

### Tráfico general

| KPI | Descripción | Por qué importa |
|---|---|---|
| Usuarios | Usuarios únicos (diarios/mensuales) | Base de audiencia. Determina el valor publicitario y la relevancia del medio |
| Páginas vistas | Total de páginas vistas en el sitio | Directamente ligado a impresiones publicitarias e ingresos programáticos |
| Video views | Reproducciones de vídeo | KPI específico del negocio de vídeo. Ligado a acuerdos y monetización de vídeo |

---

### Métricas de calidad

Estas métricas afectan directamente a tráfico, monetización y retención:

| Métrica | Relación con el negocio |
|---|---|
| Tasa de rebote | Un rebote alto reduce páginas vistas y retención de usuarios |
| Tiempo en página | Indica calidad de la experiencia; baja retención = menos páginas vistas |
| Páginas por usuario | Cada página adicional por sesión multiplica impresiones y RPM. En un sitio con media de 1,2-1,5 páginas por sesión, mejorar la profundidad equivale a más inventario sin aumentar usuarios |
| Scroll medio | Profundidad de lectura; proxy de interés real frente a rebote inmediato |
| Recirculación interna | Usuarios que navegan a más de una noticia. Multiplica las páginas vistas por sesión |
| CTR en módulos de recirculación | Eficacia de los módulos para retener al usuario dentro de MARCA |
| Métricas de la Portada | Clics a noticias desde la portada, scroll medio, rendimiento de flexes y módulos editoriales, y cualquier KPI de engagement específico de la home |
| Tasa de usuarios registrados / logados | Porcentaje de usuarios con identidad conocida. Base del inventario addressable y del CPM premium; entrada a modelos de suscripción o freemium |

#### Páginas por usuario / sesión

**Mejoras a corto plazo**
- Auditar los módulos de recirculación actuales: qué CTR tienen, dónde están colocados, si están activos en todos los dispositivos
- Activar recirculación contextual al final de cada noticia (artículos relacionados por tema, no solo por fecha)
- Reducir la tasa de rebote en portada mejorando la presentación de los titulares y el acceso a contenido en un clic

**Mejoras a largo plazo**
- Rediseñar la experiencia de artículo para que invite a continuar leyendo (siguiente noticia automática, módulos de recirculación en mitad del texto, no solo al final)
- Construir secciones de destino con contenido agrupado (Mundial 2026, LaLiga en directo) que aumenten la profundidad de sesión de forma natural
- Implementar notificaciones push y newsletters segmentadas para traer de vuelta a usuarios que ya salieron

#### CTR en módulos de recirculación

**Mejoras a corto plazo**
- Auditar CTR por módulo y dispositivo; desactivar o rediseñar módulos con CTR residual
- Probar titulares y miniaturas alineados con el artículo de origen (contexto > genérico)

**Mejoras a largo plazo**
- Personalizar recirculación según historial de lectura o sección cuando haya datos suficientes
- Integrar recirculación en el flujo de lectura (mitad de artículo) con formato nativo

#### Tasa de usuarios registrados / logados

**Mejoras a corto plazo**
- Medir la tasa actual de logins activos sobre el total de usuarios únicos mensuales
- Activar un CTA de registro contextual en los momentos de mayor intención (final de artículo largo, acceso a estadísticas, Fantasy MARCA)
- Simplificar el flujo de registro: login social (Google, Apple) como opción principal

**Mejoras a largo plazo**
- Construir una propuesta de valor clara para el usuario registrado: qué recibe a cambio de darse de alta
- Integrar los registros de todos los productos MARCA (Fantasy, newsletters, Radio) en un único perfil de usuario unificado
- Explorar un modelo freemium ligero: contenido premium o sin publicidad para usuarios registrados como incentivo

---

### Métricas de publicidad

KPIs del área publicitaria. Se evalúan de forma complementaria al tráfico y a la calidad de la experiencia: una mejora en publicidad que dañe usuarios o páginas vistas es un resultado negativo.

| Métrica | Descripción |
|---|---|
| Impresiones publicitarias | Derivado directo de páginas vistas y de la configuración de inventario |
| Fill rate programático | Porcentaje de las solicitudes de anuncio (ad requests) que reciben una respuesta con anuncio real. Un fill rate bajo indica invendidos. Benchmark: >85% en sitios de tráfico alto con header bidding activo |
| CPM medio por posición y Content Type | Coste por mil impresiones, segmentado por slot/placement y por tipo de contenido (artículo, portada, vídeo, etc.) |
| Viewability | Porcentaje de impresiones realmente vistas (IAB: al menos el 50% del anuncio visible ≥1 s; vídeo ≥2 s). Benchmark: >70% display, >80% vídeo |
| Patrocinios | Ingresos por acuerdos directos: secciones, competiciones, formatos especiales. La renovación está ligada a KPIs de audiencia |
| Invendidos en programática | Porcentaje del inventario sin puja efectiva; coste de oportunidad y riesgo de mala UX si queda vacío |
| RPM de sesión | Ingresos por cada mil sesiones; combina fill rate, CPM, páginas por sesión y viewability. Fórmula: (ingresos totales / sesiones totales) × 1000 |
| Porcentaje de inventario addressable | Impresiones con datos 1st/3rd party que permiten targeting. El inventario sin dato se vende a fracción del precio en open auction |
| Frecuencia media por usuario | Veces que un usuario ve el mismo anuncio en sesión o período. Exceso reduce CPM percibido |
| Ratio ingresos directos vs programática | Parte de ingresos de venta directa (patrocinios, campañas) frente a programática. Un ratio muy alto de programática expone a fluctuaciones de mercado |

#### Viewability

**Mejoras a corto plazo**
- Reposicionar los slots existentes más arriba en el viewport (above the fold) sin añadir nuevos formatos
- Eliminar o reducir slots con viewability consistentemente por debajo del 40%
- Revisar la velocidad de carga de las páginas: un scroll más lento antes de la carga mejora la exposición

**Mejoras a largo plazo**
- Rediseñar las plantillas de artículo para que los slots publicitarios queden integrados en el flujo de lectura natural
- Implementar lazy loading inteligente que cargue el anuncio justo cuando entra en viewport
- Establecer reporting automático de viewability por formato y sección para detectar degradaciones

#### Completion rate en vídeo

**Mejoras a corto plazo**
- Limitar la duración de pre-rolls a 15 segundos no saltables (reduce abandono)
- Reducir la frecuencia de mid-rolls en vídeos de menos de 3 minutos
- Revisar el orden de los anunciantes: los creativos más cortos o más relevantes para la audiencia deportiva primero

**Mejoras a largo plazo**
- Desarrollar targeting contextual por tipo de contenido (partido en directo vs. resumen vs. entrevista) para aumentar relevancia del anuncio
- Negociar con anunciantes formatos de vídeo nativos integrados en el player (branded content) con mayor tolerancia del usuario
- Crear un score de calidad de anuncio interno para priorizar creativos con mayor completion rate histórico

#### Inventario de vídeo

**Mejoras a corto plazo**
- Aumentar la distribución de contenido de vídeo en homepage y secciones de alto tráfico (sin crear fricción)
- Activar autoplay con sonido desactivado en los módulos de recirculación donde aún no esté habilitado
- Añadir un slot de pre-roll en los vídeos del hub que actualmente no lo tienen

**Mejoras a largo plazo**
- Aumentar la producción editorial de vídeo corto (60-90 segundos) para generar más sesiones de vídeo por usuario
- Construir el hub de vídeo como destino recurrente (newsletters, notificaciones push) para multiplicar sesiones de vídeo
- Explorar sindicación de contenido de vídeo externo (agencias, ligas) para aumentar inventario sin coste editorial

#### Fill rate programático

**Mejoras a corto plazo**
- Revisar los pisos de precio (price floors) en los slots con mayor volumen de invendidos: bajar el floor puede recuperar demanda programática sin impactar CPM medio de forma relevante
- Activar más SSPs o DSPs en los slots con mayor volumen de invendidos
- Revisar la configuración de passback: cuando un slot queda invendido, debe servir un house ad o un formato alternativo en lugar de espacio en blanco

**Mejoras a largo plazo**
- Implementar header bidding completo si no está activo, o auditar la configuración actual con el equipo de ad tech
- Establecer acuerdos preferred deals o programmatic guaranteed con anunciantes recurrentes para garantizar cobertura mínima en fechas clave (LaLiga, Copa del Rey, eventos MARCA)
- Crear segmentos de audiencia propios (datos 1st party) para aumentar el valor del inventario remanente en open auction

#### CPM medio (por posición y Content Type)

**Mejoras a corto plazo**
- Segmentar el inventario por sección y contexto para comunicarlo mejor a los compradores (la sección de fútbol tiene más valor que una página genérica)
- Revisar que todos los slots tienen las categorías IAB correctamente definidas en el ad server
- Activar deal ID con los principales anunciantes de automoción, apuestas y banca (categorías de mayor CPM en medios deportivos españoles)

**Mejoras a largo plazo**
- Desarrollar una estrategia de datos 1st party que permita ofrecer segmentos verificados a los compradores (fans de Real Madrid, usuarios de Fantasy MARCA, etc.)
- Construir un paquete de patrocinio + programática para anunciantes que combinen ambas vías y justifiquen un CPM premium
- Auditar con el equipo de ad tech si existe discrepancia entre impresiones registradas en el ad server y en los DSPs (la discrepancia reduce el CPM percibido por el comprador)

#### Patrocinios

**Mejoras a corto plazo**
- Documentar el inventario de patrocinios activos: qué está vendido, a qué precio, hasta cuándo, y qué métricas se reportan al patrocinador
- Crear un one-pager de cada sección patrocinada con datos de audiencia actualizados (para facilitar renovaciones y nuevas ventas al equipo comercial)
- Identificar secciones de alto tráfico sin patrocinio activo como oportunidades inmediatas para el equipo de ventas

**Mejoras a largo plazo**
- Crear productos de patrocinio ligados al Mundial 2026 con visibilidad asegurada durante el torneo
- Desarrollar formatos de branded content nativo para patrocinadores que quieran ir más allá del logo en una sección
- Establecer un calendario de renovaciones con antelación suficiente para que comercial pueda negociar antes del fin de contrato

#### Invendidos en programática

**Mejoras a corto plazo**
- Mapear qué slots, secciones y franjas horarias concentran más invendidos (el problema suele ser muy desigual)
- Configurar house ads o contenido propio (promoción de Fantasy MARCA, Radio MARCA) como fallback en los slots con mayor tasa de invendidos
- Revisar si los slots con más invendidos tienen problemas técnicos de configuración (tamaños no estándar, tiempos de respuesta altos)

**Mejoras a largo plazo**
- Reducir el número de slots en las páginas con mayor tasa de invendidos: menos inventario de menor calidad puede generar más ingresos que mucho inventario mal monetizado
- Explorar acuerdos de backfill con redes publicitarias de garantía (Google Ad Exchange como backfill de último nivel)
- Usar los invendidos como oportunidad de autopromoción medida: newsletters, suscripción MARCA+, app — con tracking para evaluar si generan valor equivalente al CPM de mercado

#### RPM de sesión

**Mejoras a corto plazo**
- Cruzar el RPM por sección: portada y noticias probablemente tienen RPM muy distinto. Actuar primero donde el gap es mayor
- Medir el impacto de cada cambio de publicidad en RPM, no solo en CPM o fill rate aislados
- Establecer una línea base mensual para detectar degradaciones rápido

**Mejoras a largo plazo**
- Usar el RPM como KPI de aprobación para cualquier cambio de publicidad: ningún formato nuevo se implementa sin proyección de impacto en RPM
- Segmentar el RPM por tipo de usuario (recurrente vs nuevo, logado vs anónimo) para priorizar inversión en los segmentos más rentables
- Construir el dashboard de RPM por sección, dispositivo y franja horaria como herramienta de decisión permanente

#### Porcentaje de inventario addressable

**Mejoras a corto plazo**
- Medir qué porcentaje del tráfico actual está logado o tiene cualquier dato 1st party asociado
- Activar el registro en los productos que ya tienen base de usuarios: Fantasy MARCA, newsletters, Radio MARCA
- Configurar la pasarela de registro con fricción mínima (login con Google, sin formulario largo)

**Mejoras a largo plazo**
- Construir una estrategia de datos 1st party: qué datos se recogen, cómo se activan en el ad server, cómo se ofrecen a los compradores
- Crear incentivos de registro ligados a contenido o funcionalidades exclusivas (estadísticas avanzadas, alertas de resultados, Fantasy premium)
- Explorar la creación de segmentos de audiencia propios vendibles como deal ID (fans de clubes concretos, consumidores de vídeo, usuarios de alta frecuencia)

#### Frecuencia media por usuario

**Mejoras a corto plazo**
- Revisar si hay frequency capping configurado en el ad server y en qué límite está por defecto
- Comparar el CPM de las primeras impresiones por usuario vs las impresiones de alta frecuencia: el diferencial indica cuánto daño hace el exceso
- Ajustar los caps por formato: los formatos más intrusivos (interstitial, skin) necesitan caps más agresivos

**Mejoras a largo plazo**
- Establecer una política de frequency capping por defecto para todos los formatos, revisable trimestralmente
- Usar los datos de frecuencia para argumentar ante los anunciantes que el inventario de MARCA tiene alcance real, no solo impresiones repetidas
- Explorar modelos de compra por reach único en lugar de por impresiones para anunciantes de branding

#### Ratio ingresos directos vs programática

**Mejoras a corto plazo**
- Medir el ratio actual si no está documentado: es el punto de partida para cualquier decisión estratégica
- Identificar 3-5 anunciantes actuales de programática con gasto alto que podrían convertirse en acuerdos directos más estables
- Crear un paquete de venta directa específico para el Mundial 2026 con garantía de visibilidad

**Mejoras a largo plazo**
- Establecer un objetivo de ratio (por ejemplo, 30% directo / 70% programática) como meta estratégica del área de negocio
- Desarrollar un equipo o proceso de venta directa más activo para categorías con alto CPM (apuestas, automoción, banca)
- Construir productos publicitarios propios (branded content, newsletters patrocinadas, especiales editoriales) que no dependan de la programática

#### Impresiones publicitarias

Las mejoras pasan por aumentar páginas vistas de calidad, fill rate y CPM. Ver acciones en RPM de sesión, páginas por usuario, fill rate, CPM y recirculación en las secciones correspondientes de este documento.

---

### Métricas de vídeos

MARCA puede consolidar una plataforma de vídeo (OTT o semi-OTT) con inventario propio y cedido. El inventario de vídeo debe cumplir los **criterios técnicos y de calidad** exigidos por publicidad (duración mínima cobrable, viewability del player, políticas de autoplay, etc.) alineados con el equipo de ad tech.

| Métrica | Descripción |
|---|---|
| Video views | Volumen de reproducciones (alineado con tráfico general; aquí se desglosa para negocio vídeo y monetización) |
| Completion rate | Porcentaje de anuncios de vídeo (pre-roll, mid-roll) reproducidos hasta el final o punto mínimo cobrable. Benchmark: >65% pre-roll, >50% mid-roll |
| Inventario de vídeo | Impresiones de vídeo disponibles para monetizar; depende de video views y de slots por sesión |
| Stock total y tasa de crecimiento del catálogo | Número de vídeos en catálogo (original vs cedido) y ritmo de publicación (semanal/mensual). Sin ritmo constante el catálogo envejece |
| Video views por vídeo publicado | Vistas medias por pieza; diagnostica distribución vs relevancia del contenido |
| Duración media de sesión de vídeo | Tiempo de consumo de vídeo por visita; indica consumo en cadena |
| Acuerdos de contenido cedido | Fuentes externas recurrentes (agencias, clubes, ligas, federaciones, medios). Más fuentes = stock más robusto |
| Coste por vídeo producido y ROI | Coste medio de producción original frente a views e ingresos atribuibles; prioriza formatos rentables |

#### Stock total de vídeo

**Mejoras a corto plazo**
- Auditar el catálogo actual: cuántos vídeos activos hay, qué antigüedad tienen, cuántos tienen views reales y cuántos están sin distribuir
- Activar acuerdos con agencias de contenido deportivo ya disponibles en el mercado (Reuters Sport, AP Sports, beIN Sports clips, Sportradar) para aumentar el stock de forma inmediata sin coste editorial
- Reutilizar el archivo propio: clips de entrevistas antiguas, resúmenes históricos, momentos icónicos de MARCA — con packaging editorial mínimo tienen valor de consumo

**Mejoras a largo plazo**
- Establecer acuerdos de sindicación con LaLiga, Real Madrid TV, Atlético de Madrid, selección española y federaciones nacionales
- Crear una línea de producción de contenido original corto (60-90 segundos) con formato fijo: dato del día, análisis exprés, predicción de partido
- Explorar acuerdos de co-producción con otros medios del grupo RCS para amortizar el coste de contenido original

#### Tasa de crecimiento del catálogo

**Mejoras a corto plazo**
- Establecer un mínimo de publicación semanal por categoría (resultados, entrevistas, análisis) aunque sea con producción básica
- Definir responsabilidades editoriales claras: quién produce, quién edita, quién publica y en qué plazo desde el evento
- Crear plantillas de producción de vídeo corto que reduzcan el tiempo de edición a menos de 30 minutos por pieza

**Mejoras a largo plazo**
- Construir un calendario editorial de vídeo alineado con el calendario deportivo (pretemporada, LaLiga, Champions, Copa, Mundial 2026)
- Invertir en herramientas de edición automatizada (IA para highlights, subtitulación automática, clipping de partidos) para aumentar el volumen sin escalar el equipo
- Desarrollar una estrategia de contenido evergreen que no dependa del directo: rankings históricos, especiales de jugadores, documentales cortos

#### Video views por vídeo publicado

**Mejoras a corto plazo**
- Identificar los 20 vídeos con más views del último mes: qué tienen en común (formato, duración, temática, momento de publicación)
- Revisar la distribución actual: los vídeos aparecen en la home, en las noticias relacionadas, en el hub de vídeo. ¿Están todos los puntos de entrada activos?
- Mejorar los thumbnails y títulos de los vídeos más estratégicos: en plataformas de vídeo el CTR del thumbnail es determinante

**Mejoras a largo plazo**
- Implementar recomendación algorítmica de vídeo basada en el comportamiento del usuario (qué vio antes, qué temática consume)
- Distribuir el contenido de vídeo en canales externos (YouTube, redes sociales) con link de vuelta a MARCA para aumentar el alcance sin canibalizar las views propias
- Crear series de vídeo con continuidad (formato episódico) que generen hábito de consumo y retorno

#### Duración media de sesión de vídeo

**Mejoras a corto plazo**
- Activar autoplay del siguiente vídeo relacionado al terminar el que se está viendo
- Reducir la fricción entre vídeos: el reproductor no debe volver a la página de artículo entre vídeo y vídeo si el usuario está en el hub
- Construir listas de reproducción temáticas (todos los goles de Vinicius esta temporada, resúmenes de la jornada) que incentiven el consumo en cadena

**Mejoras a largo plazo**
- Construir un hub de vídeo con experiencia de navegación propia, separada del flujo de noticias, pensada para el consumo de vídeo continuo
- Desarrollar contenido de larga duración (20-45 minutos) para usuarios con alta intención de consumo: documentales, entrevistas en profundidad, especiales de competición
- Estudiar la viabilidad de una sección de vídeo en directo o semi-directo con contenido exclusivo (ruedas de prensa, entrenamientos abiertos, análisis post-partido)

#### Acuerdos de contenido cedido activos

**Mejoras a corto plazo**
- Mapear todos los acuerdos de contenido de vídeo activos: qué se recibe, con qué frecuencia, en qué condiciones de uso
- Identificar los gaps más obvios: si no hay acuerdo con ninguna agencia de noticias deportivas, es la primera prioridad
- Revisar si los acuerdos existentes se están aprovechando al 100% o hay contenido disponible que no se publica

**Mejoras a largo plazo**
- Negociar acuerdos de contenido con los clubes más seguidos por la audiencia de MARCA (Real Madrid, Barcelona, Atlético) — muchos tienen canales propios con material cedible
- Explorar acuerdos de reciprocidad con medios internacionales del grupo RCS (La Gazzetta dello Sport, Corriere della Sera) para intercambio de contenido deportivo
- Desarrollar un proceso estandarizado de ingesta, metadatado y publicación de contenido cedido que reduzca el tiempo entre recepción y publicación a menos de 2 horas

#### Coste por vídeo producido y ROI

**Mejoras a corto plazo**
- Documentar el coste real actual de producción de vídeo por tipo de pieza (sin este dato no hay decisión posible)
- Clasificar el catálogo en tres niveles de producción: básico (redactor + teléfono), medio (equipo + edición), premium (producción completa)
- Priorizar el nivel básico para aumentar volumen rápido y medir qué temáticas funcionan antes de invertir en producción mayor

**Mejoras a largo plazo**
- Establecer un umbral mínimo de views por vídeo para justificar el coste de cada nivel de producción
- Calcular el CPM equivalente del contenido original propio (ingresos publicitarios generados por ese vídeo / coste de producción) para compararlo con el coste de contenido cedido
- Usar el ROI por formato para construir el presupuesto de vídeo del año siguiente con criterio, no solo por intuición editorial

---

### Hub de vídeos

KPIs específicos del **destino vídeo** (home de vídeos, hub), además del consumo embebido en noticias:

| Métrica | Descripción |
|---|---|
| Crecimiento del hub de vídeos | Usuarios, sesiones o video views atribuibles al hub frente a baseline (se alinea con stock, distribución y promoción) |
| Frecuencia de actualización de la Home de vídeos | Cadencia con la que se renuevan destacados, carruseles y módulos editoriales; afecta recurrencia |
| Volumen de producción | Piezas publicadas en el hub / canal vídeo en el período |
| Rendimiento por vídeo / contexto | CTR, views, completion y engagement por pieza, formato o placement en el hub |
| Tasa de retorno al hub | Porcentaje de usuarios que vuelven al hub en 7 o 30 días tras la primera visita; indicador de hábito y justificación de inversión en contenido |

#### Tasa de retorno al hub de vídeo

**Mejoras a corto plazo**
- Activar notificaciones push específicas para usuarios que ya han consumido vídeo: alertas de nuevo contenido de sus temáticas
- Crear una newsletter semanal de vídeo: los 5 mejores vídeos de la semana, con acceso directo al player
- Medir la tasa actual: sin línea base no se puede gestionar el KPI

**Mejoras a largo plazo**
- Lanzar una identidad de marca para el hub de vídeo de MARCA como destino específico, diferenciado del medio de noticias
- Explorar la creación de contenido exclusivo para el hub que no se distribuye en el resto del site (genera razón de visita)
- Evaluar si un modelo de acceso premium al catálogo de vídeo (MARCA+ o similar) tiene viabilidad dado el volumen y calidad del stock

#### Crecimiento del hub, Home de vídeos y producción

Las acciones de Stock total, Tasa de crecimiento del catálogo, Inventario de vídeo y Duración media de sesión de vídeo aplican también al crecimiento del hub, la cadencia de la Home de vídeos y el volumen de producción. Priorizar según el gap medido (usuarios recurrentes vs nuevos, secciones con más abandono).

---

## 5. Anexo — contexto operativo

### Responsabilidades del departamento SEO

- Estrategia de canales SEO: Search, Google News, Showcase y Discover
- Desarrollo de audiencias: análisis de edades, géneros, ubicación y comportamiento por plataforma y temática
- Revisión de viabilidad técnica SEO en todas las capas: definiciones, validaciones, seguimiento y revisiones post-salida
- Coordinación entre la edición española y las ediciones de México y USA
- Objetivo a medio plazo: ampliar el scope más allá del orgánico hacia otros canales de captación de audiencia

**Modelo de intervención:**
- Editorial: Damien fija el camino estratégico; no toca el día a día editorial salvo el análisis de tráfico
- Técnica: toda decisión se debate con los stakeholders correspondientes, salvo problemas técnicos puros o aspectos 100% SEO donde puede actuar solo si el CMS o las herramientas lo permiten

### Estructura de reporte y stakeholders clave

El departamento de Audiencias/SEO pertenece orgánicamente a **Tecnología**, pero está físicamente en la **Redacción**. Esto posiciona al equipo en la intersección de todos los departamentos.

**Damien reporta directamente a:**
- **Nacho Delgado**
- **Gema Monjas** — Directora de Negocio Nacional. Suele estar del lado de Damien, aunque no siempre tiene el apoyo interno que necesita.
- **Juan Ignacio Gallardo** — Director de MARCA
- **Emilio Contreras** — Director Adjunto España
- **François Guérin** — Director Global de MARCA. Interlocutor complejo: toma decisiones sin conocimiento técnico ni consulta a los equipos correctos. Ejemplos: rediseñó el CMP (originalmente implementado en enero 2024 por obligación legal) cuando llegó al cargo, con cambios específicos para USA/MX sin coordinación clara con UX; implementó una redirección por IP en la portada sin medirla, con el objetivo de maquillar datos.

**Redacción (estrategia editorial):**
- Juan Ignacio Gallardo — Director de MARCA
- Emilio Contreras — Director Adjunto España
- Francisco Villalobos — Redactor Jefe para Internacional

**Producto:**
- Karen Rodrigues — Head of Product
- Javier Rodríguez — Producto Editorial

**Tecnología:**
- Belén Gómez
- Jorge Abboud
- Ricardo Moreno

### Fricciones operativas

**Director de Audiencias (nuevo rol):** Se ha contratado un Director de Audiencias que cubre redes sociales y la parte editorial de Tiramillas (contenido no deportivo). Antes, estas áreas las gestionaba el equipo SEO. El solapamiento de responsabilidades genera fricción constante sobre quién decide qué.

**Investigación técnica sin documentación:** Gran parte del tiempo se pierde investigando problemas técnicos que no tienen respuesta documentada. Nada está documentado internamente.

**Redacción como cuello de botella:** Los responsables editoriales frenan la adopción de estrategias SEO. La calidad editorial de MARCA es objetivamente baja comparada con otros medios de Unidad Editorial como El Mundo. Si MARCA quiere volver a crecer, hay que buscar vías que no dependan de Redacción.

**Monetización desconectada de audiencia:** Los CPMs son bajos. Desde Negocio se atribuye al "inventario de baja calidad". En la práctica, el foco siempre está en crecer en audiencia, pero el tráfico no se monetiza bien. La presión existe, pero siempre apunta hacia otro lado.

### Problemáticas y necesidad de negocio

- **Deportistas y representación:** Los deportistas ya no necesitan los medios para hacerse ver. Necesidad de recuperar el contacto directo y hacer que lo valoren. Iniciativa en curso: Damien habló con **Condor Media** (empresa madre de **Straikr**), que integra una empresa de representación de jugadores. Una alianza podría ser clave para crecer en España, México y USA.
- **Decadencia de medios tradicionales** frente al auge de apps de resultados, plataformas audiovisuales y redes sociales.
- **Web obsoleta** con imagen de marca envejecida.
- **Imagen promadridista y poco plural** — visible en datos de Cataluña y Comunidad Valenciana. Problema reconocido internamente, aunque muchos lo eviten.
- **Bloqueo de IAs:** Decisión corporativa de bloquear todos los bots de IA para negociar remuneración con las tecnológicas. Riesgo real: si el bloqueo incluye `Google-Extended` (usado para AI Overviews), MARCA queda fuera de las respuestas de IA en búsqueda justo cuando ese canal crece. Pendiente verificar qué user-agents están bloqueados en `robots.txt`.
- **Medición infravalorada:** MARCA no tiene ni la mitad de sus redes sociales agregadas en ComScore, lo que reduce artificialmente su cuota de mercado percibida.

### Problemas adicionales identificados

- El CMP diseñado sin UX probablemente está afectando las tasas de consentimiento, lo que impacta directamente en la calidad del inventario publicitario y los CPMs bajos.
- La redirección por IP en portada sin medición contamina los datos de tráfico y hace imposible diagnosticar caídas reales.
- YouTube sin estrategia es una oportunidad de captación de audiencia nueva desaprovechada, especialmente relevante para las ediciones internacionales.
- La opacidad de infraestructura es un riesgo SEO permanente: si Googlebot queda bloqueado por algún cambio de sistemas y nadie lo detecta, el impacto puede ser enorme antes de que se identifique.

### Herramientas del día a día

| Herramienta | Uso principal |
|---|---|
| Marfeel | Análisis de audiencias y comportamiento |
| Trello | Gestión de tareas y prioridades del equipo |
| Gemini | Apoyo en tareas de IA |
| NotebookLM | Gestión y análisis de documentación con IA |
| Google Cloud Shell | Entorno de desarrollo y automatizaciones |
| Claude | Asistente IA principal |
| Google Workspace | Suite ofimática (Drive, Docs, Sheets, Meet) |
| Confluence | Documentación interna |
| Jira | Proyectos técnicos y tickets |
| Kibana | Análisis de logs de servidor |
| GitHub | Control de versiones y repositorio de proyectos |
| Make | Automatizaciones y flujos de trabajo |
| Straikr | Plataforma de representación de deportistas |
| Narrativa | Generación automática de contenido con IA |
| Google Search Console | Rendimiento orgánico, cobertura, rastreo |
| Screaming Frog | Auditoría técnica SEO y rastreo de URLs |
| Teams | Comunicación corporativa |
| Outlook | Correo corporativo |
| Google Trends | Tendencias de búsqueda y oportunidades |

### MCP / Automatizaciones

- **gdrive** — MCP server de Google Drive configurado en `~/.claude/settings.json`. Requiere reinicio de sesión para activarse.
- **playwright** — MCP server de Playwright configurado con Chrome Profile 10 (`~/Library/Application Support/Google/Chrome/Profile 10`), perfil dedicado "Claude" con sesión iniciada en Confluence y otras herramientas internas. No hay API token de Confluence disponible. Requiere reinicio de Claude Code para activarse.

### Stack tecnológico (CMS)

| CMS | Edición / Uso |
|---|---|
| **Xalok** | España (actual). CMS nuevo, en proceso de implantación para las demás ediciones |
| **UEdit** | Ediciones internacionales (USA, México, English). CMS antiguo; su falta de flexibilidad fue el principal freno para avanzar técnicamente |
| **Talea** | Directos en MARCA. Versión equivalente en El Mundo, Expansión y Telva |
| **Drupal** | CuídatePlus (subdominio de MARCA). El que más guerra ha dado históricamente |

**Deuda técnica y limitaciones:** Enorme deuda acumulada. Los principales cuellos de botella son la velocidad de desarrollo, la falta de autonomía para ejecutar y —el más crítico para SEO— la opacidad en la capa de infraestructura y sistemas, que impide saber si se está bloqueando algo a Google.

### Timeline — Cambios y eventos clave

Cronología de cambios técnicos, editoriales y algorítmicos relevantes para el análisis SEO de MARCA.

**Categorías:**
- `[XALOK]` — migración de CMS
- `[CONSENT]` — cambios en gestión de consentimiento (CMP)
- `[MIDDLEWARE]` — despliegue del middleware publicitario
- `[GOOGLE]` — algoritmos / actualizaciones / acciones manuales
- `[VÍDEOS]` / `[HUB DE VÍDEOS]` — vídeo y hub multimedia
- `[AMP]` — cambios en infraestructura o dominio AMP
- `[ROBOTS.TXT]` — cambios en robots.txt
- `[ESTÁTICOS]` — infraestructura de archivos estáticos
- `[REDACCIÓN]` — cambios de producción o agencias
- `[MEDICIÓN]` — cambios en analítica o atribución
- `[INDEXACIÓN]` — problemas de indexación
- `[MX]` / `[USA]` / `[EN]` — acciones específicas por edición
- `[TIRAMILLAS]` — sección Tiramillas
- `—` — evento externo, incidencia o mejora sin categoría específica

#### 2025

##### Marzo

| Fecha | Categoría | Evento |
|---|---|---|
| 31 Mar | [XALOK] | Migración Tiramillas |

##### Abril

| Fecha | Categoría | Evento |
|---|---|---|
| 03 Abr | [XALOK] | Migración crónicas + Portadillas sección fútbol |
| 08 Abr | [XALOK] | Migración Portada - ES |
| 23-29 Abr | [INDEXACIÓN] | Problemas de indexación |
| 28 Abr | [CONSENT] | Subida AMP - IP USA |

##### Mayo

| Fecha | Categoría | Evento |
|---|---|---|
| 02 May | [VÍDEOS] | Integración de STN en todos los contenidos |
| 15 May | [REDACCIÓN] | Aumento de producción con SAM |
| 22 May | [CONSENT] | Implementación Fase 2 |

##### Junio

| Fecha | Categoría | Evento |
|---|---|---|
| 01 Jun | [REDACCIÓN] | Cambio de agencias internacional (Raíz → LW) |
| 02 Jun | [GOOGLE] | Sanción manual - 1er aviso |
| 04 Jun | [CONSENT] | Eliminación Consent 45 Estados |
| 09 Jun | [MIDDLEWARE] | Despliegue y activación al 0% (solo con cookie) |
| 12-13 Jun | — | Problemas con Google Lens, Discover y Voice Search |
| 13 Jun | — | Google Search experimenta problemas de indexación |
| 30 Jun – 17 Jul | [GOOGLE] | **June 2025 Core Update** |

##### Julio

| Fecha | Categoría | Evento |
|---|---|---|
| 07 Jul | [ROBOTS.TXT] | Subida en amp.marca.com |
| 07 Jul | [GOOGLE] | **Caída de tráfico (-80% Discover)** |
| 14 Jul | [ROBOTS.TXT] | Subida robots.txt a AMP US (amp-us.marca.com/robots.txt) |
| 14 Jul | [MIDDLEWARE] | Activación al 1% desktop |
| 16 Jul | [HUB DE VÍDEOS] | Salida a producción |
| 26 Jul | [VÍDEOS] | Autoplay en AMP |
| 29 Jul | [MEDICIÓN] | SEO Branded se asigna a Directo - Google |
| 30 Jul | [CONSENT] | Rediseño MX y USA |

##### Agosto

| Fecha | Categoría | Evento |
|---|---|---|
| 11 Ago | [AMP] | Cambio de dominio NFL - ENGLISH |
| 11 Ago | — | Prueba AMP NFL |
| 12 Ago | — | Prueba AMP Bienestar |
| 12 Ago | [AMP] | Cambio de dominio Bienestar - España |
| 26 Ago – 22 Sep | [GOOGLE] | August 2025 Spam Update |
| 27 Ago | [TIRAMILLAS] | Eliminación de Seedtag de la imagen principal |
| 27 Ago | [MX] | Se elimina la redirección de Portada IP MX |

##### Septiembre

| Fecha | Categoría | Evento |
|---|---|---|
| 05 Sep | — | Rotación de subdominios |

##### Octubre

| Fecha | Categoría | Evento |
|---|---|---|
| 02 Oct | [VÍDEOS] | Activación del PiP en web |
| 03-06 Oct | — | Problemas continuos de servicio (Serving) |
| 07 Oct | [MIDDLEWARE] | Activación al 5% desktop |
| 13 Oct | [ESTÁTICOS] | Cambio a objetos-estáticos |
| 20 Oct | [ROBOTS.TXT] | Nuevo robots.txt bloqueando apw, nydus* y edge-services/user-geo.html* |
| 22 Oct | [MX] | Redirección 302 - Portada ES |
| 23 Oct | — | Mejora en detección de tablets en reportes de analítica |
| 23 Oct | [USA] | Redirección por IP (Maine, Virginia, Vermont, Pennsylvania, Dakota del Norte y Sur) |
| 27 Oct | [EN] | Noticia mobile — Retraso JS Kaltura, eliminación loader Taboola y refactorización JQuery |
| 29 Oct | — | Mejora en la atribución de refresco (Refresh attribution) |

##### Noviembre

| Fecha | Categoría | Evento |
|---|---|---|
| 03 Nov | [EN] | Limpieza contenidos críticos |
| 04 Nov | [USA] | Redirección Portada IP US (resto de Estados) |
| 14 Nov | — | Actualización de métricas de Facebook para compatibilidad con API |

##### Diciembre

| Fecha | Categoría | Evento |
|---|---|---|
| 11-29 Dic | [GOOGLE] | **December 2025 Core Update** |
| 15 Dic | — | Mejoras en la precisión de Web Vitals |

#### 2026

##### Enero

| Fecha | Categoría | Evento |
|---|---|---|
| 12 Ene | [MIDDLEWARE] | Activación al 20% en desktop |

##### Febrero

| Fecha | Categoría | Evento |
|---|---|---|
| 05-27 Feb | [GOOGLE] | **February 2026 Discover Update** |
| 25 Feb | — | Incidencia puntual en el servicio (Serving) |

##### Marzo

| Fecha | Categoría | Evento |
|---|---|---|
| 24-25 Mar | [GOOGLE] | March 2026 Spam Update |
| 27 Mar | [GOOGLE] | **March 2026 Core Update** |

---

## 🔗 Relacionado

- [[damien-santiago]]
- [[equipo-seo-marca]]
- [[organigrama-marca]]
- [[gema-monjas]]
- [[gfk-estrategia-audiencias]] — plan de usuarios únicos GfK (local, edad y género, Redacción)
- [[gfk]] — SOP de análisis de informes GfK
- [[muvera]] — caída de tráfico del 7-7-2025
- [[marca-competitors-spain]]
- [[spain-dafo-analysis]]
- [[radio-marca]]
- [[marca-toons]]
- [[dinamica-editorial-marca-es]]
