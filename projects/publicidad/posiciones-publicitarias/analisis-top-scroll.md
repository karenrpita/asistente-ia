# Analisis formato Top Scroll — Impacto en CLS

**Estado:** En evaluacion  
**Fecha de pruebas:** Abril 2026  
**Portales analizados:** MARCA (marca.com/ajedrez.html) y EL MUNDO (elmundo.es/nosotras.html)

---

## Personas involucradas

| Nombre | Rol | Funcion en este proyecto |
|---|---|---|
| Karen Rodrigues | Head of Product | Coordinacion de producto; cuestion viabilidad combinacion Top + Mid Scroll |
| Jose Manuel Olano Daza | Director de Programatica | Impulsa implementacion comercial; gestiona pruebas en secciones (Baloncesto, Motor) |
| Alba Recio Sanson | Analista Tecnica | Metodologia de prueba, parametros de consentimiento para datos limpios en Lighthouse y PageSpeed |
| Luis Mariano Garcia Corral | IT | Identifico impacto critico inicial en CLS; alerto sobre valores superiores al umbral |
| Tamara Vazquez Alvarez | Tecnologia/IT | Responsable de reportar conclusiones finales en Jira |
| Carmen Sanchez Diaz | Negocio/Publicidad | Gestiona relacion con agencia externa Icreate; coordina activacion/desactivacion de pruebas |
| Gabriela Bolognese | (sin especificar) | Solicito reunion de 30 min para despejar dudas antes de decision de implementacion |

---

## Metrica clave: CLS (Cumulative Layout Shift)

El CLS mide el movimiento inesperado de elementos durante el ciclo de vida de una pagina.

- Bueno: <= 0.1
- Necesita mejora: 0.1 - 0.25
- Deficiente: > 0.25

Las pruebas se realizan sobre la carga inicial de la pagina. Los datos de CrUX (usuarios reales de Google) son mas representativos porque miden el CLS a lo largo de toda la interaccion del usuario.

---

## Resultados comparativos

| Portal / Dispositivo | Sin Top Scroll | Con Top Scroll | Conclusion |
|---|---|---|---|
| MARCA Desktop | 0.4 - 0.6 | 0.3 - 0.4 | Ligera mejora, sigue en rango deficiente |
| MARCA Mobile | 0.1 - 0.2 | 0.3 - 0.4 | Salta de bueno a critico |
| EL MUNDO Desktop | ~0.2 | ~0.4 | Empeoramiento del doble |
| EL MUNDO Mobile | 0.1 - 0.2 | 0.3 - 0.4 | Empeoramiento similar a MARCA |

---

## Herramientas de medicion utilizadas

**Tab Performance (Chrome DevTools):** Mide el CLS en condiciones locales. Sirve para comparativa rapida pero no refleja usuarios reales.

**Lighthouse (Chrome DevTools):** Analisis de rendimiento simulado desde el ordenador del analista. Util para diagnostico, pero los resultados varian entre pruebas.

**CrUX (Chrome User Experience Report):** Datos de usuarios reales recogidos por Google. Es la fuente mas fiable. Para MARCA/ajedrez.html existe reporte por URL. Para elmundo.es/nosotras.html solo hay datos a nivel de dominio (insuficientes datos de esa URL concreta).

**PageSpeed (pagespeed.web.dev):** Combina datos de CrUX (campo) con un analisis Lighthouse lanzado desde servidor. Limitation detectada: al lanzarse desde servidor con parametro gdpr-consent=_true, no carga publicidad, por lo que el CLS que reporta no refleja el impacto real del formato.

---

## Hallazgos clave

**Desktop:** El CLS es malo tanto con como sin Top Scroll en MARCA. En EL MUNDO el formato empeora significativamente un CLS que antes era aceptable.

**Mobile:** En ambos portales, el formato top-scroll lleva el CLS de niveles buenos (0.1-0.2) a niveles criticos (0.3-0.4). Sin embargo, los datos de CrUX para MARCA/mobile muestran valores mejores que las pruebas locales, probablemente porque los usuarios hacen scroll antes de que cargue la publicidad, lo que evita el desplazamiento de contenido visible.

**Formato Top + Mid Scroll + Display:** La combinacion de los tres formatos simultaneos es excesiva. Hay consenso tecnico en que perjudica gravemente la navegacion.

**Icreate (agencia externa):** Se ha detectado un salto visual en el renderizado que debe corregir la agencia.

---

## Solucion tecnica propuesta

Reservar una altura minima fija en el layout para el espacio publicitario, independientemente de si hay campana activa.

- Ventaja: elimina el desplazamiento de contenido cuando carga la publicidad.
- Inconveniente: deja un hueco vacio cuando no hay campana. Si se elimina ese hueco dinamicamente una vez cargada la pagina, vuelve a generar CLS.
- Conclusion: la solucion optima es mantener siempre el hueco reservado.

---

## Proximos pasos

- Reunion con Gabriela Bolognese (30 min) para despejar dudas antes de decision de implementacion definitiva.
- Decision sobre si activar el formato en Red Global.
- Si se aprueba: frecuencia propuesta de 2 campanas por semana.
- Correccion del salto visual de renderizado por parte de Icreate.

---

## Referencias externas

- Definicion y medicion de CLS: https://web.dev/articles/cls?hl=es-419
- CrUX MARCA/ajedrez.html: https://cruxvis.withgoogle.com/#/?view=visstability&url=https%3A%2F%2Fwww.marca.com%2Fajedrez.html
- Documentacion CrUX: https://developer.chrome.com/docs/crux?hl=es-419
- PageSpeed con Top Scroll (MARCA): https://pagespeed.web.dev/analysis/https-www-marca-com-ajedrez-html/ctnwgw90s7?form_factor=desktop
- PageSpeed sin Top Scroll (MARCA): https://pagespeed.web.dev/analysis/https-www-marca-com-ajedrez-html/caxdzwje6p?form_factor=desktop
- PageSpeed con Top Scroll (EL MUNDO): https://pagespeed.web.dev/analysis/https-www-elmundo-es-nosotras-html/ydzqctnpt5?form_factor=desktop
- PageSpeed sin Top Scroll (EL MUNDO): https://pagespeed.web.dev/analysis/https-www-elmundo-es-nosotras-html/vnxj0z4mss?form_factor=desktop
