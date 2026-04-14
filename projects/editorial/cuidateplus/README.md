# CuídatePlus

**Estado:** Activo

## Descripción

CuídatePlus es la cabecera de salud de Unidad Editorial. El equipo SEO de MARCA da soporte transversal a este vertical. El contenido de salud entra en la categoría YMYL (Your Money or Your Life), lo que implica requisitos EEAT más estrictos por parte de Google.

El proyecto en curso es la **migración de CuídatePlus como carpeta dentro de MARCA** (marca.com/cuidateplus/). De unas 40K URLs actuales, el objetivo es reducir en aproximadamente un 25% antes de la migración.

## Contactos clave

- Daniel Aparicio — Director Salud
- Mar Sevilla — Jefa de redacción
- Oscar Sánchez Martín — Desarrollo
- Sergio Magan — Maquetador
- Chary Serrano — Directora Negocio

## Objetivo SEO

Mantener y mejorar la visibilidad orgánica de CuídatePlus bajo los criterios EEAT para contenido YMYL, ejecutando la migración sin pérdida de tráfico.

## Diagnóstico y prioridades de limpieza

**PRIORIDAD 1 — YMYL:**
- Eliminar URLs con poco valor: no firmadas, no actualizadas desde 2015 (especialmente medicamentos y enfermedades)
- Contenidos de medicamentos y enfermedades: si se mantienen, deben revisarse al 100% y firmarse
- Eliminar Mediktor
- Eliminar imágenes médicas (jeringuillas, pastillas) en contenidos y contenidos patrocinados
- Contenidos patrocinados: nofollow en todos los enlaces + noindex si son médicos

**PRIORIDAD 2 — Necesidades técnicas:**
- Certificado de acreditación (tipo URAC)
- Todos los contenidos nuevos firmados (mandatory)
- Páginas de autor para todos los redactores y expertos
- Fact Checked — implementación correcta en web + AMP
- Arquitectura nueva: de muchas secciones a 4-7 secciones principales
- CT Noticia para todos los contenidos (única plantilla)
- Diccionarios, recetas y patologías a CT Noticia
- Programas educativos: renombrar a "Educación" y migrar
- Migrar imágenes y adaptar a los cortes de Xalok

## Decisiones tomadas (de las reuniones de planificación)

- **Bienestar y C+:** Unificar. Usar el recurso aprobado en MARCA para atacar la actualidad y Discover.
- **Medicamentos:** Eliminar thin content. El contenido bien hecho no necesariamente.
- **Enfermedades:** Eliminar thin content. Analizar caso a caso el bien hecho.
- **Sin firmas:** No migrar. Sin firma = eliminar.
- **Tags:** Compartir con MARCA.
- **Imágenes:** Mismos cortes (3) que MARCA y imageobject.
- **CTs sin equivalente en MARCA:** Unificar bajo CTs de MARCA.
- **Nombre:** Mantener CuídatePlus.

## Estructura de URLs (migración)

```
cuidateplus.marca.com/[SLUG]  →  301  →  www.marca.com/cuidateplus/[SLUG]
```

Resoluciones:
- 301: URLs con autoridad que no interese conservar
- 410: URLs que no interese conservar

**URLs de cuidateplus.com** deben apuntar directamente a URLs finales (incluyendo enlaces internos).

## Plantillas especiales existentes

- Portadillas de enfermedades (agrupaciones de patologías)
- Fichas de enfermedades individuales
- Diccionarios: alimentación, dietas, belleza, sexualidad, ejercicio físico, bebé, niño, adolescencia, fertilidad, parto, embarazo
- Términos de diccionario (plantilla propia)
- Recetas
- Sección Preguntas y Respuestas (años sin actualizarse — evaluar)
- Portadilla Programas Educativos
- Proyectos de publicidad: Cuidándote, MásQuePacientes

## Recursos internos

- Carpeta Drive: https://drive.google.com/drive/u/0/folders/1RDf7j4yZjVDPR0K0B4Cp28QhrfEUtFra
- CMS: https://cms-cuidateplus.marca.com/
- Staging sin caché: https://sta-cms-cuidateplus.marca.com/
- Control de Jiras: https://docs.google.com/spreadsheets/d/1H0boq9ypQ8k4qyahYXTIau7v6U8myGSQ5pa1mq0R6GE/
- Arquitectura web: https://docs.google.com/presentation/d/1W3Um2nuBlzfHe9ioLZL2EMGfkoHKVKSSPa-xkKBfnzI/
- Calendario días de la salud: https://docs.google.com/spreadsheets/d/17N80TBg2x0NQjd05sfwOYtoD_lpJgIdLcR9qmPEjGgE/
- Sitemaps: https://cuidateplus.marca.com/simplemap-index.xml

## Posicionamiento competitivo (GfK — Marzo 2024)

CuídatePlus sigue líder en salud a pesar del Core Update de Marzo 2024. Competidores principales: webconsultas.com, mejorconsalud.as.com, vitonica.com.

## Consideraciones SEO críticas

- **YMYL:** Salud es categoría de máximo riesgo en evaluación EEAT de Google
- **E-E-A-T:** Autoría médica clara, bios de autores con credenciales, fuentes verificables
- **Autoría:** Cada artículo debe tener autor experto identificado (médico, nutricionista, etc.)
- **Revisión médica:** Indicar si el contenido ha sido revisado por profesional sanitario
- **Fuentes:** Citar estudios, organismos oficiales (OMS, ministerios)
- **Actualización:** Contenido YMYL desactualizado puede ser penalizado

## Personas involucradas

- Damien Santiago (responsable SEO)
- Pablo Caño (soporte técnico SEO)
