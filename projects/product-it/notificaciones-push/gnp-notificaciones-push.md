# GNP - Nuevo sistema de notificaciones Push

## 1. Identificación de la necesidad

- **Las ediciones internacionales no pueden enviar push:** la herramienta actual (desarrollo in-house antiguo) solo permite enviar notificaciones a la edición MARCA España. MARCA USA, MARCA English y MARCA México no tienen canal push propio, aunque su cobertura deportiva es distinta (por ejemplo, NFL en MARCA English). Hoy, o no les llega nada o les llega contenido de España que no les interesa. KPI afectado: usuarios y páginas vistas de las ediciones internacionales.
- **No se mide el rendimiento de las push:** de cada envío solo se sabe el número de envíos. No hay datos de cuántos dispositivos lo reciben, cuántos lo abren ni qué consumen después. Con un volumen de 20 o más push al día en España, no se puede saber qué funciona ni optimizar. KPI afectado: usuarios, páginas vistas y video views.
- **Formatos limitados:** las push son de texto. Sin imagen ni GIF, las notificaciones compiten peor en la pantalla del móvil contra las de otros medios y apps. KPI afectado: usuarios (retorno a la app) y páginas vistas.
- **Riesgo técnico:** la herramienta actual está obsoleta y hay que retirarla. Mientras siga en uso, cualquier fallo deja sin push manuales ni alertas automáticas (goles y resultado final), que son un motor de retorno a la app. Si se cambia de sistema sin migrar bien los tokens y las suscripciones, se pierde la base de usuarios con opt-in, y en iOS el permiso no se puede volver a pedir libremente.

## 2. Objetivo

- **Envío segmentado por edición desde una sola app:** con el mismo APK en Android y la misma compilación en iOS, cada una de las 4 ediciones (MARCA España, MARCA USA, MARCA English y MARCA México) envía sus push solo a los usuarios de esa edición. Cada redacción envía las suyas. Responde a la necesidad 1.
- **Medición completa y con histórico:** cada push tiene datos de envío, recepción, apertura y del tráfico posterior (páginas vistas, video views, sesión) en tiempo casi real. Se consultan en un dashboard y en Looker Studio con histórico para analizar qué funciona. Responde a la necesidad 2.
- **Rich push y deep links:** push de texto, con imagen y con GIF. Todas pueden llevar un enlace a cualquier destino de la app (noticia, directo, páginas de datos) o a un destino externo (app de Radio MARCA, app de Fantasy MARCA, cualquier web o app de terceros). Responde a la necesidad 3.
- **Retirar la herramienta antigua sin perder base ni servicio:** migrar todos los tokens y las suscripciones por tipología sin pedir de nuevo el opt-in, y mantener sin interrupción las alertas automáticas de goles y resultado final. Responde al riesgo.
- **Frenos conocidos:**
  - **GIF en Android:** las notificaciones nativas de Android no animan GIF. Se intenta la animación, y si no es viable se muestra el primer fotograma. En iOS se muestra animado.
  - **Permiso de notificaciones:** iOS y Android 13 o superior exigen permiso explícito. Si se pierde un token en la migración, recuperar a ese usuario depende de que vuelva a aceptar. Se sortea migrando los tokens existentes, sin pedir de nuevo el permiso.
  - **Atribución:** la decisión sobre la herramienta de atribución de la app sigue abierta (Adjust, AppsFlyer o Singular, ver [atribución](../app-general/atribución/README.md)). El tracking de las push no depende de esa decisión: se hace con parámetros propios en cada deep link.

## 3. Descripción

La definición se plantea como desarrollo propio del equipo de Aplicaciones de IT. Propuesta de arquitectura: un backoffice y un backend propios para el envío, con Firebase Cloud Messaging (FCM) como canal de entrega para Android e iOS (sobre APNs). FCM no tiene coste de envío y lo mantiene Google. Así se evita volver a depender de un sistema de transporte propio que se quede obsoleto. Si se prefiere contratar, las alternativas de mercado están en el apartado 7, y este GNP sirve como pliego de requisitos para evaluarlas.

