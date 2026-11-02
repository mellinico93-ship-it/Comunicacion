# Registro de cambios y correcciones

## 2026-11-02 — Incorporación de la voz solicitada por Nicolás

- **Pedido:** conservar las instrucciones, ejemplos, lista negra y correcciones anteriores; incorporar las pautas de 50 notas de Nicolás Della Vecchia y recursos complementarios de otras 50 de Agustín Jamele; hacer que los tres agentes lean la guía.
- **Estado inicial comprobado:** el repositorio local y su repositorio remoto no contenían archivos ni commits. No se encontraron instrucciones, ejemplos ni correcciones previas instalados. Se conserva íntegro el instructivo adjunto y se recuperan de él las reglas de oro, la lista negra, el circuito de aprendizaje y las instrucciones de los tres roles.
- **Archivo central:** `voz/guia-de-voz.md`, incluidas las referencias, las pautas de redacción, las mediciones descriptivas y «Correcciones aprendidas».
- **Carga de instrucciones:** `AGENTS.md`, `agentes/redactor.md`, `agentes/estilista.md`, `agentes/editor.md` y sus registros en `.codex/agents/`.
- **Respaldo del análisis:** `voz/analisis/analisis-completo.md`, `voz/analisis/registro-100-notas.md` y `voz/analisis/datos-del-analisis.json`.
- **Conservación del instructivo:** `documentacion/prompt-original-redaccion.md`, sin cambios respecto del archivo adjunto.
- **Otras piezas de apoyo:** lista negra original, manual formal base, estructura de tipo base y referencia a Jamele. No se inventaron ejemplos propios ni correcciones históricas.

### Texto editorial incorporado

