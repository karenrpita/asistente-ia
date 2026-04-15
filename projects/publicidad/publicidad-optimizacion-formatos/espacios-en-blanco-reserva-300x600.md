# Problema: espacios en blanco en posiciones publicitarias

**Estado:** En debate  
**Afecta a:** Web, AMP, Apps  
**Fecha apertura:** 2026-04-15

---

## Descripcion del problema

En las posiciones publicitarias dentro de noticias, se reserva un espacio de 300x600 px anticipando la llegada de un formato display o roba de ese tamaño. Sin embargo, lo que se recibe con frecuencia son creatividades de 300x250.

El resultado es un espacio en blanco visible arriba y abajo del anuncio (el creativo queda centrado verticalmente en el slot de 300x600), lo que genera en el usuario la percepción de error o fallo en la página.

Adicionalmente, cuando no carga ningún formato publicitario, el hueco reservado de 300x600 queda completamente en blanco en mitad de la lectura.

---

## Contexto tecnico

- El centrado vertical del creativo dentro del slot ya está implementado a nivel técnico.
- El problema visual es consecuencia directa de la diferencia de tamaño entre el slot reservado (300x600) y el anuncio servido (300x250).
- Esto ocurre en los tres entornos: web, AMP y apps.

### Lo que ya esta implementado en AMP

El espacio está bloqueado (tamaño fijo) para evitar CLS y que los elementos de la página no se muevan. Esto resuelve el problema de Core Web Vitals en AMP, pero mantiene el problema visual de los espacios en blanco cuando el creativo no ocupa el slot completo.

---

## Por que no se puede escalar el slot dinamicamente

Escalar el espacio de reserva en función del anuncio que entra genera dos problemas graves:

1. **Recargas y saltos de página** — Imposibilitan una lectura continua y fluida para el usuario.
2. **Impacto en CLS (Cumulative Layout Shift)** — Métrica crítica de Core Web Vitals de Google. Un CLS elevado penaliza el posicionamiento SEO y la valoración de la página por parte de Google.

---

## Opciones en evaluacion

> Esta sección se irá completando conforme avance el debate.

### Opcion 1: Placeholder visual con fondo neutro
Mostrar un fondo neutro (gris claro, color corporativo, etc.) en el espacio sobrante para que no parezca un error. No elimina el espacio en blanco, pero cambia la percepción del usuario.

- Pros: sin impacto en CLS, sin saltos de página, implementación sencilla
- Contras: sigue ocupando espacio sin contenido útil; puede seguir pareciendo raro

### Opcion 2: Reducir la reserva al tamaño minimo esperado (300x250)
Reservar por defecto el slot más pequeño esperado y expandir si llega un formato mayor, aceptando el riesgo de CLS.

- Pros: menos espacio vacío visible en el caso más frecuente
- Contras: genera CLS cuando entra un 300x600; penaliza Core Web Vitals

### Opcion 3: Aspect ratio contenedor con min-height
Reservar un contenedor con min-height de 300x250 y permitir que crezca si llega un formato mayor, con transición suave.

- Pros: reduce el espacio vacío en el caso habitual; la transición puede suavizar el CLS percibido
- Contras: no elimina el CLS si el anuncio es más grande; requiere validación técnica del impacto real en la métrica

### Opcion 4: Collapse del slot si no carga publicidad
Si no entra ningún formato, colapsar el slot a 0 px en lugar de dejar el hueco de 300x600.

- Pros: elimina el espacio en blanco cuando no hay publicidad
- Contras: el colapso en sí genera CLS; hay que implementarlo con cuidado (por ejemplo, solo colapsar tras timeout definido)

### Opcion 5: Reservar solo el tamaño del formato solicitado (bidding)
Coordinar con el equipo de ad ops para que el tamaño del slot reservado corresponda exactamente al formato que se está pujando.

- Pros: elimina la discrepancia de origen
- Contras: requiere coordinación con ad ops y posible cambio en la configuración del header bidding

---

## Referencia: como lo resuelven otros medios

### Netzwelt (Alemania) — caso documentado

Medio digital de referencia con el mismo problema: slots multisize 300x250/300x600 con CLS alto.

Solución aplicada:
- Reserva de tamaño fijo por slot (el mínimo esperado)
- Eliminación de slots multisize en las posiciones superiores

Resultados:
- +27% páginas vistas
- Viewability por encima del 75%
- +18% de ingresos publicitarios

Conclusión clave: mejorar el CLS no redujo los ingresos publicitarios, los aumentó. Es el argumento directo para ad ops si hay resistencia interna.

Fuente: https://web.dev/case-studies/netzwelt

### Washington Post — infraestructura propia

Desarrollaron un wrapper open source propio (ArcAds) sobre Google DFP para gestionar el tamaño de los slots antes del pintado en pantalla. Confirma que los grandes publishers resuelven este problema a nivel de infraestructura, no con parches visuales.

Fuente: https://github.com/washingtonpost/ArcAds

### Google Publisher Tag — guia oficial

Google tiene una guía técnica oficial sobre cómo minimizar layout shift en slots publicitarios. Es la referencia que IT debería usar como punto de partida para la implementación.

Fuente: https://developers.google.com/publisher-tag/guides/minimize-layout-shift

### Medios españoles

No hay casos documentados públicamente de medios españoles (AS, El Mundo, etc.). Habría que revisar manualmente cómo lo están resolviendo.

---

## Decisiones tomadas

> Ninguna tomada aún. Este documento recoge el estado del debate.

---

## Proximos pasos

- Revisar manualmente cómo resuelven este problema AS, El Mundo u otros medios de referencia
- Confirmar con IT si están usando Prebid.js u otro wrapper de header bidding (determina viabilidad de la opción 5)
- Validar con IT el impacto real en CLS de las opciones que implican cambio de tamaño
- Decidir si se aborda primero web, AMP o apps (AMP ya tiene CLS resuelto; web es la prioridad)