El proyecto se divide en 5 fases:

- **Fase 1 - Auditoría y diseño técnico:** inventario de la herramienta actual y diseño de la nueva arquitectura.
- **Fase 2 - Backend y backoffice de envío:** herramienta de envío manual, programado y automático segmentada por edición.
- **Fase 3 - Integración en las apps iOS y Android:** registro por edición, rich push, deep links y eventos de recepción y apertura.
- **Fase 4 - Medición y dashboard:** recogida de eventos, histórico, dashboard en la herramienta y Looker Studio.
- **Fase 5 - Migración, convivencia y retirada de la herramienta antigua:** paso de usuarios, envío en paralelo y apagado.

### 3.1. Fase 1 - Auditoría y diseño técnico

- **Qué se hace y con qué criterio:** documentar la herramienta actual: nombre, dónde está alojada, cómo guarda los tokens, catálogo de tipologías de suscripción (fútbol, todas las noticias, Real Madrid, etc.), lógica de las alertas automáticas y conexión con la API de resultados. Con esto se diseña la arquitectura nueva: modelo de datos (dispositivo, plataforma, edición, tipologías, estado del permiso), topics o segmentos por edición y tipología, esquema de deep links y modelo de eventos de medición. Se define el catálogo de tipologías por edición, porque cada edición tiene su propia cobertura (por ejemplo, NFL en MARCA English y Liga MX en MARCA México).
- **Tecnologías y superficies:** herramienta actual, base de datos de suscriptores, API de resultados, apps iOS y Android.
- **Calendario:** por definir (ver apartado 6).
- **Resultado:** documento de arquitectura, catálogo de tipologías por edición, esquema de deep links y plan de migración validados por IT y Producto.

### 3.2. Fase 2 - Backend y backoffice de envío

- **Qué se hace y con qué criterio:**
  - **Segmentación por edición:** cada push se envía a una edición (España, USA, English o México) y, dentro de ella, a todos sus usuarios o a una tipología concreta. Por defecto, el usuario recibe las push de la edición que eligió en el onboarding o, si la cambió después, de la que tenga activa en el área de usuario.
  - **Tipos de push:** texto (título y cuerpo), con imagen y con GIF. Vista previa de iOS y Android antes de enviar.
  - **Enlace:** cada push puede llevar un deep link interno (noticia, directo, sección, páginas de datos de resultados, calendario y estadísticas) o un enlace externo (app de Radio MARCA, app de Fantasy MARCA, cualquier URL o app de terceros). El enlace es opcional: sin él, la push abre la portada de la edición.
  - **Envío inmediato y programado:** la hora de programación se interpreta en la zona horaria de la edición: España en hora peninsular, México en hora de Ciudad de México y USA y English en hora del Este (ET) por defecto.
  - **Alertas automáticas:** goles y resultado final a partir de la API de resultados, como hoy, con reglas configurables por edición (qué competiciones y equipos disparan alerta en cada una).
  - **Roles y permisos:** usuarios editoriales con permiso por edición, para que cada redacción envíe solo a la suya. Rol de administrador para Producto e IT.
  - **Envío de prueba:** envío a una lista de dispositivos de test antes del envío real, con un paso de confirmación que muestre la edición, la tipología y el número estimado de destinatarios.
  - **Selector de contenido (recomendado):** buscar una noticia del CMS para rellenar automáticamente título, imagen y deep link, y ahorrar tiempo a la redacción.
  - **Volumen:** sin límite técnico de envíos diarios. Debe soportar 20 o más push al día por edición, más los picos de alertas automáticas en jornada de partidos.
- **Tecnologías y superficies:** backend propio, FCM (Android) y FCM sobre APNs (iOS), API de resultados, CMS (Xalok y UEdit) para el selector de contenido.
- **Calendario:** por definir (ver apartado 6).
- **Resultado:** backoffice operativo para las 4 ediciones, con envío manual, programado y automático.

