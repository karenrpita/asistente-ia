# Publicidad — MARCA

**Estado:** Activo  
**Responsable negocio:** José Manuel Olano (Director de Programática)  
**Responsable técnico middleware:** José María Millán (Ad Tech)

---

## Descripción

Estrategia, acuerdos y operativa de publicidad programática y directa en MARCA. Incluye el middleware publicitario propio, los acuerdos con partners externos y los formatos activos en la web.

---

## Problema transversal: opacidad y contratos sin validación de producto

El mayor problema del área de publicidad no es técnico ni comercial — es estructural:

1. **Sin reporting real.** Ninguno de los partners principales tiene un dashboard accesible para el equipo de SEO/Audiencias. Las decisiones se toman sin datos.
2. **Contratos firmados sin validación de producto.** Los acuerdos con Taboola incluyen obligaciones que dañan directamente la experiencia del usuario y la recirculación del tráfico. Nadie de Producto o SEO validó los contratos antes de firmar.
3. **Activaciones arbitrarias.** Formatos como el interstitial se activan y desactivan sin criterio ni comunicación al resto de equipos.

---

## Status 2026-04-16

- **STN Player:** incluido en MARCA España IP USA.
- **Caliente MX:** activo en edición México IP México. En desarrollo: edición España IP México.
- **Newsletter Real Madrid (abril):** se está vendiendo — formatos Mega, Logo y Banner.

---

## Partners activos

| Partner | Tipo | Acuerdo | Reporting | Archivo |
|---|---|---|---|---|
| Middleware propio | Stack publicitario | Interno (Ad Tech) | No | [middleware.md](middleware.md) |
| Seedtag | Display contextual | Directo (Olano) | Estimación | [seedtag.md](seedtag.md) |
| Taboola | Widget + feed | Directo (Olano) | No | [taboola.md](taboola.md) |
| Interstitial | Formato de pantalla completa | Publicidad | No | [interstitial.md](interstitial.md) |
| Amazon | Red publicitaria | — | — | Sin espacios propios |
| Google | Red publicitaria | — | — | Sin espacios propios |

---

## Formatos activos

| Formato | Tipo | Control | Estado | Problema principal | Archivo |
|---|---|---|---|---|---|
| Posiciones display propias | Display (300x250 / 300x600) | Directo (ad tech) | Activo — en debate | Espacios en blanco; 300x600 reduce viewability de slots siguientes | [espacios-en-blanco-reserva-300x600.md](publicidad-optimizacion-formatos/espacios-en-blanco-reserva-300x600.md) |
| Interstitial | Pantalla completa | Publicidad (sin protocolo) | Activo — activación arbitraria | Sin métricas; riesgo SEO en móvil; ningún freno desde Producto o UX | [interstitial.md](interstitial/interstitial.md) |
| Taboola — widget noticias relacionadas | Widget embebido en artículo | Indirecto (contrato directo Olano) | Activo | Posición antes del penúltimo párrafo; no pasa por middleware | [taboola.md](taboola/taboola.md) |
| Taboola — 30 cards al final | Feed de contenido recomendado | Indirecto (contrato directo Olano) | Activo | Destruye recirculación; 165 px obligatorios por contrato; genera círculo vicioso | [taboola.md](taboola/taboola.md) |
| Seedtag | Display contextual (IA) | Indirecto (contrato directo Olano) | Activo | Formatos exactos desconocidos; sin reporting | [seedtag.md](seedtag/seedtag.md) |
| Top Scroll | Nuevo formato — parte superior del scroll | Directo (ad tech) | Bloqueado — compromete CLS | Prueba en Ajedrez: impacto en Core Web Vitals. No activar sin resolver CLS | [topscroll/README.md](topscroll/README.md) |
| Patrocinios directos | Display directo / imágenes patrocinadas | Directo (comercial) | Activo — incidencia abierta (Oppo) | Calidad de imágenes en Xalok incompatible con patrocinadores de imagen premium | [patrocinios/README.md](patrocinios/README.md) |
| Middleware propio | Stack publicitario (header bidding) | Directo (ad tech — Millán) | Activo | Sin visibilidad del incremento real generado | [middleware.md](middleware/middleware.md) |

---

## Resumen del estado actual

**El problema no es de volumen, es de eficacia y control.**

- Demasiados formatos con escaso o nulo reporting. Las decisiones se toman sin datos.
- Los contratos con partners externos (Taboola, Seedtag) se firmaron sin validación de Producto, UX ni SEO. Algunas obligaciones contractuales dañan directamente las métricas de negocio.
- Formatos como el interstitial se activan sin protocolo, sin criterio y sin medición de impacto.
- Los espacios en blanco en posiciones display dañan la percepción de calidad y reducen la viewability de los slots siguientes, generando un efecto en cadena que lleva a meter más publicidad para compensar, lo que empeora la experiencia y reduce el engagement.
- El formato con mayor riesgo inmediato para las métricas es Taboola: destruye la recirculación y el contrato impide resolverlo sin renegociación.

**Criterio de actuación:** ningún formato se mantiene o activa sin responder si el balance neto (ingresos vs. impacto en usuarios, páginas vistas y recirculación) es positivo.

---

## Riesgos activos

- **Taboola destruye la recirculación.** Las 30 cards al final de las noticias bloquean la navegación continua, lo que reduce el tráfico interno y hace que MARCA incumpla los mínimos de tráfico contractuales con Taboola. Círculo vicioso.
- **Middleware sin visibilidad.** No se sabe si el incremento generado por el middleware es real ni de qué magnitud.
- **Interstitial sin control.** Se activa sin criterio desde el equipo de Publicidad. Nadie lo frena desde UX ni desde Producto.
