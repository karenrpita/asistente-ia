# Fase 1 — Sistema de navegación y menú

**Estado:** En validación
**Última actualización:** 2026-05-06

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

## Equipos implicados

- UX/UI
- SEO
- Analítica
- QA
- Producto