### 3.3. Fase 3 - Integración en las apps iOS y Android

- **Qué se hace y con qué criterio:**
  - **Registro del dispositivo:** al dar el permiso, la app registra el token con su edición y sus tipologías. Si el usuario cambia de edición o de tipologías en el área de usuario, se actualiza la suscripción al momento.
  - **Pantalla de preferencias:** el usuario gestiona sus tipologías de suscripción con el catálogo de su edición.
  - **Rich push:** en iOS, una Notification Service Extension descarga y muestra la imagen o el GIF animado. En Android, imagen con estilo de imagen grande. El GIF se anima si es viable y, si no, se muestra el primer fotograma.
  - **Router de deep links:** resuelve los destinos internos (noticia, directo, sección, páginas de datos) y los externos. Para Radio MARCA y Fantasy MARCA abre su app si está instalada y, si no, la tienda o la web. Las URL externas se abren en el navegador.
  - **Eventos de medición:** la app envía un evento de recepción (en iOS desde la Notification Service Extension, en Android al recibir el mensaje) y un evento de apertura al pulsar la notificación. Ambos llevan el identificador de la push.
  - **Parámetros de tracking:** cada deep link lleva parámetros de campaña (origen push, identificador de push, edición, tipo) que la app pasa a la herramienta de analítica. Así se atribuye a la push la sesión posterior: páginas vistas, video views y flujo de navegación.
- **Tecnologías y superficies:** app iOS y app Android (mismo binario para las 4 ediciones), SDK de FCM, herramienta de analítica de la app.
- **Calendario:** por definir (ver apartado 6).
- **Resultado:** versión de app en tiendas con el nuevo sistema de push, compatible con la herramienta antigua durante la convivencia.

### 3.4. Fase 4 - Medición y dashboard

- **Qué se hace y con qué criterio:** guardar cada push con todos sus datos y cruzarla con sus eventos. Se mide:
  - **Envío:** número de dispositivos a los que se envía.
  - **Recepción:** dispositivos que confirman la llegada. Ratio de recepción = recibidas / enviadas.
  - **Apertura:** dispositivos que pulsan la push. Ratio de apertura = abiertas / recibidas, y también abiertas / enviadas.
  - **Tráfico generado:** sesiones, páginas vistas y video views atribuidas a cada push.
  - **Datos de cada push:** edición, tipo (texto, imagen, GIF), tipología, texto, enlace de destino, fecha y hora de envío, si fue manual, programada o automática, y quién la envió.
  - **Desgloses:** por edición, plataforma (iOS o Android), dispositivo, país o región (derivado de la IP) y franja horaria.
  - **Tiempo real:** el dashboard de la herramienta muestra envío, recepción y apertura en tiempo casi real (latencia objetivo de pocos minutos) para seguir una push recién enviada.
  - **Histórico:** los datos se exportan a un almacén (BigQuery u otro que decida IT) y se explotan en Looker Studio para el análisis a lo largo del tiempo: ranking de push por apertura y tráfico, comparativa entre ediciones y mejores horas y formatos.
- **Tecnologías y superficies:** backend de eventos, almacén de datos, Looker Studio, herramienta de analítica de la app.
- **Calendario:** por definir (ver apartado 6).
- **Resultado:** dashboard en el backoffice e informe en Looker Studio con histórico, validados por Analítica.

### 3.5. Fase 5 - Migración, convivencia y retirada de la herramienta antigua

- **Qué se hace y con qué criterio:** migrar a la nueva base de datos todos los tokens y las suscripciones por tipología de la herramienta actual, sin pedir de nuevo el permiso al usuario. Asignar a cada usuario migrado su edición (la que tenga activa en la app). Mantener un periodo de convivencia en el que la herramienta antigua siga activa para las versiones de app que no se hayan actualizado, evitando que un usuario reciba la misma push dos veces. Activar primero MARCA España, comprobar que los volúmenes y las alertas automáticas igualan los actuales y después abrir las ediciones internacionales. Apagar la herramienta antigua cuando el porcentaje de usuarios en versiones antiguas sea residual.
- **Tecnologías y superficies:** herramienta actual, nuevo backend, apps iOS y Android.
- **Calendario:** por definir (ver apartado 6).
- **Resultado:** 100 % de los envíos desde el nuevo sistema y herramienta antigua apagada y archivada.

