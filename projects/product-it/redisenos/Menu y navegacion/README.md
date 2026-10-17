# Fase 1 — Sistema de navegación y menú

**Estado:** En validación
**Última actualización:** 2026-10-01

---

## Contexto

Uno de los objetivos principales de cara a 2026 es rediseñar MARCA. El proyecto se divide en tres bloques: Cabecera y navegación, Portada y Contenidos. Este documento detalla el primero.

---

## Objetivo

Modernizar y renovar una cabecera y una navegación que han quedado obsoletas. Mejorar la navegabilidad para mejorar la experiencia y fidelización del usuario, el tiempo de permanencia en el sitio y el posicionamiento.

---

## Descripción

### Cabecera

**Mobile:**
- Únicamente hamburguesa e icono de login.
- Espacio reservado para destacar ofertas y campañas de Suscripción.
- Club MARCA se integra dentro del menú.
- Radio MARCA: se define en una fase posterior.

**Desktop:**
- Mismo menú que mobile (hamburguesa). Ancho: 1200px.
- Pendiente de definir si se sacan elementos del menú a la cabecera (en principio, no).
- Se mantienen hamburguesa, login y espacio para suscripción/ofertas.
- Selector de ediciones: preferiblemente dentro del menú.
- Portada de papel: se le dedicará un lugar diferente.
- Radio MARCA: se define en una fase posterior.

**Barra SEO:** actualmente en primera posición; se incluirá dentro del menú.

**Escudos:**
- Elemento de navegación muy valorado por editorial y usuarios.
- Se busca mayor presencia y versatilidad.
- Componente reutilizable en diferentes portadillas o posiciones de portada.
- Gestión autónoma de los escudos mostrados.
- Presencia en mobile.

**Componente de enlazado de competiciones:**
- Componente gestionable de forma autónoma.
- Permite navegar a competiciones destacadas según agenda o interés editorial.

