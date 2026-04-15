# Problema: espacios en blanco en posiciones publicitarias

**Estado:** En debate  
**Afecta a:** Web, AMP, Apps  
**Fecha apertura:** 2026-04-15

---

## Descripcion del problema

En las posiciones publicitarias dentro de noticias aparecen espacios en blanco visibles que generan en el usuario la percepción de error o fallo en la página. Esto ocurre tanto cuando no carga ningún anuncio como cuando el creativo servido no coincide en tamaño con el slot reservado.

El problema afecta principalmente a posiciones cedidas a terceros (intext y similares). En los espacios que controlamos directamente, ad tech confirma que no hay problemas de tamaño en web y AMP — si los hubiera, depende de nosotros arreglarlo.

---

## Contexto tecnico

- El centrado vertical del creativo dentro del slot ya está implementado.
- El problema visual es consecuencia de la diferencia entre el tamaño del slot reservado y el del creativo servido.
- Afecta a web, AMP y apps, aunque con causas y soluciones distintas según el entorno.

### Lo que ya esta implementado en AMP

El espacio está bloqueado (tamaño fijo) para evitar CLS y que los elementos de la página no se muevan. Resuelve el problema de Core Web Vitals, pero mantiene el problema visual de los espacios en blanco cuando el creativo no ocupa el slot completo.

---

## Causas identificadas (input ad tech, 2026-04-15)

El problema en web se da principalmente en posiciones cedidas a terceros (intext). Al ceder el espacio con un tamaño acordado, ese tercero hace sus propias llamadas internas para rellenarlo, y puede servir creatividades de dimensiones distintas. Hay tres escenarios concretos:

### Causa 1: cascada de terceros sin sincronizacion de tamaños

Nuestro adserver devuelve un slot de dimensiones AxB (fijo). El tercero que lo gestiona hace sus propias llamadas para rellenarlo y puede servir una creatividad de dimensiones CxD. A su vez, ese tercero puede apoyarse en otro, y así sucesivamente. Los tamaños no siempre se reajustan hacia arriba en toda la cadena. Solucionarlo requeriría una sincronización no solo con nuestro tercero directo, sino con todos los niveles inferiores de la cascada.

### Causa 2: recargas con cambio de formato

Cuando termina un vídeo, se produce una recarga que puede servir una posición de display con dimensiones distintas a las del vídeo. Las dimensiones de display no coinciden con las de vídeo, lo que genera espacios en blanco, a veces vertical, a veces horizontal.

### Causa 3: creatividades modificadas automaticamente

En algunos casos, una creatividad de dimensiones AxB es transformada de forma automática a dimensiones CxD. El espacio sobrante queda "relleno" técnicamente, pero el usuario lo ve como blanco.

### Por que el anuncio no puede redimensionar su propio slot

Técnicamente es posible, pero requiere soporte en toda la cascada de tecnologías del tercero. El obstáculo principal es el **safe frame**: los anuncios deben servirse dentro de un entorno aislado por seguridad. Desde dentro de ese entorno no es sencillo modificar la página que lo contiene, precisamente para evitar que un anuncio malicioso pueda alterar cualquier elemento de la página, no solo su propio slot. En apps, la complejidad aumenta considerablemente.

---

## Impacto en viewability y densidad publicitaria

Reservar un slot de 300x600 empuja hacia abajo el contenido y los slots publicitarios siguientes. Esto reduce de forma inevitable la viewability del siguiente slot, ya que el usuario tiene que hacer más scroll para llegar a él. Para compensar esa pérdida de viewability, la tendencia es meter más unidades publicitarias en la página, lo que empeora la experiencia de usuario y puede entrar en conflicto con las políticas de densidad publicitaria de Google.

Es un efecto en cadena: slot más grande → menor viewability del siguiente → más publicidad para compensar → peor experiencia → menor engagement → menos páginas vistas.

---

## Por que no se puede escalar el slot dinamicamente

Escalar el espacio de reserva en función del anuncio que entra genera dos problemas graves:

1. **Recargas y saltos de página** — Imposibilitan una lectura continua y fluida para el usuario.
2. **Impacto en CLS (Cumulative Layout Shift)** — Métrica crítica de Core Web Vitals de Google. Un CLS elevado penaliza el posicionamiento SEO y la valoración de la página por parte de Google.

---

## Opciones en evaluacion

> Las opciones 1-4 aplican a los espacios que controlamos directamente. Para posiciones cedidas a terceros, la solución pasa por negociación contractual o técnica con el tercero (ver opción 5).

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

### Opcion 5: Negociar con el tercero el tamaño exacto del creativo servido
Para posiciones cedidas, la solución de raíz pasa por exigir contractual o técnicamente que el tercero respete el tamaño acordado del slot en toda su cascada interna.

- Pros: elimina la discrepancia de origen; no requiere cambios en nuestra infraestructura
- Contras: depende de la voluntad y capacidad técnica del tercero; puede ser complejo de implementar en cascadas con múltiples niveles

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

> Cualquier dato adicional sobre impacto en UX o ingresos publicitarios será bienvenido. Si alguien del equipo o de ad ops tiene benchmarks, añadirlos aquí.

---

## Decisiones tomadas

> Ninguna tomada aún. Este documento recoge el estado del debate.

---

## Proximos pasos

- Identificar qué posiciones concretas están cedidas a terceros y cuáles controlamos directamente
- Para posiciones propias: decidir solución técnica con IT (opciones 1-4)
- Para posiciones cedidas: abrir conversación con los terceros para exigir respeto del tamaño acordado
- Revisar manualmente cómo resuelven este problema AS, El Mundo u otros medios de referencia
- Validar con IT el impacto real en CLS de las opciones que implican cambio de tamaño
- Decidir si se aborda primero web, AMP o apps (AMP ya tiene CLS resuelto; web es la prioridad)
