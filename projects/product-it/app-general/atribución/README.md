# Atribución — Selección de MMP

**Estado:** Decisión pendiente — evaluación comparativa activa
**Última actualización:** 2026-05-04 (propuesta AppsFlyer actualizada con datos del Excel de Capacity Credits)
**Owner técnico (IT):** Franz

---

## Decisión a tomar

Seleccionar el MMP (Mobile Measurement Partner) para la nueva app de MARCA. Función principal: atribuir instalaciones, deduplicar canales (Meta, Google, CRM, afiliados, QR...) y optimizar la inversión en marketing.

Candidatos activos: **Adjust**, **AppsFlyer**, **Singular**

---

## Información pendiente para decidir

Estos datos están bloqueando la decisión. Sin ellos no se puede cerrar ni precio ni proveedor.

### De MARCA

| # | Dato necesario | Quién lo tiene | Estado |
| :--- | :--- | :--- | :--- |
| 1 | Volumen real de impresiones de banners web que llevan a la app | Ana Maria / MKT | Pendiente |
| 2 | Presupuesto máximo aprobado para el MMP | Gema Monjas | Pendiente |
| 3 | Canales de marketing activos (Meta, Google, afiliados, CRM, newsletters, QR...) | MKT | Pendiente |
| 4 | Fecha de lanzamiento de la app | Karen / Franz | Pendiente |
| 5 | Peso real de las redes de afiliados en el mix (riesgo de fraude) | MKT | Pendiente |

> El dato más crítico es el #1: sin él no se puede calcular si ninguno de los paquetes actuales es suficiente.

### De los proveedores

| # | Dato necesario | Proveedor | Contacto | Estado |
| :--- | :--- | :--- | :--- | :--- |
| 6 | Propuesta completa (precio, modelo, funcionalidades) | Singular | — | No iniciada |
| 7 | Confirmar si el precio especial sigue vigente (expiración prevista fin de abril 2026) | Adjust | Elena Schad | Pendiente |
| 8 | Confirmar si las condiciones de Q4 2025 siguen vigentes | AppsFlyer | Nicolas Orozco | Pendiente |

---

## Comparativa de proveedores

Incompleta hasta recibir propuesta de Singular y confirmar vigencia de precios.

| Criterio | Adjust | AppsFlyer | Singular |
| :--- | :--- | :--- | :--- |
| Precio anual | €8.000 (op.1) / €10.000 (op.2) | $82.000 Estándar / $99.870 Premium (~75K€ / ~92K€) | Pendiente |
| Modelo de consumo | Data Points (cap 1,4B) | Capacity Credits (4.354 incluidos, 2.354 + 2.000 bono) | Pendiente |
| Conversiones incluidas | 350K (op.1) / 480K (op.2) | 443K estimadas (reales MARCA: ~88K) | Pendiente |
| Anti-fraude | No documentado | Protect360 — solo en Premium | Pendiente |
| Audiencias | No documentado | Solo en Premium | Pendiente |
| Soporte | No documentado | Enterprise CSM (dedicado) vs Growth CSM (compartido) | Pendiente |
| Plazo mínimo contrato | Anual | 24 meses | Pendiente |
| MAUs incluidos | No documentado | Hasta 2M (ambos paquetes) | Pendiente |
| Vigencia precio actual | Posiblemente expirado | Condiciones firmadas antes del 31 dic 2025 — posiblemente expirado | — |
| Integraciones confirmadas | No documentado | OneLink, Web-to-app, QR, AdMob, Data Locker | Pendiente |
| Brecha presupuestaria | — | ~15K€ entre objetivo MARCA (60K€) y opción más barata (~75K€) | — |

---

## Criterios de decisión

Para evaluar los tres en igualdad de condiciones:

1. **Precio ajustado** a volúmenes reales de MARCA (no estimaciones del proveedor)
2. **Suficiencia del límite de consumo** sin riesgo de sobrecosto (data points / credits)
3. **Anti-fraude** — relevante por uso de redes de afiliados locales con riesgo de bots y click spamming
4. **Calidad de reporting** y acceso a datos raw
5. **Integraciones** — Meta, Google, CRM, QR digital e impreso, web-to-app
6. **Facilidad de integración SDK** para Franz / IT
7. **Soporte real post-firma** (no el nivel comercial)
8. **Cumplimiento GDPR**