## 4. Ámbito (Web, Apps, Mobile...)

- **CMS:** sin cambios en Xalok ni UEdit. Solo lectura de contenidos para el selector de noticias del backoffice.
- **Web desktop:** no se toca.
- **Web mobile:** no se toca.
- **AMP:** no se toca.
- **App iOS:** registro por edición y tipología, preferencias de notificaciones, Notification Service Extension para imagen, GIF y evento de recepción, router de deep links y eventos de apertura y tracking.
- **App Android:** lo mismo que iOS, con imagen grande y GIF animado si es viable (primer fotograma si no).
- **Ediciones:** las 4: MARCA España, MARCA USA (español), MARCA English (inglés) y MARCA México (español). Cada una con su catálogo de tipologías, sus reglas de alertas automáticas, su zona horaria y sus permisos de envío.
- **Newsletters:** no se tocan.
- **Notificaciones push:** sustitución completa del sistema actual de push de las apps: envío manual, programado y automático, rich push, deep links y medición.
- **Feeds y sitemaps:** no se tocan.
- **Publicidad:** no se toca. Sin push patrocinadas en este proyecto.
- **Analítica:** eventos de recepción y apertura, parámetros de campaña en los deep links, dashboard en tiempo casi real y Looker Studio con histórico.
- **Integraciones:** API de resultados para las alertas automáticas, FCM y APNs para la entrega, y apps de Radio MARCA y Fantasy MARCA como destinos de deep link.
- **Fuera de ámbito:** web push, segmentación nueva por equipo, competición o deporte (más allá de mantener las tipologías de suscripción que existen hoy), Live Activities, widget de resultados en vivo (proyectos independientes), push patrocinadas e integración con la herramienta de atribución.

## 5. Alcance / requisitos

- **Volumen:** 4 ediciones, 2 plataformas (iOS y Android), 3 tipos de push (texto, imagen, GIF), envío manual, programado y automático (goles y resultado final). Toda la base actual de suscriptores y sus tipologías. 20 o más push al día por edición, más los picos de alertas automáticas.
- **Criterios de calidad:** ninguna push llega a una edición distinta de la elegida. Ningún usuario recibe la misma push dos veces durante la convivencia. Las alertas automáticas no deben tardar más que hoy. La vista previa del backoffice coincide con lo que ve el usuario en iOS y en Android.
- **Requisitos técnicos:** un único binario por plataforma para las 4 ediciones. Entrega por FCM y APNs (o el proveedor que se elija). Migración de tokens sin volver a pedir el permiso. Si falla la carga de la imagen o del GIF, la push se muestra igual como texto. Los deep links internos funcionan con la app cerrada, en segundo plano y abierta. El backoffice tiene roles por edición y registro de quién envía cada push.
- **Requisitos SEO:** no aplica (proyecto solo de app, sin superficies indexables).
- **Requisitos analíticos:** identificador único por push presente en los eventos de envío, recepción y apertura y en los parámetros del deep link. Ratios de recepción y apertura por push, edición, plataforma, dispositivo y país. Atribución de sesiones, páginas vistas y video views a cada push. Histórico consultable en Looker Studio. Validación del marcado por Analítica antes del lanzamiento.
- **Requisitos de negocio:** cada edición internacional puede enviar push con su propia cobertura de forma autónoma. El nuevo sistema no puede reducir la base de usuarios con opt-in ni el volumen de envíos actual de MARCA España. Ninguna decisión puede hacer caer usuarios, páginas vistas ni video views.
- **Requisitos legales:** la IP se usa solo para derivar país o región y no se guarda en bruto en el dashboard. El tratamiento de los datos de dispositivo y de los eventos cumple el RGPD y la normativa aplicable en USA y México.

