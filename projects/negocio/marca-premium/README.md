# MARCA Premium

**Estado:** En definición — lanzamiento previsto tras el parón de septiembre 2026
**Ultima actualizacion:** 2026-05-06

## Status 2026-04-16

- Mei mostró la nueva landing con los planes.
- **MARCA PRO no estará entre las ofertas** del nuevo Premium.
- Las secciones de Tiramillas, Gaming y las estáticas **no se cerrarán**. Tampoco noticias en AMP.
- Se va a evaluar con Publicidad la posibilidad de **reducir posiciones publicitarias** que se muestran a los suscriptores.
- Habrá un **trial gratuito** o con un precio más bajo.
- **Lanzamiento:** después del parón de septiembre 2026.
- Se plantea **Google One Tap** para captar registros. En El Mundo está funcionando muy bien. Pendiente de estimacion de esfuerzo tecnico antes de aprobar.
- **CLUB MARCA / Jakala:** en evaluación empresas que puedan sustituir a Jakala. Reunion con Qualifio prevista semana del 12/05/2026.
- **Qualifio:** estimado el GNP para enviar información de autenticación del usuario a Qualifio. Talla estimada: S.

---

## Descripcion

Transicion de MARCA hacia un modelo de negocio hibrido: desde la gratuidad total hacia un modelo Premium/Paywall. Se inicio con el Club MARCA (registro obligatorio en ciertos contenidos con incentivos de fidelizacion) como fase previa. El objetivo final es cerrar contenido bajo un muro de pago para monetizar la audiencia fiel, reduciendo la dependencia de formatos publicitarios intrusivos.

---

## Contexto y Justificacion

- **Erosion del trafico directo:** Se prevee una perdida progresiva de usuarios que llegan directamente a la web por nuevos habitos de consumo.
- **Crisis de fidelidad:** Descenso historico de usuarios recurrentes, atribuido a la gestion de la web y a la calidad percibida del contenido.
- **Impacto en KPIs:** Se asume una caida casi segura en el volumen total de paginas vistas. El exito del modelo depende de que el aumento en calidad editorial compense la perdida de inventario publicitario masivo mediante ingresos por suscripcion.

---

## 1. Vision Estrategica

Marca evoluciona de un modelo dependiente de la publicidad hacia un modelo de suscripcion.

- **Cierre de contenidos:** Proactivo y manual por el equipo editorial (no dinamico). Entre 10 y 20 contenidos diarios. El criterio es discrecional: se cierran los contenidos mas trabajados editorialmente y con mayor atractivo. No hay criterios objetivos definidos a fecha de mayo 2026.
- **Tipologias de contenido cerrado:** Noticias, opinion, directos, videos, cronicas y fotogalerias.
- **Exclusiones del muro de pago:** Resultados, estadisticas, calendarios y paginas estaticas.
- **Eliminacion del "Registro":** El modelo de contenido bajo registro desaparece. Los articulos con valor anadido pasan directamente al muro de pago.

---

## 2. Oferta y Planes de Suscripcion

- **Contenido Gratuito:** Acceso estandar (se mantiene).
- **Suscripcion de Contenido:** Acceso a los 10-20 articulos diferenciales diarios.
- **Pack Orbit:** Contenido gratuito + servicios Orbit.
- **Marca Pro:** Suscripcion independiente para eliminar publicidad (actualmente solo en App). Decidido que NO se integra como beneficio en los planes de MARCA Premium — son productos separados.
- **Precios:** Sin definir a fecha de mayo 2026.
- **Moneda:** Unicamente Euros (EUR), por limitaciones de la herramienta de cobros (Osone).
- **Promociones:** Codigos promocionales y periodos de trial en fase de definicion.

---

## 3. Experiencia de Usuario (UX)

- **Reduccion de publicidad:** Se evaluara eliminar formatos intrusivos (Sticky, Robapaginas, Taboola) en articulos de pago.
- **Muro de pago:** Modelo de previsualizacion (Lead-in) de ~450 caracteres para fomentar conversion.
- **Seccion exclusiva:** Portada o seccion dedicada con todo el contenido cerrado para suscriptores.
- **Landing de ventas:** Nueva pagina de aterrizaje para mostrar beneficios y permitir eleccion de plan (mensual/anual).

---

## 4. Ecosistema Tecnologico

- **Pasarela de pago:** Alenta. Presenta limitaciones en gestion dinamica de precios y productos; requerira despliegues tecnicos especificos en produccion. Existe debate tecnico con otras opciones de mayor coste.
- **App nativa:** Pagos obligatoriamente a traves de Google Play Store y Apple App Store.
- **AMP:** Excluido del modelo de pago en el lanzamiento. AMP se encuentra en fase de cierre en el sector.
- **Fidelizacion (MARCA Premium):** Gestionado actualmente por Jakala. Usuarios registrados tendran descuentos fijos; suscriptores tendran acceso a sorteos dinamicos. Requiere integracion tecnica para envio de informacion de autenticacion desde Marca a Jakala. Jakala ha demostrado ser poco eficaz. Reunion prevista semana del 12/05/2026 con Qualifio como alternativa. CMS propio tambien en evaluacion como solucion paralela.
- **Muro dinamico:** Se planteo la opcion de acceso tras N contenidos consumidos (ej. 5 articulos), aun en debate.

---

## 5. Retencion y Engagement