---

## Detalle por proveedor

---

### Adjust

#### Participantes clave

- **Karen Rodrigues Pita** — Head of Product, MARCA (Unidad Editorial)
- **Elena Schad** — Mobile Attribution Consultant / Account Executive, Adjust
- **Clara Pardo Latre** — Equipo de producto digital, MARCA
- **Gema Monjas Ramirez** — Directora de Negocio MARCA y Radio MARCA
- **Ana Maria Ramos Esteban** — Contacto para homologación de proveedores, MARCA

---

#### Comparativa de opciones (actualizada al 27-29 de abril de 2026)

| Elemento | Opción 1 | Opción 2 |
| :--- | :--- | :--- |
| Conversiones anuales | 350.000 | 480.000 |
| Coste conversión extra | €0,045 | €0,04 |
| Data Point Cap | 1,4 Billones (ajustado) | 1,4 Billones |
| Precio especial MARCA | **€8.000** | **€10.000** |

> **Nota crítica:** Elena Schad aclaró que en la Opción 1 el límite es de 1,4 billones de data points, corrigiendo el error previo del contrato que indicaba 0,6B.

---

#### Definiciones y métricas

- **Data Points:** Suma total de impresiones, clics, sesiones y eventos in-app. Cada impresión cuenta como un data point, aunque no convierta (confirmado por Elena Schad).
- **Conversiones (Paid):** Instalaciones o reatribuciones derivadas de marketing de pago (Ads, redes sociales, afiliados) y Owned Media (newsletters, QR, anuncios en webs propias) si usan links de Adjust.
- **Instalaciones orgánicas:** Gratuitas. Instalación = Descarga + Apertura de la App.
- **Ad Spend:** Límite de $2,5M en gasto publicitario gestionado a través de la herramienta.

---

#### Tiempos, plazos e implicaciones

- **Vigencia de precios:** Los descuentos especiales estaban sujetos a firma antes de finales de marzo/abril de 2026.
- **Estado del contrato (29 de abril de 2026):** Elena solicita novedades sobre la firma. Karen informa que el equipo de marketing está calculando el volumen total de impresiones para confirmar que el límite de data points sea suficiente.
- **Coste por exceso de data points:** €1.400 por cada 100 millones adicionales.
- **Alertas automáticas de consumo:** Adjust notifica al alcanzar el 50%, 75% y 90% del uso. No es posible restringir el consumo técnicamente; la gestión es manual.
- **Condiciones de pago:** Pago anual por adelantado (Annual up front), vencimiento a 30 días.

---

#### Estado actual y bloqueos (mayo 2026)

El contrato no está firmado. Los bloqueos activos son:

1. **Volumen de impresiones pendiente:** El equipo de Marketing está calculando el total de impresiones para determinar si 1,4B de data points es suficiente o si se necesita subir a 2B. Sin esta cifra no se puede elegir opción ni cerrar precio.
2. **Evaluación de Singular:** Se ha incorporado Singular al proceso de selección. La decisión final de proveedor depende de esta evaluación comparativa (Adjust vs AppsFlyer vs Singular).
3. **Elección de opción (€8.000 vs €10.000):** Bloqueada hasta resolver los puntos 1 y 2.
4. **Aprobación presupuestaria:** Gema Monjas debe validar el presupuesto una vez cerrados los puntos anteriores.
5. **Homologación de proveedor:** No iniciada. Depende de cerrar el acuerdo. Contacto: Ana Maria Ramos Esteban.

> Los precios especiales negociados tenían vigencia hasta finales de abril de 2026. Pendiente confirmar con Elena Schad si siguen vigentes.

---

#### Próximos pasos

1. Obtener cifra de impresiones de MKT y comparar con el límite de 1,4B.
2. Completar evaluación de Singular y decidir proveedor.
3. Si se elige Adjust: confirmar opción, negociar precio si el límite necesita subir a 2B, y confirmar vigencia de los precios especiales.
4. Aprobación presupuestaria con Gema Monjas.
5. Iniciar homologación de proveedor con Ana Maria Ramos Esteban.
6. Coordinación técnica con Franz (IT) para integración del SDK.

