# Top Scroll

**Estado:** En evaluación activa — decisión final pendiente para el jueves 2026-05-14
**Última actualización:** 2026-05-12

## Descripción

Nuevo formato publicitario Top Scroll: se muestra en la parte superior de la página, por encima del menú, antes de que el usuario haga scroll. Se ha evaluado junto con el formato Mid Scroll en los entornos de MARCA y EL MUNDO.

---

## Responsables

| Nombre | Rol en el proyecto |
|---|---|
| Jose Manuel Olano | Director de Programática — lidera la activación de campañas y coordinación técnica |
| Karen Rodrigues | Head of Product — supervisa impacto en UX y CLS |
| Carmen Sánchez Díaz | Coordina ventanas de prueba y comunicación entre Negocio y Tecnología |
| Javier Rodríguez Diez | Implementación en MARCA, gestión de requisitos técnicos |
| Myriam Aguado de Corral | Enlace entre publicidad programática y rendimiento |

---

## URLs analizadas

- MARCA: https://www.marca.com/ajedrez.html
- EL MUNDO: https://www.elmundo.es/nosotras.html

---

## Análisis técnico — CLS (Cumulative Layout Shift)

El CLS es la métrica más afectada. Mide el movimiento inesperado de elementos en la página durante su ciclo de vida. Valores buenos: ≤0.10. Valores deficientes: >0.25.

### MARCA — Portadilla Ajedrez

| Escenario | Desktop CLS | Mobile CLS |
|---|---|---|
| Sin Top Scroll (display tradicional) | 0.4 – 0.6 | 0.1 – 0.2 |
| Con Top Scroll | 0.3 – 0.4 (picos 0.6) | 0.3 – 0.4 |

- En desktop, curiosamente, el formato Top Scroll produce un CLS ligeramente menor que la publicidad display anterior.
- En mobile, el Top Scroll empeora los valores respecto al estado sin el formato.
- Los datos de CrUX (usuarios reales, Google) para la portadilla de Ajedrez muestran que el CLS en desktop ha sido malo desde 2025, independientemente del formato. En mobile, el CLS real es mejor porque Google mide toda la interacción del usuario, no solo la carga inicial: si el usuario hace scroll antes de que cargue el anuncio, el elemento no impacta el viewport y el CLS sube menos.

### EL MUNDO — Portadilla Nosotras

| Escenario | Desktop CLS | Mobile CLS |
|---|---|---|
| Sin Top Scroll | 0.2 – 0.4 (cercano a 0.2) | 0.1 – 0.2 |
| Con Top Scroll | 0.3 – 0.4 (picos 0.6) | 0.3 – 0.4 |

- No hay datos de CrUX específicos para esta URL. Google solo muestra datos del dominio origin (elmundo.es). El comportamiento esperado es similar al de la portadilla de Ajedrez.

### Lighthouse (herramienta de laboratorio)

- Las mediciones de PageSpeed/Lighthouse vía servidor no reflejan el impacto real del Top Scroll porque el servidor no espera a que cargue la publicidad.
- Los datos de CrUX (campo) son más fiables para este análisis.

---

## Cronología de pruebas

| Fecha | Evento |
|---|---|
| 14–16 abril 2026 | Pruebas iniciales activadas en Baloncesto, Motor y Polideportivo de MARCA |
| 28 abril 2026 | Se identifica necesidad de aislar análisis de carga limpia (con/sin formatos) |
| 29 abril 2026 (10:00–12:00) | Ventana crítica: desactivación de formatos para análisis comparativo en Ajedrez y Nosotras |

---

## Riesgo principal

- CLS elevado penaliza posicionamiento SEO y la evaluación de Core Web Vitals por Google.
- La combinación de Top Scroll + Mid Scroll + Display simultáneos se considera excesivamente intrusiva. No deben activarse los tres a la vez.

---

## Reunión 2026-05-12 — Decisiones y bloqueos

### Participantes
- **Ricky** — SEO/técnico. Foco en CLS y reserva de espacios.
- **Gaby** — Validez de datos y representatividad de los escenarios de prueba.
- **Marta / Cristina** — Tráfico y Producto. Implementación técnica y comercialización.
- **Fran** — Experimentación y mediciones locales.

### Bloqueo principal: "blanqueo" de laterales
Hay discrepancia sin resolver entre la postura comercial y la técnica:
- **Comercial:** quiere mantener Skies + Robapáginas activos junto al Top Scroll para asegurar impresiones.
- **Técnico/Producto:** la interpretación original era que Top Scroll sustituye todos los demás formatos para limpiar la página.

Este punto debe resolverse antes del jueves.

### Hallazgo técnico confirmado
Los datos de campo (CrUX) no muestran degradación tan grave como las pruebas locales. Razón: si el usuario hace scroll antes de que cargue el anuncio, el desplazamiento ocurre fuera del viewport y Google penaliza menos. Esto valida que las pruebas locales sobreestiman el impacto real.

### Problema de representatividad de datos
Las pruebas de los últimos 30 días están contaminadas porque Top Scroll y Midscroll han convivido simultáneamente. Los datos en Noticias (donde está el tráfico real) aún no se han medido de forma limpia.

---

## Próximos pasos y decisiones pendientes

| Acción | Responsable | Plazo |
|---|---|---|
| Prueba en Noticias: Top Scroll + Laterales + Roba | Cristina / Tráfico | Inmediato |
| Página de pruebas abierta que replique Portada | Fran / equipo técnico | 48h (antes del jueves) |
| Evaluar escenario 1 (solo Top Scroll) vs. escenario 2 (Top Scroll + laterales + roba) | Todo el equipo | Jueves 2026-05-14 |
| Explorar si el Mega puede ir siempre encima de la cabecera (hueco fijo) | Ricky | Pendiente evaluación |

**Nota:** El proyecto lleva 4 meses de retraso (lanzamiento previsto para enero 2026). La reunión del jueves debe cerrar la decisión definitiva antes de la salida masiva al mercado.

---

## Conclusión técnica

Cualquier elemento que se cargue tras la carga inicial y mueva contenido inesperadamente generará CLS. La única solución que evita el CLS es reservar el espacio de antemano con altura fija, independientemente de si hay campaña activa. Quitar o añadir ese hueco en tiempo de ejecución siempre generará CLS.
