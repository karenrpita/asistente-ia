---
title: "SOP-TECH-012: Redacción de GNPs (alta de nuevos proyectos)"
tipo: sop
categoria: technical
estado: activo
fecha-creacion: 2026-10-02
updated: 2026-10-17
tags:
  - sop
  - knowledge
  - tema/producto
---

# SOP-TECH-012: Redacción de GNPs (alta de nuevos proyectos)

## Índice

1. [Objetivo](#objetivo)
2. [Cuándo se aplica](#cuándo-se-aplica)
3. [Paso 1 — Investigación previa](#paso-1--investigación-previa)
4. [Paso 2 — Estructura fija del GNP](#paso-2--estructura-fija-del-gnp)
5. [Paso 3 — Control de calidad antes de entregar](#paso-3--control-de-calidad-antes-de-entregar)
6. [Dónde se guarda](#dónde-se-guarda)
7. [Plantilla en blanco](#plantilla-en-blanco)
8. [Historial de versiones](#historial-de-versiones)

---

## Objetivo

Un **GNP** es la ficha con la que se da de alta un nuevo proyecto. Tiene una estructura cerrada: todos los GNPs llevan **los mismos apartados, en el mismo orden y con el mismo nivel de detalle**. Así todos los equipos (técnico, contenido, SEO, analítica, negocio) los leen igual y se pueden comparar y priorizar entre sí.

Este SOP fija ese modelo. Primero se investiga y después se redacta siguiendo exactamente la plantilla, sin añadir, quitar ni reordenar apartados.

---

## Cuándo se aplica

Cuando se pida "hazme un GNP de…", "prepara el GNP para…", "necesito dar de alta el proyecto…" o equivalente.

---

## Paso 1 — Investigación previa

Antes de escribir una línea, reunir todo lo que ya se sabe del proyecto. **No inventar datos:** si una cifra no tiene fuente, va a *Aspectos pendientes de definir*.

| Qué buscar | Para qué sirve en el GNP |
|---|---|
| Nota o documentación del proyecto (contexto, decisiones, datos) | Necesidad, objetivo y descripción |
| Tareas abiertas y diagnósticos relacionados | Necesidad (problemas detectados) y pendientes |
| Menciones en reuniones o notas recientes | Decisiones tomadas y huecos por cerrar |
| Proyectos parecidos ya hechos o GNPs anteriores | Ejemplos / prototipos y referencia de fases |
| Metodologías y SOPs aplicables | Describir las fases con rigor |
| **Objetivos y KPIs vigentes de la empresa / cabecera** en ese momento | Necesidad (punto de partida obligatorio) y objetivos |
| **Frenos documentados:** limitaciones técnicas, necesidades no cubiertas, cosas que se han dicho que "ahora mismo no se pueden hacer" (en cualquier proyecto, reunión o nota) | Objetivo (realismo), descripción y alcance |
| Stack tecnológico del producto afectado (CMS, apps, AMP, ediciones, integraciones) | Descripción y ámbito |
| Contexto del producto o negocio afectado (audiencia, estrategia) | Objetivos medibles y requisitos |
| Equipos y personas implicadas | Equipos implicados, con responsable si se conoce |
| Datos actuales (tráfico, inventario, rendimiento) | Cifras de la necesidad y del alcance — solo si se piden o el GNP no se sostiene sin ellas |

**Resultado del paso:** una lista de hechos, cada uno con su fuente, y una lista de preguntas para el usuario con todo lo que no se ha encontrado. **Las preguntas se hacen antes de redactar**, no se dejan para el apartado de pendientes.

---

## Paso 2 — Estructura fija del GNP

Título: **`GNP - [Nombre del proyecto]`**. Después, estos ocho apartados, en este orden y con estos nombres exactos.

### 1. Identificación de la necesidad
**Qué es:** el problema que origina el proyecto, no la solución.
**Antes de redactar:** revisar los **objetivos y KPIs vigentes de la empresa** en ese momento. Si no están documentados, **preguntar al usuario para qué cabecera o producto es y cuáles son sus KPIs**. La necesidad se justifica contra esos KPIs.
**Formato:** 2-4 puntos, cada uno con etiqueta en negrita y una frase concreta.
**Debe incluir:** el KPI al que afecta cada problema, cifras cuando existan y los riesgos (técnicos, de posicionamiento, de negocio, legales) si los hay.

### 2. Objetivo
**Qué es:** lo que se consigue al terminar.
**Antes de redactar:** cruzar cada objetivo con los **frenos conocidos**. Son las limitaciones técnicas, las necesidades no cubiertas y lo que alguna vez se ha dicho que "ahora mismo no se puede hacer", esté documentado en este proyecto o en cualquier otro. Un objetivo que choca con un freno se reformula o se acompaña del freno y de cómo sortearlo.
**Formato:** 2-4 puntos con etiqueta en negrita.
**Regla:** cada objetivo responde a una necesidad del apartado 1. Medibles cuando se pueda. Ninguno ignora un freno documentado.

### 3. Descripción
**Qué es:** el detalle de **todo** lo que hay que hacer, lo más completo posible.
**Cobertura tecnológica:** tener en cuenta todas las tecnologías que toca el proyecto, según su tamaño:
- **Proyecto pequeño o personal** (p. ej. un WordPress): basta con el stack real del sitio.
- **Proyecto corporativo o de un medio:** revisar el CMS y todas sus dependencias. Incluye web desktop y mobile, AMP, apps iOS/Android, ediciones (nacionales e internacionales), newsletters, notificaciones push, feeds, sitemaps, publicidad, analítica, buscador interno, integraciones con terceros, etc. Si una tecnología no se ve afectada, se dice.

**Formato:**
- Un párrafo de apertura que enumera las fases, con una línea por fase.
- Después, una subsección numerada por fase (`1. Nombre de la fase`, `2. …`) con:
  - qué se hace y con qué criterio,
  - qué tecnologías y superficies toca,
  - calendario si se conoce (mes/año por fase),
  - estructuras resultantes (URLs, taxonomías, componentes, flujos) cuando aplique.

**Regla:** cada fase anunciada en la apertura tiene su subsección desarrollada. Ninguna queda en blanco.

### 4. Ámbito (Web, Apps, Mobile...)
**Qué es:** las superficies, tecnologías y ediciones afectadas.
**Formato:** una línea por superficie explicando qué se toca en ella. Repasar la lista completa: CMS, web desktop/mobile, AMP, apps iOS/Android, ediciones, newsletters, push, feeds y sitemaps, publicidad, analítica y cualquier otra que aplique.
**Regla:** lo que no se toca también se dice ("Fuera de ámbito"), para que nadie lo dé por incluido. En proyectos pequeños, solo las superficies que existen.

### 5. Alcance / requisitos
**Qué es:** qué entra en el proyecto y qué condiciones debe cumplir.
**Formato:** lista con etiqueta en negrita + frase.
**Debe cubrir:** volúmenes (inventario, nº de plantillas, secciones), criterios de calidad y requisitos técnicos, SEO, analíticos y de negocio.

### 6. Aspectos pendientes de definir
**Qué es:** lo que de verdad no se puede cerrar todavía. **La meta es que haya lo mínimo posible.**
**Antes de redactar:** todo lo que no esté definido se le plantea al usuario **antes de cerrar el GNP**, para definirlo juntos. El proyecto no debe pasar a tecnología con huecos que se podían haber resuelto.
**Formato:** cada punto dice **qué falta**, **por qué no se puede cerrar aún** y **quién debe decidirlo**.
**Regla:** solo entra lo que, tras consultarlo, sigue dependiendo de un tercero o de un dato futuro. Si todo está definido, decirlo explícitamente.

### 7. Ejemplos / prototipos
**Qué es:** proyectos que sirven de modelo: propios, de competidores o referentes.
**Antes de redactar:** revisar todo lo documentado hasta ahora (proyectos anteriores, GNPs, migraciones, rediseños, análisis de competencia). Si no aparece nada que sirva, **preguntar al usuario** antes de dejar el apartado flojo.
**Formato:** enlace + una frase de por qué sirve. Si hay prototipos o diseños (maquetas, Figma, etc.), enlazarlos.
**Regla:** ninguna frase a medias.

### 8. Equipos implicados
**Qué es:** quién participa y en qué.
**Criterio:** por defecto, la mayoría de los equipos participan en casi todos los proyectos. Se parte de la lista completa y solo se quita un equipo si de verdad no tiene nada que hacer. La lista es: SEO, IT/Desarrollo, Producto, Diseño/UX, Contenido/Editorial, Analítica, Audiencias/Redes, Publicidad/Comercial, Marketing/Newsletters, Legal, QA. Si hay dudas sobre quién lleva algo, preguntar antes.
**Formato:** un punto por equipo con **en qué participa** concretamente.
**Regla:** si se conoce a la persona responsable, nombrarla.

### Cierre
No hay apartado extra: el GNP termina en *Equipos implicados*. Sin conclusiones, resúmenes ni próximos pasos fuera de la plantilla. Lo que quede abierto va en el apartado 6.

**Estilo:** español, frases cortas, formato "**Etiqueta:** explicación" en las listas, sin relleno. Que se pueda copiar y pegar tal cual en el sistema donde se da de alta.

---

## Paso 3 — Control de calidad antes de entregar

- [ ] Están los 8 apartados con su nombre exacto y en orden.
- [ ] La necesidad está anclada a los KPIs vigentes (documentados o confirmados por el usuario).
- [ ] Cada necesidad tiene un objetivo que la responde.
- [ ] Se han revisado los frenos documentados y ningún objetivo choca con uno sin decirlo.
- [ ] Descripción y Ámbito repasan todas las tecnologías y ediciones aplicables, incluido lo que queda fuera.
- [ ] Lo indefinido se ha consultado con el usuario; en Pendientes solo queda lo que depende de terceros.
- [ ] Equipos: se ha partido de la lista completa y cada exclusión está justificada.
- [ ] Todas las fases de la Descripción están desarrolladas (ninguna numeración vacía, ninguna frase cortada).
- [ ] Toda cifra tiene fuente; si no, está en Pendientes.
- [ ] Los ejemplos enlazan a documentos que existen.
- [ ] Cada equipo tiene su rol concreto, no solo el nombre.

Al entregar, indicar en 1-2 líneas qué fuentes se usaron y qué quedó en Pendientes por falta de información.

---

## Dónde se guarda

- En la carpeta del proyecto: `<carpeta-del-proyecto>/gnp-<proyecto>.md` (o junto a la nota principal si el proyecto no tiene carpeta propia).
- Enlazarlo desde la nota principal del proyecto.

---

## Plantilla en blanco

Esqueleto para copiar. Lo que va entre `[ ]` se sustituye; los comentarios en cursiva se borran.

> **GNP - [Nombre del proyecto]**
>
> **Identificación de la necesidad**
> - **[Problema 1]:** [Qué pasa hoy, con cifra si existe.]
> - **[Problema 2]:** [Qué pasa hoy, con cifra si existe.]
> - **[Riesgo]:** [Qué puede salir mal si no se actúa.]
>
> **Objetivo**
> - **[Objetivo 1]:** [Qué se consigue — responde al problema 1.]
> - **[Objetivo 2]:** [Qué se consigue — responde al problema 2.]
> - **[Objetivo 3]:** [Qué se consigue — responde al riesgo.]
>
> **Descripción**
> El proyecto se divide en [N] fases:
> - **[Fase 1]:** [Una línea.]
> - **[Fase 2]:** [Una línea.]
> - **[Fase 3]:** [Una línea.]
>
> *1. [Fase 1]* — [Qué se hace, con qué criterio, cuándo y qué resulta.]
>
> *2. [Fase 2]* — [Qué se hace, con qué criterio, cuándo y qué resulta.]
>
> *3. [Fase 3]* — [Qué se hace, con qué criterio, cuándo y qué resulta.]
>
> **Ámbito (Web, Apps, Mobile...)**
> - **[Superficie 1]:** [Qué se toca en ella.]
> - **[Superficie 2]:** [Qué se toca en ella.]
> - **Fuera de ámbito:** [Lo que explícitamente no entra, si aplica.]
>
> **Alcance / requisitos**
> - **[Volumen]:** [Inventario, nº de plantillas, secciones…]
> - **[Criterio de calidad]:** [Condición que debe cumplir.]
> - **[Requisito técnico / SEO / analítico / de negocio]:** [Condición que debe cumplir.]
>
> **Aspectos pendientes de definir**
> - **[Tema abierto]:** [Qué falta decidir] — decide: [equipo o persona].
>
> **Ejemplos / prototipos**
> - **[Referencia]:** [Enlace] — [por qué sirve de modelo.]
>
> **Equipos implicados**
> - **[Equipo 1]:** [En qué participa] — responsable: [persona, si se conoce].
> - **[Equipo 2]:** [En qué participa] — responsable: [persona, si se conoce].

---

## Historial de versiones

| Versión | Fecha | Cambio |
|---|---|---|
| 1.0 | 2026-10-02 | Creación a partir de un GNP real de migración de CMS. |
| 2.0 | 2026-10-17 | Versión genérica: sin referencias a proyectos ni empresas concretas; el ejemplo real se sustituye por una plantilla en blanco y cada apartado explica qué es, su formato y su regla. |
| 2.1 | 2026-10-17 | Necesidad anclada a KPIs vigentes (o preguntar cabecera y KPIs); objetivos cruzados con frenos documentados; descripción y ámbito con cobertura tecnológica completa; pendientes mínimos, consultados antes de cerrar; ejemplos y equipos con revisión completa y pregunta si falta información. |

---

## 🔗 Relacionado

- [[sops-index]]
- [[web-migration-guidelines]] · [[seo-content-audit]] · [[redesign-implementation-process]]