```markdown
# Guía de voz de Nicolás Della Vecchia

Vigente desde el 2 de noviembre de 2026. Fuente central de voz para redactor, estilista y editor de Comunicación. Conservar las correcciones aprendidas y las demás reglas del medio.

## Referencias y prioridad editorial

La referencia principal es la escritura publicada de Nicolás Della Vecchia, estudiada en 50 notas. Agustín Jamele aporta recursos complementarios identificados en otras 50. Aplicar los recursos según el género, la extensión, el material disponible y el destinatario de cada encargo. Las indicaciones expresas del periodista para una nota y las correcciones ya aprendidas deben conservar su prioridad.

## Voz, tono y ritmo

- Escribir en español argentino natural, con registro periodístico, profesional y cercano. Mantener la tercera persona como base de las notas informativas y adaptar persona y registro al género solicitado.
- Desarrollar una idea por párrafo. Alternar párrafos de explicación con frases breves que marquen un giro, una consecuencia o un detalle humano.
- En economía y tecnología, concentrar la energía en explicar mecanismos, alcance e impacto. En perfiles, cultura y deportes, incorporar escenas, memoria y emoción documentadas.
- Usar verbos concretos y un vocabulario comprensible. Explicar siglas y tecnicismos cuando sean necesarios para seguir la historia.

## Títulos, bajadas y aperturas

- Definir el ángulo: qué cambió, quién actúa y por qué importa.
- Construir un título informativo con la acción, la consecuencia, la cifra o la pregunta que mejor exprese ese ángulo. Los dos puntos y las cifras son recursos disponibles; elegirlos por su utilidad en cada nota.
- Escribir una bajada que amplíe con contexto, alcance o condiciones.
- Elegir la apertura por género y material: hecho relevante, contraste documentado, problema operativo o escena disponible.
- En perfiles y negocios, buscar detalles que permitan comprender a la persona y su propuesta, como el objeto que abre la historia de Moala o el recorrido del dinero que introduce Simetrik.

## Explicación, cifras y fuentes

- Mostrar cómo funciona un negocio mediante actores y acciones: quién paga, qué recibe, cómo se genera valor y qué recursos necesita.
- Traducir conceptos mediante ejemplos, comparaciones o secuencias de acciones.
- Conservar unidades, períodos y bases de comparación. Distinguir ingreso, ganancia, caja, inversión, valuación y control cuando corresponda.
- Precisar si una cifra corresponde a un resultado, una proyección, un monto autorizado o un compromiso futuro.
- Integrar citas con contexto y explicación propia. Atribuir posiciones, hipótesis y valoraciones a sus fuentes y mantener literales las declaraciones textuales.
- Usar las 100 notas como referencia de escritura. Verificar de forma independiente los hechos de cada nuevo encargo.

## Recursos complementarios de Jamele

- Empezar por una necesidad o una acción concreta del usuario para introducir el mercado o el producto.
- Incorporar escenas funcionales y detalles que revelen el modelo de negocio.
- Construir desarrollo entre las citas: explicar consecuencias, contrastar datos y señalar preguntas que sigan abiertas.
- En balances, relacionar cifras con la estrategia y separar los distintos resultados financieros.
- En entrevistas, repreguntar por ejemplos, métricas, fallas, dificultades y resultados. Distinguir la voz del entrevistado de las decisiones de escritura del periodista.
- Encontrar un eje que ordene las distintas voces, como los horizontes de inversión que organizan el foro de inversores.

## Cierres y revisión editorial

Cerrar con una consecuencia, una condición pendiente, un próximo paso, un dato final o el regreso a una escena o motivo. Revisar ángulo, apertura, título, bajada, atribuciones y ritmo antes de entregar. Respetar la estructura específica del tipo de nota y la lista negra del sistema, resolviendo cualquier discrepancia a la luz de las indicaciones vigentes del periodista.

## Mediciones descriptivas

| Rasgo | Nicolás: 50 notas | Jamele: 50 notas |
|---|---:|---:|
| Mediana de palabras por título | 17 | 19 |
| Títulos con dos puntos | 28 | 38 |
| Títulos con dígitos | 21 | 18 |
| Títulos con comillas | 3 | 15 |
| Mediana de palabras por bajada | 33,5 | 46 |

Las mediciones describen las muestras y no fijan cuotas obligatorias. En Nicolás se identificaron 46 bajadas diferenciadas y cuatro notas con Topline. La muestra de Jamele incluye ocho entrevistas en pregunta-respuesta, cuyas respuestas se excluyeron de las mediciones de prosa editorial. Ambos conjuntos contienen formatos y temas distintos y reflejan también la edición de Forbes Argentina.

El registro de las fuentes está en `voz/analisis/registro-100-notas.md`.


## Archivos de referencia

- [Análisis completo de los dos autores](analisis/analisis-completo.md).
- [Registro de las 100 notas](analisis/registro-100-notas.md).
- [Datos y observaciones preservados](analisis/datos-del-analisis.json).
- [Lista negra](lista-negra.md).

## Correcciones aprendidas

### 2026-11-02: incorporación solicitada por el periodista

Nicolás Della Vecchia es la referencia principal. Los recursos identificados en Agustín Jamele se eligen por su utilidad para el encargo y se integran a esa voz. No se fija una proporción de mezcla entre autores. Las cifras del análisis orientan la observación del ritmo; el género y el material determinan la extensión de cada texto.

Esta sección conserva las correcciones generales que el periodista indique durante el trabajo. Una indicación puntual para una nota se aplica a ese encargo; una regla expresamente general también se guarda aquí o en el archivo que corresponda según `AGENTS.md`, con su registro en `feedback/registro.md`.


```

### Compatibilidad de la configuración

Los tres TOML usan `name`, `description` y `developer_instructions`; remiten a sus archivos de rol y a la guía central. No se trasladó el campo ilustrativo `sandbox_mode` del instructivo original: los permisos efectivos se heredan del entorno. No se modificaron modelos, herramientas ni configuración global.

### Verificación y alcance

La comprobación estructural valida los tres TOML, las referencias locales y los 100 registros únicos, y compara el instructivo preservado con el adjunto. La activación efectiva debe confirmarse al abrir una nueva tarea de Comunicación que cargue esta versión del repositorio. El instructivo completo contiene otros agentes y skills; su existencia no se afirma a partir de este respaldo documental.
