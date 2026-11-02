# Redacción en Comunicación

Las pautas de voz están guardadas en este repositorio. Las tareas de Codex que abran el proyecto y lean `AGENTS.md` deben cargar la guía antes de escribir. Los cambios guardados en el repositorio acompañan al proyecto entre tareas.

## Uso rápido

Podés pedir: «Redactá un explicador sobre este tema con el material que te paso. Leé la guía de voz antes de empezar». Indicá el tipo de nota o el largo cuando sea relevante.

Para comprobar la configuración en una tarea nueva: «Leé AGENTS.md y decime qué guía de voz estás usando, quién es la referencia principal y qué correcciones aprendidas encontraste». Si falta un archivo, el agente debe indicarlo.

## Dónde queda cada cosa

- `voz/guia-de-voz.md`: voz editorial que integra recursos de Nicolás Della Vecchia, Agustín Jamele y Laura Mafud, con las correcciones aprendidas.
- `voz/lista-negra.md`: muletillas y giros que evitamos, conservados del instructivo original.
- `voz/analisis/analisis-completo.md`: informe anterior de Nicolás y Agustín.
- `voz/analisis/laura-mafud-50-notas.md`: informe de Laura y criterios de integración.
- `voz/analisis/registro-laura-mafud-50-notas.md`: 50 observaciones individuales de Laura.
- `voz/analisis/registro-150-notas.md`: índice conjunto de las tres referencias.
- `voz/analisis/registro-100-notas.md`: enlaces de las 50 notas de cada autor.
- `voz/analisis/datos-del-analisis.json`: respaldo estructurado de observaciones, métricas y metadatos, sin cuerpos completos de artículos.
- `agentes/`: instrucciones del investigador, redactor, verificador, estilista y editor. Sus registros de Codex están en `.codex/agents/`.
- `fuentes-confiables.md`: prioridades y fuentes iniciales para investigar y verificar.
- `manual-de-estilo.md` y `voz/tipos/base.md`: reglas formales y estructura base, editables según las preferencias del medio.
- `feedback/registro.md`: qué se incorporó, cuándo y dónde.
- `documentacion/prompt-original-redaccion.md`: copia íntegra del instructivo que suministraste.

## Cómo conservar lo que aprendemos

Las correcciones claramente generales se aplican a la nota y se guardan en el archivo que corresponde según `AGENTS.md`. Las indicaciones puntuales se aplican al encargo. Si el alcance es ambiguo, el agente lo consulta. Cada cambio general se registra en `feedback/registro.md`.

Podés sumar tus notas publicadas en `voz/ejemplos/<tipo>/`. En esta incorporación no se encontraron ejemplos previos en el repositorio y no se inventaron notas para completar la carpeta. Las referencias a Jamele y Mafud están separadas de los ejemplos propios. La guía combina recursos de los tres autores según el tipo de nota y el material disponible; no fija porcentajes de mezcla.

Para revisar o deshacer una regla, buscá su entrada en `feedback/registro.md` y pedí el cambio concreto. Conservá los cambios autorizados en el repositorio para que otras tareas reciban la misma versión.

## Alcance de esta incorporación

El repositorio estaba vacío. Primero se guardaron la voz, el análisis y las instrucciones del redactor, estilista y editor. Después se incorporaron investigador y verificador con las instrucciones del prompt original. Ahora están definidos los cinco agentes. El instructivo también describe skills de trabajo; su instalación sigue pendiente. No se publica ninguna nota ni se modifica configuración global.

Los permisos y herramientas de los cinco agentes se heredan del entorno de Codex. Investigador y verificador usan la búsqueda web disponible; si no tienen acceso a una fuente, lo informan. Si el entorno no reconoce un agente personalizado, revisá que la tarea haya cargado esta versión del repositorio; las mismas instrucciones también están disponibles en sus archivos de texto.

Para una investigación puntual podés pedir: «Lanzá el agente investigador sobre este tema, con este ángulo». Para revisar una nota: «Lanzá el agente verificador con este borrador y sus fuentes». El orden previsto para una nota completa es investigador, redactor, verificador, estilista y editor. Las skills que automatizan ese circuito todavía no están instaladas.

La comprobación estructural no equivale a una ejecución de los agentes. Al abrir una nueva tarea en Comunicación, verificá la lectura de `AGENTS.md` y `voz/guia-de-voz.md` con la consulta de uso rápido. Una persona revisa siempre los borradores antes de publicar.