- **Newsletters:** Los suscriptores recibiran boletines diarios con avances y previas del contenido del dia.
- **Sinergia Discover:** El Paywall es el vehiculo para proteger y rentabilizar los proyectos de contenido original y exclusivo bajo el enfoque Estrategias Discover, diferenciando a MARCA de la competencia.

---

## Consideraciones de Implementacion

El equipo de desarrollo debe cumplir estrictamente con:

1. **Guia de Implementacion Analitica:** Seguimiento de conversiones y comportamiento.
2. **Requisitos SEO:** Asegurar que el cierre de contenido no afecte el posicionamiento organico.
3. **Flujos de Navegacion:** Optimizacion del proceso de compra y acceso para evitar fricciones.

---

## Owner

**Mei** — Product Manager de Ventas. Es la responsable del proyecto. Toda decision relevante requiere aprobacion de:
- **Negocio:** François y Gema Monjas
- **Producto:** Karen (Head of Product)

---

## Stakeholders

1. **Departamento de Negocio/Ventas (Suscripciones):** Responsables de la rentabilidad del modelo. Interlocutores: François y Gema Monjas.
2. **Equipo Editorial:** Encargados de la estrategia de contenido. Punto critico de friccion.
3. **Equipo Tecnico:** Desarrollo e integracion de plataformas de pago y gestion.

---

## Riesgos y Problematicas

- **Owner definido pero con dependencias multiples:** Mei es la owner del proyecto, pero toda decision relevante requiere alineacion con Negocio (François, Gema) y Producto. Esto puede ralentizar la toma de decisiones.
- **Paralisis ejecutiva:** La complejidad del desarrollo sin hoja de ruta clara reduce las probabilidades de exito.
- **Inconsistencia editorial:** Historicamente las iniciativas editoriales y de negocio no han estado alineadas.
- **Cultura de datos:** Dificultad persistente para obtener datos fiables para la toma de decisiones.
- **Resistencia al cambio:** El equipo editorial muestra dificultades para adoptar la estrategia correcta y no existe presion interna efectiva.
- **Dificultad estructural:** La ejecucion de estrategias complejas en la organizacion actual se percibe como un reto casi inalcanzable sin un cambio de modelo de gestion.

---

## Timeline

- **Historico:** Incumplimiento sistematico de hitos previos. Calendarios poco realistas en el pasado.
- **Estado actual:** No existe un timeline definido para la fase de Paywall. Se planteo lanzarlo antes del Mundial pero los retrasos lo mantienen en suspension.

---

## KPIs esperados

- Usuarios suscritos (conversion)
- Retencion de suscriptores
- Impacto en usuarios, paginas vistas y video views

---

## Analisis de Impacto Publicitario — Eliminacion de Formatos F, F2 y F3

**Fuente:** MarcaPremium_20260430_Content_type_WebApp.xlsx
**Fecha del analisis:** abril 2026
**Cohorte objetivo:** ~9,000 suscriptores estimados para el primer ano

El objetivo es cuantificar el impacto de eliminar los formatos **F (Interstitial)**, **F2 (Teads)** y **F3 (Seedtag)** para los suscriptores. Se usa como referencia el comportamiento de los usuarios del signwall, que representan el perfil mas cercano al futuro suscriptor.

### KPIs de navegacion (media mensual — Q1 2026)

| Plataforma | Usuarios Unicos (signwall) | PV por usuario/mes |
| :--- | :--- | :--- |
| Web | ~90,000 | ~226 PVs |
| App | ~7,500 | ~345 PVs |

El engagement en App es un 50% superior al de Web. La portada y los articulos concentran mas del 70% del peso de trafico, siendo los puntos criticos de exposicion a los formatos F, F2 y F3.

### Perfil demografico

- Grupo principal: **35-54 anos** (~45% del total de usuarios).
- Sesgo masculino marcado: >85% en App, ~62% en Web.
- En App, el trafico es predominantemente directo (90%), lo que facilita la retencion.
- En Web, mayor dependencia de buscadores, pero los usuarios de signwall muestran recurrencia superior a la media.

### Impacto por formato

| Formato | Ubicacion | Nivel de intrusividad | Efecto de la eliminacion |
| :--- | :--- | :--- | :--- |
| F (Interstitial) | Entrada / carga de pagina | Alto | Mejora significativa en velocidad de carga y experiencia (LCP) |
| F2 (Teads) | Outstream (dentro del texto) | Medio | Aumenta tiempo de permanencia al eliminar interrupciones visuales |
| F3 (Seedtag) | In-image / contextual | Bajo-Medio | Limpieza visual del contenido editorial |

### Estimacion de impresiones no servidas

Con una media de 345 PV/mes en App aplicada a los 9,000 suscriptores:

- **Mensual:** ~3.1 millones de PVs sin publicidad intrusiva.
- **Anual:** ~37 millones de impresiones de estos formatos no servidas a suscriptores.

### Consideraciones estrategicas

- La eliminacion de F y F2 es el argumento de venta mas fuerte para convertir al usuario registrado en suscriptor.
- Con 345 PVs/mes, el usuario Premium es un perfil de alto consumo y alta rentabilidad publicitaria. El precio de la suscripcion debe cubrir ese coste de oportunidad.
- Debe vigilarse si la perdida de ingresos por CPM (Teads/Seedtag) se compensa con el LTV del suscriptor.
- Tener en cuenta la estacionalidad: eventos como finales de mayo/junio disparan el PV y aumentan el valor del inventario no servido.
- **Pendiente:** calcular el coste de oportunidad con CPMs reales de cada formato para una valoracion economica exacta.
