# Prueba comparativa: YouTube vs Dailymotion en autoplay de portada

**Fecha de la prueba:** 14 de mayo de 2026

## Objetivos

- Comprobar que una misma campaña se trafica en portada con los players de YouTube y Dailymotion sin problema.
- Validar que el player de YouTube acepta frecuencia 1 (hasta ahora las campañas se ejecutaban siempre sin control de frecuencia).
- Con frecuencia 1 en YouTube, observar el PI de viewability para comparar el dato entre ambos players.

## Condiciones de la prueba

La prueba se realizó en el autoplay de portada con ambos reproductores activos el mismo día:

- **YouTube:** streaming en directo. Prueba activa aproximadamente **30 minutos**.
- **Dailymotion:** VOD. Prueba activa **15 minutos**, una vez finalizado el directo de YouTube.

El menor volumen en Dailymotion se explica por el menor tiempo de activación. Como referencia, Dailymotion puede servir ~55.000 impresiones/hora en condiciones normales.

> Dado el volumen reducido de impresiones, los resultados deben considerarse **orientativos**.

## Resultados

### Convivencia de players
Confirmado: una misma campaña puede traficarse en portada con ambos players sin incidencias.

### Frecuencia en YouTube
YouTube acepta frecuencia 1. Técnicamente no hay limitación para implementarla. Hasta la prueba, las campañas se ejecutaban sin control de frecuencia.

### Viewability y VTR (Completion Rate)

| Métrica | YouTube | Dailymotion |
|---|---|---|
| Viewability | 51% | 59% |
| VTR (Completion Rate) | 41% | 28% |

**Conclusiones:**
- Dailymotion muestra mayor viewability (59% vs 51%).
- YouTube presenta mejor VTR/Completion Rate (41% vs 28%).
