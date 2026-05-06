# Loteria de Navidad 2025 — MARCA

**Descripcion:** Cobertura editorial y producto digital del sorteo de la Loteria de Navidad 2025. Migracion a Xalok. Replica del especial del año pasado, sin el Comprobador de Pedrea.

**Estado:** En desarrollo
**Ultima actualizacion:** 2026-05-06
**Responsable de producto:** Karen Rodrigues Pita
**Jiras:**
- https://rcsuejira.atlassian.net/browse/NP-793
- https://rcsuejira.atlassian.net/browse/UXPRODUCTO-482

---

## Contexto

Se replica el especial del año anterior con una excepcion: este año no se incluye el Comprobador de la Pedrea.

CMS destino: Xalok.

URL de referencia de la portadilla: https://www.marca.com/loteria/loteria-navidad.html

---

## Componentes y prioridades

| Componente | Prioridad | Estado | Fecha objetivo |
|---|---|---|---|
| Portadilla | — | Hecho | — |
| Localizador de numeros | 1 | Pendiente | Finales septiembre |
| Listado de administraciones | 2 | Pendiente | Principios octubre |
| Comprobador de decimos | 3 | Pendiente | Principios octubre (desactivado) |
| Widget Modulo de Premios | — | Pendiente | — |
| Noticias automaticas | — | Pendiente | — |

---

## Detalle por componente

### Portadilla

- Misma estructura que el año pasado
- URL: https://www.marca.com/loteria/loteria-navidad.html

---

### Localizador de numeros (Prioridad 1)

**Estatica:**
- H1: Buscar Loteria Navidad 2025
- URL: https://www.marca.com/loteria/loteria-navidad/buscar-numero.html
- Estructura: H1 + WIDGET localizador + H2 + texto
- Textos: en definicion por SEO
- Fecha objetivo: finales de septiembre

**Modulo de premios en la estatica:**
- Desktop: columna derecha
- Mobile: al final de la estatica

**Publicidad:** posiciones habituales (Mega, Roba, Sky, sticky, etc.)

**Apps:** tab dentro de la portadilla → enlaza a la estatica via Webview

---

### Comprobador de decimos (Prioridad 3)

**Estatica:**
- H1: Comprobar Loteria de Navidad 2025
- URL: https://www.marca.com/loteria/loteria-navidad/comprobar-loteria.html
- Estructura: H1 + WIDGET comprobador de decimos + H2 + texto
- Textos: en definicion por SEO
- Fecha objetivo: principios de octubre, desactivado

**Modulo de premios en la estatica:**
- Desktop: columna derecha
- Mobile: al final de la estatica

**Mensajes de respuesta del comprobador:** Sorteo no iniciado / Introducir decimo / Completar importe / Numero Premiado / Numero no premiado / Error

**Publicidad:** posiciones habituales (Mega, Roba, Sky, sticky, etc.)
- Mensaje personalizado con logo y link (nofollow) al anunciante en el comprobador, diferenciado por premiado y no premiado
- Taggeado para diferenciar publicidad de premiado y no premiado
- Puede ser patrocinado

**Apps:** tab dentro de la portadilla → enlaza a la estatica via Webview

---

### Listado de Administraciones (Prioridad 2)

