# InmunIA

Inmunología y Alergología con práctica adaptativa, laboratorios y simulación clínica. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/inmunia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24477918.svg)](https://doi.org/10.5281/zenodo.24477918)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Sistema de práctica de la asignatura 1947 Inmunología y Alergología (2.º de Medicina, UMH), construido a partir de su guía docente 2026-2027.

- **Diagnóstico inicial**: una pregunta por cada uno de los 19 resultados de aprendizaje (RA) y las prácticas.
- **Práctica adaptativa**: el dominio de cada RA se estima con un modelo tipo Elo con olvido; cada ítem se repasa con espaciado (cajas 0-1-3-7-16-35 días); los RA se intercalan; los errores cometidos «con seguridad» vuelven antes. Cada actividad muestra por qué se ha elegido.
- **Banco de 73 ítems** (opción múltiple, verdadero/falso, emparejar y ordenar) con feedback elaborado, y **13 generadores de problemas con solución calculada** y diagnóstico de errores típicos: cámara de Neubauer, gel de agarosa, citometría (con ventanas interactivas), HLA, complemento, prick test, espirometría, triptasa, dosis de adrenalina, UAS7, ARIA, control del asma y diagnóstico molecular. Empiezan con un ejemplo resuelto y la ayuda se retira tras dos aciertos seguidos.
- **Simuladores** con predicción previa: déficits del complemento, respuesta primaria y secundaria (adyuvante, déficit de CD40L) y clasificador de Gell y Coombs.
- **Lectura de pruebas** con imágenes sintéticas generadas por código (antebrazo con prick, curvas volumen-tiempo, dot plots, gel).
- **4 casos clínicos** con petición de pruebas, diagnóstico, conducta y errores críticos; **urgencia de anafilaxia** con reloj simulado y puntuación de la cronología.
- **Simulacro** con el formato de la guía: test de Inmunología (con preguntas de prácticas) y de Alergia + prueba complementaria; nota 2/3 + 1/3 sin compensar por debajo de 4,5; vídeo opcional del 10 %.
- **Asistente del vídeo expositivo** (duración estimada, cifras no presentes en el artículo, lista de comprobación) y **tutor socrático** opcional con IA.
- **Progreso**: dominio por RA, calibración, repasos de los próximos 7 días, informe Word, copia JSON y exportación anónima voluntaria.
- **Panel del profesorado**: análisis de la guía, importación de datos anónimos, analítica de ítems (dificultad, discriminación, distractores) con propuestas de mejora, marca de ítems validados y exportación a Moodle XML, GIFT y CSV.

## Ciencia del aprendizaje

Práctica de recuperación (Roediger y Karpicke, 2006, doi:10.1111/j.1467-9280.2006.01693.x; Larsen et al., 2009, doi:10.1111/j.1365-2923.2009.03518.x), espaciado (Cepeda et al., 2006, doi:10.1037/0033-2909.132.3.354), intercalado (Rohrer y Taylor, 2007, doi:10.1007/s11251-007-9015-8), ejemplos resueltos con retirada gradual (Renkl y Atkinson, 2003, doi:10.1207/S15326985EP3801_3), feedback (Hattie y Timperley, 2007, doi:10.3102/003465430298487), hipercorrección de errores con alta confianza (Butterfield y Metcalfe, 2001, doi:10.1037/0278-7393.27.6.1491) y síntesis de Dunlosky et al. (2013, doi:10.1177/1529100612453266). No se ha medido todavía el efecto de esta app.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. No hace falta servidor.

## Privacidad

Todo (progreso, respuestas, casos) se guarda en IndexedDB del navegador. Solo sale información si se usa el tutor, el comentario de un caso o el asistente del vídeo: lo que escribe la persona, con correos, teléfonos y documentos enmascarados, tras un aviso con la muestra exacta. La copia y los datos anónimos no incluyen la clave de IA.

## Límites

- Los ítems, problemas y casos han sido **revisados por el profesorado de la asignatura** (noviembre de 2026); ante discrepancia, manda lo explicado en clase.
- El dominio es una estimación orientativa, no una nota. Los pesos de la prueba complementaria y la penalización por error no constan en la guía (por defecto, 30 % y sin penalización).
- Las imágenes son sintéticas y esquemáticas; no sustituyen a casos reales ni al juicio clínico.
- La IA puede equivocarse: sus citas se verifican por código y nunca pone nota.
- Los datos anónimos no son evidencia por sí solos: investigar con ellos requiere comité de ética (OEP UMH) y consentimiento informado.
- Para adaptarla a otra asignatura se edita `src/curriculum.js` y se ejecuta `python3 build.py` y `node tests/logic_test.js`.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Esther Caparrós Cayuela (Universidad Miguel Hernández de Elche).

Esther Caparrós Cayuela es profesora de la asignatura. Construida a partir de la Guía Docente 2026-2027 de la asignatura 1947 Inmunología y Alergología (Grado en Medicina, UMH).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Esther Caparrós Cayuela [0000-0002-9681-0408](https://orcid.org/0000-0002-9681-0408)

## Cómo citar

Borrás Rocher, F. y Caparrós Cayuela, E. (2026). *InmunIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.24477918](https://doi.org/10.5281/zenodo.24477918)

## Licencia

MIT. Véase [LICENSE](LICENSE).
