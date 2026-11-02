# Redacción en Comunicación

Las pautas de voz están guardadas en este repositorio. Las tareas de Codex que abran el proyecto y lean `AGENTS.md` deben cargar la guía antes de escribir. Los cambios guardados en el repositorio acompañan al proyecto entre tareas.

## Uso rápido

Podés pedir: «Redactá un explicador sobre este tema con el material que te paso. Leé la guía de voz antes de empezar». Indicá el tipo de nota o el largo cuando sea relevante.

Para comprobar la configuración en una tarea nueva: «Leé AGENTS.md y decime qué guía de voz estás usando, quién es la referencia principal y qué correcciones aprendidas encontraste». Si falta un archivo, el agente debe indicarlo.

## Dónde queda cada cosa

- `voz/guia-de-voz.md`: voz de Nicolás Della Vecchia, con recursos complementarios de Agustín Jamele y correcciones aprendidas.
- `voz/lista-negra.md`: muletillas y giros que evitamos, conservados del instructivo original.
- `voz/analisis/analisis-completo.md`: informe y 100 observaciones individuales.
- `voz/analisis/registro-100-notas.md`: enlaces de las 50 notas de cada autor.
- `voz/analisis/datos-del-analisis.json`: respaldo estructurado de observaciones, métricas y metadatos, sin cuerpos completos de artículos.
- `agentes/`: instrucciones del redactor, estilista y editor. Sus registros de Codex están en `.codex/agents/`.
- `manual-de-estilo.md` y `voz/tipos/base.md`: reglas formales y estructura base, editables según las preferencias del medio.
- `feedback/registro.md`: qué se incorporó, cuándo y dónde.
- `documentacion/prompt-original-redaccion.md`: copia íntegra del instructivo que suministraste.

## Cómo conservar lo que aprendemos

Las correcciones claramente generales se aplican a la nota y se guardan en el archivo que corresponde según `AGENTS.md`. Las indicaciones puntuales se aplican al encargo. Si el alcance es ambiguo, el agente lo consulta. Cada cambio general se registra en `feedback/registro.md`.

Podés sumar tus notas publicadas en `voz/ejemplos/<tipo>/`. En esta incorporación no se encontraron ejemplos previos en el repositorio y no se inventaron notas para completar la carpeta. Las referencias a Jamele están separadas de los ejemplos propios.

Para revisar o deshacer una regla, buscá su entrada en `feedback/registro.md` y pedí el cambio concreto. Conservá los cambios autorizados en el repositorio para que otras tareas reciban la misma versión.

## Alcance de esta incorporación

El repositorio estaba vacío. Se guardaron la voz, el análisis y las instrucciones de los tres agentes solicitados, recuperando del instructivo las reglas anteriores disponibles. El instructivo también describe investigador, verificador y skills de trabajo; esos componentes no se declaran instalados por el hecho de conservar el documento. No se publica ninguna nota ni se modifica configuración global.

Los permisos y herramientas de los tres agentes se heredan del entorno de Codex. Si el entorno no reconoce un agente personalizado, revisá que la tarea haya cargado esta versión del repositorio; las mismas instrucciones también están disponibles en sus archivos de texto.

La comprobación estructural no equivale a una ejecución de los agentes. Al abrir una nueva tarea en Comunicación, verificá la lectura de `AGENTS.md` y `voz/guia-de-voz.md` con la consulta de uso rápido. Una persona revisa siempre los borradores antes de publicar.