**Estatica:**
- URL: https://www.marca.com/loteria/loteria-navidad/comprar-loteria-administracion.html
- Listado completo de las 52 provincias con links al resto
- Cada provincia enlaza a una noticia, igual que el año pasado (ejemplo: https://www.marca.com/loteria/loteria-navidad/2023/11/30/6515afaa46163fbd098b45e1.html)
- Las noticias de provincia las hace SEO

**Fecha objetivo:** principios de octubre (cuando empiezan a subir las busquedas). El año pasado se publico el 12 de diciembre por problemas con AMP.

**Modificaciones respecto al año pasado:**
- Dentro de cada noticia, poder incluir la tabla al principio y no al final (el año pasado solo podia meterse como sumario y el usuario no llegaba abajo)
- Mejorar el enlazado en la miga
- En mobile: incluir tabs de navegacion

**Jiras de referencia 2023:**
- http://rcsuejira.atlassian.net/servicedesk/customer/portal/3/OPS-33708
- http://rcsuejira.atlassian.net/browse/LOTERIAS-366

**Datos estructurados:** Organization, BreadcrumbList, Event. Textos en definicion de SEO.

**Publicidad:** posiciones habituales (Mega, Roba, Sky, sticky, etc.)

**Apps:** tab dentro de la portadilla → enlaza a la estatica via Webview

---

### Widget Modulo de Premios

Presente en: Portada, Portadilla, Noticia, Directo y paginas estaticas.

**Posiciones:**

| Superficie | Desktop | Mobile |
|---|---|---|
| Portada | Bloque del carrusel de resultados actual (cuidado con no cargarse el cintillo de mkt) + bloque nuevo antes del flex List AD "No deportivo" | Mismo bloque visible |
| Portadilla | Tras el Mega | Tras las tabs de secciones |
| Noticias / Directo | Sidebar, tras el Roba A | Previo al modulo de Taboola |
| AMP | — | Previo al modulo de Taboola |

Ejemplo de referencia: https://www.marca.com/loteria/loteria-navidad/2023/12/27/658c190f22601d92388b4575.html

**Enlace al directo:** debe incluirse en el widget. La URL del directo debe poder cambiarse de forma agil y sin dependencia de tecnologia (Google Docs similar al de años anteriores).

**Links dentro del modulo:**
- El Gordo
- Segundo premio
- Tercer premio
- Cuartos premios
- Quintos premios
- Directo
- Terminaciones y reintegros
- Los demas premios: noticias automaticas
- Noticias de la Portadilla Loteria Navidad

**Publicidad:** el modulo va acompañado de un include en la parte superior.

---

### Widget Comprobador de Decimos

Compuesto por: Titulo patrocinable + modulo de premios + Comprobador patrocinable (si no se vende uno de los dos patrocinios del include, hay que quitar la llamada).

**Posiciones:** Portada, Portadillas, Noticia, Directos.

Puede arrastrarse desde el CMS (UEdit, Talea y Xalok).

**Incluir enlace al directo** igual que el año pasado: https://www.marca.com/loteria/loteria-navidad/2024/12/22/6767f338f49425d14de899af-directo.html

**Versiones necesarias:** Desktop, Mobile, AMP (noticias y directos)

**Posiciones por superficie:**
- Portada desktop y mobile: debajo del modulo de premios
- Noticias y directos (desktop, mobile, AMP): tras la firma del autor

Ejemplo de referencia: https://www.marca.com/loteria/2022/12/22/63a42a2a46163f7c748b4594.html

**Publicidad:**
- Mensaje personalizado con logo y link (nofollow) al anunciante, diferenciado por premiado y no premiado
- Taggeado para diferenciar la publicidad de premiado y no premiado
- Puede ser patrocinado

**Apps:**
- En portadilla: ocupa la posicion de la tab de "localizador" → abre la pagina estatica via Webview
- En portada: boton que redirige a https://www.marca.com/loteria.html → Webview

---

### Noticias automaticas

- H1: XXXX, Pedrea de Loteria de Navidad 2025 | Numero premiado, donde ha tocado y como cobrar los 100 euros
- Estructura: H1 + texto SEO + H2 + video + texto seo + H2 + imagen + texto seo
- Textos en definicion de SEO
- Modificacion: que salgan segun lleguen los datos desde Loterias (el año pasado salieron horas despues y gran parte no indexaron)
- Deben verse en desktop, mobile, AMP y APPs

Jira de referencia 2023: http://rcsuejira.atlassian.net/browse/LOTERIAS-368

---

## Lo que NO se hace este año

- Comprobador de la Pedrea (referencia del año pasado: https://www.marca.com/loteria/loteria-navidad/comprobar-pedrea-numeros.html)

---

## Fechas clave

| Hito | Fecha objetivo |
|---|---|
| Localizador de numeros operativo | Finales septiembre |
| Comprobador de decimos publicado (desactivado) | Principios octubre |
| Listado de administraciones operativo | Principios octubre |
| Sorteo de Loteria de Navidad | 22 diciembre 2025 |

---

## Ambito tecnico

- Web desktop
- Web mobile
- AMP
- Apps (la mayoria de estaticas via Webview)
- CMS: Xalok

---

## Datos estructurados

Presentes en las estaticas: Organization, BreadcrumbList, Event.

---

## Equipos implicados

| Equipo / Area | Responsabilidad |
|---|---|
| Producto | Coordinacion general |
| SEO | Textos de estaticas, noticias de provincia, datos estructurados |
| Tecnologia | Desarrollo de widgets y estaticas |
| Editorial | Noticias automaticas y contenido |
| Publicidad | Patrocinios y posiciones publicitarias |
| Apps | Webviews y tabs en portadilla |
