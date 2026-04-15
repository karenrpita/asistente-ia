# Delorean

**Descripción:** Unificación de plantillas antiguas de MARCA para resolver la fragmentación tecnológica acumulada desde 2012.

**Estado:** Activo — reiniciado gracias al proyecto UFO. Sin deadline. Proyecto con ~2 años de retraso.

## Problema que resuelve

MARCA es una web tecnológicamente fragmentada. El contenido vive en múltiples CMS según la época en que fue publicado:

- Hasta 2012: CMS original
- 2012–2016: segundo CMS
- 2016–2020: tercer CMS
- 2020–actualidad: CMS más recientes

Cada capa tiene sus propias plantillas. Las más antiguas no sirven publicidad correctamente, no tienen integración con GfK, y en general no cumplen los estándares actuales técnicos ni de negocio.

## Objetivo

Unificar todas las plantillas bajo un estándar común. Afecta a todas las tecnologías y productos (web, app, CMS).

## Naturaleza del proyecto

Deuda técnica de largo recorrido (~2 años de retraso). Es un proyecto de SEO e infraestructura, no de producto visible. El impacto no es inmediato sino acumulativo y se mide en salud de la web.

## KPIs y medición

No hay KPIs de negocio directos (usuarios, PV, video views) asociados directamente. El éxito se mide en:

- **Proyecto de salud de web** — métricas técnicas de las URLs afectadas
- **Publicidad** — reporting de rendimiento publicitario en páginas migradas (pedir a ad tech)
- **Datos históricos** — acceso a datos de audiencia de páginas antiguas (GfK) una vez migradas
- **Tráfico a URLs antiguas** — monitorizar peticiones a esas URLs para confirmar correcta redirección o indexación

## Dependencias

- **UFO** — API de ingesta de Unidad Editorial. Es el proyecto que ha reactivado Delorean.
- **Xalok** — nuevo CMS al que apunta la migración de contenidos

## Personas involucradas

- Equipo IT (responsable técnico)
- Equipo SEO (responsable de criterios y validación)

## Riesgos y alertas

- Sin deadline definido: riesgo de que vuelva a quedar bloqueado o desprioritizado
- Requiere coordinación activa con IT para no perder impulso ahora que UFO lo ha reactivado
- Las páginas antiguas pueden estar generando ingresos publicitarios bajos sin que haya datos claros — pedir reporting antes de migrar para tener baseline