---

### AppsFlyer

#### Participantes clave

- **Karen Rodrigues Pita** — Head of Product, MARCA (Unidad Editorial). Coordinadora principal del proyecto.
- **Gema Monjas Ramirez** — Directora de Negocio MARCA y Radio MARCA. Aprobación final de presupuesto.
- **Ana Maria Ramos Esteban** — Equipo de Marketing. Responsable de aportar datos de rendimiento (impresiones, clics, CTR).
- **Adrián Carrión Armas** — Equipo de Producto/Tecnología. Involucrado en el seguimiento.
- **Nicolas Orozco** — Enterprise Account Executive, AppsFlyer. Gestor comercial y responsable de la propuesta.
- **Miri Shlimak** — Manager, AppsFlyer. Soporte en la negociación.

---

#### Objetivo

Establecer un MMP (Mobile Measurement Partner) para la nueva app de MARCA que permita atribuir instalaciones, deduplicar canales (Meta, Google, CRM, etc.) y optimizar la inversión en marketing.

**Gaps actuales que resuelve AppsFlyer:**
- Datos fragmentados sin visión unificada del funnel
- Duplicidad de conversiones entre plataformas (Meta, Google, Addict)
- Falta de visibilidad en el viaje web-to-app

---

#### KPIs de referencia aportados por MKT (semana tipo, 13-18 octubre)

| Métrica | Valor |
| :--- | :--- |
| Total impresiones | 9.238.908 |
| Total clics | 2.061 |
| CTR promedio | 0,02% |

> Estos datos sirven como base para el cálculo de Capacity Credits. La conversión es baja pero es la referencia real disponible.

---

#### Modelo de consumo: Capacity Credits

El coste depende del volumen de acciones registradas. Los créditos son universales (un crédito = un tipo de evento procesado).

**Créditos incluidos en la propuesta:** 4.354 totales (2.354 comprados + 2.000 de bono)

**Coste de crédito extra:** $1,35 (prepago) / $1,72 (Pay As You Go)

**Estimación de consumo proyectada para MARCA** (fuente: Excel "Créditos de capacidad actualizados"):

| Tipo de evento | Volumen estimado | Créditos consumidos |
| :--- | :--- | :--- |
| Instalaciones no orgánicas | 443.282 eventos | 355 créditos |
| Impresiones | ~725M | 725 créditos |
| Data Locker (filas procesadas) | ~848M filas | 1.698 créditos |
| **Total estimado** | — | **~2.778 créditos** |

> Con 4.354 créditos incluidos, el margen sobre el consumo proyectado es de ~1.576 créditos. Pendiente ajustar con datos reales de banners web.

**Dato histórico MARCA:** ~88.000 instalaciones no orgánicas reales (sep 2024 – sep 2025). La propuesta de AppsFlyer usa 443K como estimación conservadora hacia arriba.

---

#### Precio y condiciones

Contrato de 24 meses con pago anual. Dos paquetes:

| Elemento | Paquete Estándar | Paquete Premium |
| :--- | :--- | :--- |
| Costo total anual | **$82.000** (~75K€) | **$99.870** (~92K€) |
| Acceso plataforma | $78.822 | $96.692 |
| Capacity Credits | $3.178 | $3.178 |
| MAUs incluidos | Hasta 2M | Hasta 2M |
| Protect360 (antifraude) | No incluido | Incluido |
| Audiencias | No incluido | Incluido |
| Soporte | Enterprise o Growth CSM | Enterprise o Growth CSM |

> Los precios incluyen descuento por firma antes del 31 de diciembre de 2025. Fecha ya superada — pendiente confirmar con Nicolas Orozco si siguen vigentes.

**Brecha presupuestaria:** MARCA tiene objetivo de 60K€. La opción más barata (Estándar) es ~75K€. Diferencia: ~15K€ que Nicolas Orozco está intentando solventar con la duración del contrato a 2 años.