**Tabs / chips:**
- En mobile (valorar chips). Pendiente de definir si tienen sentido en desktop.
- Especial valor a la tab de resultados.
- La tab de última hora puede perder sentido si se añade un widget en portada con noticias de última hora + "ver todo".
- Desarrollo en curso: ver ticket [REDIMARCA-68](#redimarca-68--enlaces-tipo-chip-backoffice) — enlaces tipo chip en cabecera, gestionables desde backoffice.

**Scroll:** simplificar la cabecera tanto en scroll up como en scroll down.

---

### Navegación principal — Hamburguesa

Mismo menú para desktop y mobile.

Escalable a ediciones internacionales (arquitectura distinta: competición en primer nivel en lugar de deporte/competición).

**Barra de navegación lateral al desplegar:**

- Menú con secciones y subsecciones agrupadas.
- Destacados: espacio editorial según agenda o interés.
- Resultados.
- Equipos (TBD en función de su presencia en portada).
- MARCA TV.
- Servicios (TBD): agenda, MARCA Entradas, hemeroteca, newsletters...
- Ediciones: selector de ediciones.
- Especial (TBD): espacio para enlazar páginas o contenidos fuera de la arquitectura principal.
- Buscador: TBD — posible proyecto independiente.
- Enlaces "no follow": posibilidad de incluir secciones o enlaces no indexables para acuerdos o necesidades editoriales.
- Acceso a cuenta de usuario: login/registro. Con usuario logueado: icono activo, acceso a Mi Cuenta y cerrar sesión.
- Radio MARCA: player que permita navegar por el site manteniendo activa la reproducción. Servirá también de enlace de entrada al site/sección de la radio.
- Suscripciones: CTA destacado para acceso a landing, proceso de suscripción, upgrade o presentación de ofertas.

---

### Migas y navegación secundaria

- Navegación específica para contenidos determinados (ejemplo: videoocts y MARCA TV).
- Gestión autónoma de las migas.
- Migas de portadillas de tag personalizables: posibilidad de elegir navegación existente (ej. Fútbol) o creada manualmente.
- Tabs/chips para navegación y recirculación dentro de contenidos — dependencia con Fase 3.
- Cabeceras de sección, página, equipo y jugador: TBD.

---

### Verticales

Afinar la personalización de verticales y secciones especiales para evitar los problemas actuales de consistencia.

---

## Alcance y entregables

Primera fase del rediseño: nueva cabecera y navegación aplicadas a todas las ediciones y todos los contenidos de MARCA.

Calendario de fases UX/UI y definición de producto: `Calendario Rediseño MARCA 2026.xlsx`

---

## Requisitos técnicos

- Gestión autónoma del menú.
- Gestión autónoma de migas/enlaces de navegación.
- Gestión autónoma del CTA de suscripciones.
- Gestión autónoma del componente de enlazado de competiciones.
- Requisitos SEO: TBD.
- Estilos con prioridad CWV.

---

## Ámbito

- Web mobile
- Desktop
- AMP

---

## Pendientes de definición

- Análisis de datos de analítica.
- UX Research: benchmark, heurístico, mapas de calor.
- Presentación de prototipos.
- Capa visual.
- Requisitos técnicos SEO.

---

## Referencias y prototipos

**Medios de referencia:**
- Deportivos internacionales: The Athletic, ESPN, Yahoo Sports, L'Equipe.
- Competencia española: AS.
- Generalistas: El País, The Guardian, NYT.

**Prototipo de partida:**
Prototipo de navegación trabajado hace tres años: [MARCA — Sistema de navegación (Figma)](https://www.figma.com/design/CsTHYHmx1cz9yQ6hKgEQIw/MARCA---Sistema-de-navegaci%C3%B3n?node-id=2389-70157&t=PUfKqIdKlOGOjPnk-1)

---

## REDIMARCA-68 — Enlaces tipo chip (Backoffice)

**Estado:** To Do
**Tipo:** Desarrollo — BackOffice

### Objetivo

Incorporar un módulo dinámico de enlaces rápidos con formato visual de "chips" o "píldoras" en la cabecera principal (header) de MARCA. Dirigen tráfico a contenidos de actualidad (portadillas, eventos especiales, tags) o a la sección de Resultados, mejorando la accesibilidad a contenidos clave durante la navegación.

### Alcance y dispositivos

- Desktop
- Mobile & Tablet
- AMP: a evaluar capacidad técnica de integración en cabecera.
- Aplica a todas las ediciones de MARCA (España, México, USA, English).

### Tipología de chips

**Chip de "Resultados":**
- Posición: primera posición a la izquierda de la lista de chips (movible si es necesario).
- Comportamiento: indicador de directos (badge) con contador numérico en tiempo real del total de eventos en directo (Live) activos, independiente del deporte, competición o sección en la que esté el usuario.
- La información de estado se actualiza mediante integración con el servicio de la API deportiva.
- Estilo visual: color distintivo fijo (fondo) para diferenciarlo de los chips editoriales.

**Chips editoriales (dinámicos):**
- Cantidad: mínimo 0, máximo 5-6 chips editoriales (además del chip fijo de Resultados).
- Edición rápida e independiente por perfiles específicos desde el backoffice, a cualquier hora.
- Refresco en tiempo real / inmediato en la web tras publicación en backoffice.
- Nombre/título: nombre de la sección/tag o nombre personalizado.
- URLs: soporta enlaces internos a portadillas o tags existentes, y enlaces sintéticos y/o externos configurados manualmente desde el editor.

### Comportamiento en navegación y UX/UI

- **Ubicación:** integrados dentro del Main Header, junto a menú hamburguesa y logotipo de MARCA.
- **Scroll (desktop/mobile):** tanto en scroll down como en scroll up, el header pasa a su versión reducida manteniendo visibles los chips, el logo a la izquierda y el menú hamburguesa.
- **Estados visuales (hover/focus/active):** pendientes de definir para Resultados y para chips editoriales.
- **Accesibilidad:**
  - Indicador de foco visible.
  - Navegación por teclado.
  - `aria-current="page"` en el chip de la sección en la que está el usuario.

### Requisitos SEO y rendering

- Nofollow / sponsored, igual que en el resto de Xalok.
- Enlaces reales: `<a href="URL">`, no `<button>`, ni `onclick`, ni `href="#"`.
- Deben venir en el HTML que llega del servidor, no inyectados después por JS.
- En móvil, todos los chips deben estar en el DOM aunque solo se vean al hacer scroll horizontal, sin carga diferida (Google indexa la versión móvil).
- **Medición con Marfeel:** en el atributo `data-mrf-recirculation` del contenedor, nunca como parámetros en la URL (`?utm_`, `?ref=chips`), para medir la interacción sin duplicar URLs.
- **URLs de destino limpias:** cada chip debe enlazar a la URL canónica final — responde 200 sin redirecciones intermedias, https, barra final igual que el resto del sitio, sin parámetros. Ideal que el CMS lo valide al guardar el chip.
- **Sin CLS:** altura reservada para la fila de chips desde el primer pintado.
- **Rendimiento:** sin JS que bloquee la carga.
- **Mismo target:** enlaces internos se abren en la misma pestaña, sin `target="_blank"`.

### Requisitos CMS / Backoffice

- Configurador de chips por edición (selector de edición de MARCA).
- Añadir / eliminar / reordenar chips (máximo 5-6 slots editoriales).
- Campos por chip:
  - Texto del chip (label).
  - URL de destino (sintética o enlace a contenido existente).
  - Atributo SEO: checkbox o dropdown (follow/nofollow).
- Botón de activación / publicación en tiempo real.

### Pendientes de definición

- Estados visuales hover/focus/active para ambos tipos de chip.
- Evaluación técnica de integración en AMP.

---

## Equipos implicados

- UX/UI
- SEO
- Analítica
- QA
- Producto