## 6. Aspectos pendientes de definir

- **Fecha de lanzamiento:** Falta: fecha objetivo y calendario por fase. Por qué no se cierra aún: depende de la estimación del equipo de Aplicaciones tras la Fase 1. Decide: Producto (Karen Rodrigues Pita) con IT (Belen Gomez).
- **Herramienta actual:** Falta: nombre, alojamiento, formato de la base de tokens y lógica de las alertas automáticas. Por qué no se cierra aún: no está documentada y la conoce IT. Decide: IT, equipo de Aplicaciones.
- **Desarrollo propio o proveedor:** Falta: decisión final. Por qué no se cierra aún: depende de la estimación de coste y plazo del desarrollo propio frente a las licencias de mercado. Decide: Producto e IT, con aprobación de Gema Monjas si hay coste de licencia.
- **Datos de partida:** Falta: usuarios con opt-in por edición y plataforma, y tasa de apertura de referencia. Por qué no se cierra aún: la herramienta actual no da recepción ni apertura, y el inventario de tokens sale de la Fase 1. Decide: IT y Analítica (Jorge Alia).
- **Herramienta de analítica y almacén de datos:** Falta: confirmar dónde se reciben los eventos de la app y dónde se guarda el histórico que alimenta Looker Studio. Por qué no se cierra aún: depende del stack actual de analítica de la app. Decide: Analítica (Jorge Alia) e IT.

## 7. Ejemplos / prototipos

- **Firebase Cloud Messaging:** https://firebase.google.com/docs/cloud-messaging - Canal de entrega propuesto para el desarrollo propio. Incluye topics para segmentar y exportación de datos de entrega a BigQuery.
- **Notification Service Extension (Apple):** https://developer.apple.com/documentation/usernotifications/unnotificationserviceextension - Mecanismo de iOS para imagen, GIF y evento de recepción.
- **Airship:** https://www.airship.com - Plataforma de push usada por medios. Referencia de backoffice editorial, rich push y métricas, y alternativa si se decide contratar.
- **OneSignal:** https://onesignal.com - Alternativa de mercado con capa gratuita y dashboard de entrega y apertura. Sirve para comparar costes.
- **Braze:** https://www.braze.com - Referencia de segmentación y analítica avanzada. Más cara, útil como techo funcional.
- **Batch:** https://batch.com - Proveedor europeo con clientes de medios. Interesante por el alojamiento de datos en la UE.
- **Prototipo / diseño:** no existe todavía. El equipo de Diseño/UX lo prepara en la Fase 1 (backoffice y pantalla de preferencias).

## 8. Equipos implicados

- **IT/Desarrollo:** arquitectura, backend, backoffice, integración con la API de resultados, migración y retirada de la herramienta antigua - responsable: equipo de Aplicaciones de IT, con Belen Gomez (PM IT) en la coordinación.
- **Producto:** definición, priorización, validación funcional y coordinación entre ediciones - responsable: Karen Rodrigues Pita.
- **Diseño/UX:** interfaz del backoffice (creación, vista previa, programación, dashboard) y pantalla de preferencias de notificaciones en la app - responsable: equipo UX/UI.
- **Contenido/Editorial:** usuario principal de la herramienta. Define las tipologías y las reglas de alertas automáticas de cada edición y valida el flujo de envío - responsable: Emilio (edición España) y responsables de cada edición internacional (por confirmar).
- **Analítica:** modelo de eventos, parámetros de tracking, validación del marcado y Looker Studio - responsable: Jorge Alia.
- **Legal:** revisión del tratamiento de datos de dispositivo, IP y eventos en las 4 ediciones - responsable: por confirmar.
- **QA:** pruebas por edición, plataforma, tipo de push y deep link, y validación de la migración sin duplicados - responsable: departamento de QA.