**Incentivo incluido:** Módulo *Incrementality for UA* gratuito durante 12 meses (en ambos paquetes).

**Soporte:** Debate entre **Enterprise CSM** (dedicado, reuniones semanales, recomendado para un lanzamiento) vs. **Growth CSM** (compartido, reactivo, revisiones trimestrales).

---

#### Tiempos y plazos

El calendario original de AppsFlyer era para diciembre 2025. **Todos los plazos han sido superados** (hoy es mayo 2026).

| Periodo original | Acción planificada |
| :--- | :--- |
| 1 – 5 dic 2025 | Revisión interna y escalado a Gema y François (CEO) |
| 5 – 10 dic 2025 | Revisión legal de documentos |
| 10 – 15 dic 2025 | Firma del contrato |
| 15 – 20 dic 2025 | Inicio de onboarding con Customer Success |

> Las condiciones de Q4 2025 ya no son aplicables. Pendiente negociar nuevas condiciones con Nicolas Orozco.

**Onboarding** (cuando se reactive): fases de introducción, planificación técnica del SDK y Executive Business Reviews periódicas.

---

#### Capacidades y elementos estratégicos

- **Protect360 (antifraude):** Solo incluido en el paquete Premium. Recomendado dado el uso de redes de afiliación locales, donde el riesgo de instalaciones falsas (bots, click spamming) es alto.
- **Audiencias:** Solo en Premium. Exclusiones inteligentes y retargeting/fidelización basados en datos in-app y CRM.
- **OneLink:** Deep linking multicanal para experiencias de usuario fluidas entre web y app.
- **Web-to-app / QR:** Seguimiento de tráfico desde web y códigos QR (digital e impreso).
- **Data Locker:** Acceso a datos raw en bulk (~848M filas estimadas para MARCA). Consume 1.698 créditos.
- **AdMob:** Integración opcional para ingresos publicitarios.
- **Incrementality for UA:** Gratis 12 meses. Mide el impacto real incremental de las audiencias.

---

#### Estado actual y bloqueos (mayo 2026)

1. **Condiciones expiradas:** Los precios negociados en Q4 2025 ya no son válidos (firma requerida antes del 31 dic 2025). Hay que renegociar con Nicolas Orozco antes de cualquier otro paso.
2. **Brecha presupuestaria activa:** MARCA quiere 60K€, la opción más barata (Estándar) cuesta ~75K€. Diferencia de ~15K€ sin resolver.
3. **Decisión entre paquetes:** Protect360 y Audiencias solo están en Premium (~92K€). Si el riesgo de fraude por afiliados es relevante, el paquete Estándar no cubre ese riesgo.
4. **Datos reales de impresiones de banners web pendientes:** Sin esta cifra no se puede validar si el margen de créditos (~1.576) es suficiente.
5. **Decisión de proveedor pendiente:** AppsFlyer compite con Adjust y Singular. No se puede avanzar en la firma hasta tener la comparativa completa.
6. **Aprobación presupuestaria:** Gema Monjas debe validar una vez cerrada la comparativa y ajustado el precio.

---

#### Próximos pasos

1. Contactar a Nicolas Orozco para confirmar si hay nuevas condiciones vigentes post-2025 y si la brecha de ~15K€ tiene solución.
2. Decidir si se necesita Protect360 (afiliados) — si sí, el mínimo es Premium (~92K€), lo que amplía la brecha.
3. Obtener datos reales de impresiones de banners web (Ana Maria / MKT) para validar el margen de créditos.
4. Completar evaluación comparativa (Adjust vs AppsFlyer vs Singular).
5. Decidir proveedor, paquete y tier de soporte (Enterprise CSM vs Growth CSM).
6. Aprobación presupuestaria con Gema Monjas.
7. Revisión legal e inicio de firma.

---

### Singular

**Estado:** En evaluación — propuesta no recibida aún.

Incorporado recientemente al proceso de selección comparativa. Pendiente recibir propuesta formal con:
- Modelo de pricing y consumo
- Funcionalidades anti-fraude
- Integraciones disponibles (Meta, Google, CRM, QR, web-to-app)
- Soporte incluido
- Condiciones de contrato (plazo mínimo, forma de pago)
