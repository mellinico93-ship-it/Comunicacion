Quiero que me armes un sistema de agentes para redactar notas periodísticas usando Codex CLI: subagentes propios, skills y AGENTS.md. Somos periodistas, no programadores: todo lo que crees tiene que poder entenderse y editarse sin saber programar.

Lo más importante del sistema es LA REDACCIÓN. Buscar datos es fácil; lo difícil es que las notas suenen como nosotros y no como una IA. Todo el sistema tiene que girar alrededor de nuestra voz.

Queremos que sea fácil de usar: nada de lo que nos pidas para armar la voz es obligatorio. Si te damos ejemplos, mejor; si no, arrancá con lo que tengas, armá una voz base razonable y seguí. Cuando falte algo que mejoraría mucho el resultado, sugerilo una vez, en una línea, sin frenar el trabajo.

## Antes de empezar: documentación

Antes de crear cualquier archivo, revisá la documentación oficial actual de Codex (developers.openai.com/codex), en especial las secciones de subagentes, skills, AGENTS.md y configuración. Si algún formato de los que describo abajo no coincide con la documentación, seguí la documentación y avisame qué cambiaste.

## Paso 0: entrevistame sobre el medio

Haceme estas preguntas de a pocas, no todas juntas, y esperá mis respuestas:
1. ¿Para qué medio o tipo de medio escribimos? (diario digital, portal local, revista, newsletter, radio...)
2. ¿Qué temas cubrimos más? (política, policiales, deportes, cultura, economía, local...)
3. ¿Quién nos lee? (edad, zona, qué sabe del tema, desde dónde nos lee: celular, newsletter, redes)
4. ¿Tenemos manual de estilo? Si lo tenemos, te lo paso; si no, lo armamos juntos.
5. ¿Qué fuentes usamos seguido? (boletines oficiales, agencias, sitios de gobierno, redes, medios de referencia)
6. ¿Hay cosas que nunca hacemos? (por ejemplo: no nombrar menores, no usar "fuentes cercanas" sin aclarar, etc.)

## Paso 1: construir la voz

Todo este paso es recomendado, no obligatorio. Si en algún momento decimos "seguí" o "después", avanzá con lo que haya.

### 1.1 Tipos de nota
Preguntame qué tipos de nota escribimos. Proponé esta lista y dejame agregar otros; si no respondemos, usá noticia dura, breve y crónica como base:
- Noticia dura o de último momento
- Breve
- Crónica
- Perfil
- Entrevista (pregunta y respuesta, o narrada)
- Análisis o explicador ("qué pasó y por qué importa")
- Opinión o columna
- Cobertura en vivo o minuto a minuto
- Investigación

Si queremos, contanos para cada tipo el largo habitual, la estructura (volanta, título, bajada, intertítulos, recuadros), cómo arranca el primer párrafo y cómo suele cerrar. Si no, proponé valores típicos y los ajustamos con el uso.

### 1.2 Ejemplos (recomendado)
Sugerinos pasar ejemplos, explicando en una línea que es lo que más mejora la voz. Todo es opcional; lo que no nos pases, lo salteás:
1. **Notas nuestras publicadas**: lo ideal son unas 3 por tipo de nota, pero con una sola ya sirve. Pueden ser links o texto pegado. Guardalas en `voz/ejemplos/<tipo>/`.
2. **Notas que nos gustan de otros medios o autores** (2 a 5), y que te digamos qué nos gusta de cada una. Guardalas en `voz/referentes/` con nuestro comentario.
3. **Notas que NO queremos parecernos** (1 a 3), y por qué. Guardalas en `voz/anti-ejemplos/` con nuestro comentario.
4. **Un párrafo escrito por nosotros sin editar**, contando algo cualquiera como se lo contaríamos a un amigo. Sirve para captar el registro natural.

Si no tenemos ejemplos o los pasamos después, no pasa nada: armá la guía con lo que te contamos y dejá anotado en `voz/guia-de-voz.md` que es una versión base. Cada vez que agreguemos ejemplos, actualizala.

### 1.3 Analizá la voz
Armá `voz/guia-de-voz.md`. Tiene que ser concreta y medible, no adjetivos vagos como "claro y ágil". Si hay ejemplos nuestros, poné una cita textual como ejemplo de cada rasgo; si no, proponé el rasgo a partir de nuestras respuestas:
- **Registro y tono**: voseo, tuteo o neutro; nivel de formalidad; cuánto humor o ironía; cercanía con el lector.
- **Oraciones**: largo promedio, cuánto varían, uso de oraciones cortas para golpear.
- **Párrafos**: cuántas oraciones suelen tener y cómo se encadenan.
- **Primer párrafo**: cómo arrancamos (dato duro, escena, cita, pregunta) según el tipo de nota.
- **Cierre**: cómo terminamos (dato, cita, proyección, escena); qué cierres no usamos.
- **Citas**: cuántas, de qué largo, cómo las introducimos, qué verbos de atribución usamos ("dijo", "afirmó", "sostuvo"...) y cuáles no.
- **Vocabulario**: palabras y giros que sí usamos, regionalismos, siglas y cómo las presentamos.
- **Adjetivos y adverbios**: cuánto los usamos y de qué tipo.
- **Datos y cifras**: cómo los presentamos (redondeo, comparaciones, contexto).
- **Títulos y bajadas**: largo, estructura, si llevan verbo, si usan dos puntos o preguntas.
- **Lo que nos diferencia** de los referentes y de los anti-ejemplos.

Armá también un archivo por tipo de nota, `voz/tipos/<tipo>.md`, con la estructura y los rasgos propios de ese tipo. Si hay una nota nuestra de ese tipo, sumá un ejemplo anotado, con comentarios al margen que expliquen por qué funciona.

### 1.4 Lista negra
Armá `voz/lista-negra.md` con lo que nunca tiene que aparecer:
- Muletillas típicas de texto generado por IA: "en un mundo cada vez más...", "cabe destacar", "es importante señalar", "sin lugar a dudas", "en este contexto", "un antes y un después", "no solo... sino también" usado en todas las notas, enumeraciones de a tres por costumbre, cierres moralizantes o de resumen ("en definitiva...", "el tiempo dirá"), exceso de guiones largos, signos de exclamación, adjetivos grandilocuentes ("histórico", "crucial", "clave") sin justificación.
- Lo que nosotros señalemos en los anti-ejemplos.
- Lo que vayamos agregando con el uso.

### 1.5 Probá la voz (opcional)
Ofrecenos hacer una prueba rápida; si decimos que no, seguí al paso 2.
1. Elegí un hecho real reciente y escribí el primer párrafo en 3 versiones distintas siguiendo la guía.
2. Preguntanos cuál suena más a nosotros y qué cambiaríamos.
3. Ajustá la guía con lo que digamos y anotá cada corrección en una sección "Correcciones aprendidas" al final de `voz/guia-de-voz.md`.
4. Podemos repetir hasta 3 rondas si queremos.

## Paso 2: estructura de carpetas

```
.
├── AGENTS.md                      ← contexto general del proyecto y reglas de oro
├── manual-de-estilo.md            ← reglas formales (ortografía, siglas, números, cargos)
├── fuentes-confiables.md          ← lista de fuentes por tema, editable por nosotros
├── LEEME.md                       ← guía de uso para nosotros, en castellano simple
├── voz/                           ← EL CORAZÓN DEL SISTEMA
│   ├── guia-de-voz.md
│   ├── lista-negra.md
│   ├── tipos/<tipo>.md
│   ├── ejemplos/<tipo>/           ← nuestras notas publicadas
│   ├── referentes/                ← notas de otros que nos gustan, con comentario
│   └── anti-ejemplos/             ← notas a las que no queremos parecernos, con comentario
├── agentes/                       ← instrucciones de cada agente en texto común
│   ├── investigador.md
│   ├── redactor.md
│   ├── verificador.md
│   ├── estilista.md
│   └── editor.md
├── .codex/
│   ├── config.toml                ← solo si hace falta (por ejemplo, para habilitar búsqueda web)
│   └── agents/
│       ├── investigador.toml
│       ├── redactor.toml
│       ├── verificador.toml
│       ├── estilista.toml
│       └── editor.toml
├── .agents/
│   └── skills/
│       ├── nota/SKILL.md          ← flujo completo
│       ├── investigar/SKILL.md    ← solo investigación
│       ├── verificar/SKILL.md     ← verificar una nota ya escrita
│       ├── pulir/SKILL.md         ← pasar una nota nuestra por el estilista
│       ├── aprender-voz/SKILL.md  ← aprender de nuestras correcciones
│       ├── desgrabar/SKILL.md     ← procesar una entrevista transcripta
│       └── redes/SKILL.md         ← adaptar una nota a redes o newsletter
├── investigaciones/               ← lo que juntan los investigadores
├── borradores/                    ← versiones intermedias
├── notas/                         ← notas finales que entrega el sistema
├── publicadas/                    ← la versión que realmente publicamos, después de editarla nosotros
├── feedback/
│   └── registro.md                ← cada corrección que hicimos y en qué archivo quedó
└── entrevistas/                   ← transcripciones que subimos nosotros
```

Las instrucciones completas de cada agente van en `agentes/<nombre>.md`. El archivo `.codex/agents/<nombre>.toml` solo define el agente y en `developer_instructions` le dice que lea y siga `agentes/<nombre>.md`. Así podemos editar cada agente en un archivo de texto común y, si algún día usamos otra herramienta, reutilizamos los mismos archivos.

## Paso 3: reglas de oro

Van en AGENTS.md y se repiten en cada agente donde corresponda:
- NUNCA inventar citas, datos, cifras, fechas, nombres ni fuentes.
- Toda afirmación factual lleva su fuente con link. Si no hay fuente, se marca como [SIN FUENTE] y no se presenta como hecho.
- Las citas textuales van entre comillas y tienen que coincidir palabra por palabra con la fuente. Mejorar la redacción nunca justifica tocar una cita.
- Distinguir siempre entre hecho confirmado, declaración de alguien y versión no confirmada.
- La voz manda: todo texto que se escriba sigue `voz/guia-de-voz.md` y evita `voz/lista-negra.md`.
- Nuestras correcciones no se pierden: cada vez que corregimos algo, se guarda en el archivo que corresponde según el circuito de mejora (paso 6), para que no tengamos que repetirlo.
- La nota final SIEMPRE la revisa y publica una persona. El sistema produce borradores, no publica.
- Si algo no se pudo confirmar, se dice explícitamente; no se rellena.

## Paso 4: los agentes

Cada agente se define con un archivo TOML en `.codex/agents/` con este formato:

```toml
name = "<nombre>"
description = "<cuándo usarlo, claro y específico>"
sandbox_mode = "<read-only o el permiso de escritura que corresponda>"

developer_instructions = """
Leé y seguí al pie de la letra las instrucciones de agentes/<nombre>.md.
Antes de empezar, leé también AGENTS.md y los archivos que esas instrucciones indiquen.
"""
```

Cada subagente arranca sin ver la conversación principal, así que sus instrucciones en `agentes/<nombre>.md` tienen que ser autosuficientes: rol, qué leer primero, pasos, formato de salida y qué NO hacer. No copies la guía de voz ni el manual adentro de los agentes: que los lean de sus archivos, así los actualizamos en un solo lugar.

### investigador
- Permisos: lectura y búsqueda web. Solo puede escribir en `investigaciones/`; si el sandbox no lo permite, que devuelva el resultado y lo guarde el orquestador.
- Recibe un tema y un ÁNGULO específico (por ejemplo: datos oficiales, antecedentes, voces y repercusiones). Se puede lanzar varias veces en paralelo, con un ángulo distinto cada vez.
- Prioriza las fuentes de `fuentes-confiables.md`.
- Devuelve hechos con link, citas textuales con link y con quién lo dijo y cuándo, cifras con fuente, contradicciones entre fuentes y preguntas abiertas.
- Además, busca material que le sirva al redactor para escribir con color: escenas, detalles concretos, contexto humano, comparaciones que ayuden a entender las cifras. Siempre con fuente.
- Formato del archivo: `investigaciones/<fecha>-<tema>-<angulo>.md`.
- No redacta la nota.

### redactor (el agente más importante)
- Permisos: lectura y escritura en `borradores/`.
- Antes de escribir, SIEMPRE lee en este orden:
  1. `voz/guia-de-voz.md`, incluida la sección "Correcciones aprendidas".
  2. `voz/tipos/<tipo>.md` del tipo de nota que le pidieron.
  3. Hasta 2 notas de `voz/ejemplos/<tipo>/`, si hay, para tener la voz "en el oído".
  4. `voz/lista-negra.md`.
  5. `manual-de-estilo.md`.
- Si no le dicen el tipo de nota, elige el más adecuado según el tema y lo aclara al principio del borrador.
- Escribe a partir del material de investigación, con la estructura del tipo de nota.
- Cada dato lleva una marca de fuente al lado, por ejemplo [F1], con la lista de fuentes al final.
- Solo usa información del material de investigación; si falta algo, lo deja señalado como [FALTA: ...].
- Antes de entregar, se autorrevisa: busca cada frase de la lista negra y la reescribe, compara el primer párrafo y el cierre con los ejemplos, y revisa que el largo de oraciones y párrafos coincida con la guía.
- Guarda en `borradores/<fecha>-<tema>-v<N>.md`.

### verificador
- Permisos: read-only, con búsqueda web.
- No escribió la nota y no confía en ella.
- Revisa cada afirmación, cifra, fecha y cita contra la fuente original, abriendo los links.
- Devuelve una tabla: afirmación | fuente | estado (✅ verificada / ⚠️ dudosa / ❌ falsa o sin fuente) | comentario.
- Señala también sesgos, opiniones presentadas como hechos y problemas legales evidentes (acusaciones sin sustento, datos de menores, etc.).
- No corrige la nota: solo reporta.

### estilista (guardián de la voz)
- Permisos: read-only.
- No escribió la nota. Su único trabajo es la voz: no toca datos, no toca citas y no opina sobre el contenido.
- Lee `voz/guia-de-voz.md`, `voz/lista-negra.md`, `voz/tipos/<tipo>.md` y, si hay, 2 o 3 notas de `voz/ejemplos/<tipo>/`.
- Lee el borrador y responde: ¿esto podría haberlo escrito alguien del equipo? Da un puntaje de 1 a 10 con justificación.
- Marca frase por frase lo que suena a IA o no suena a nosotros. Para cada una: la frase original, qué rasgo de la guía rompe y una propuesta de reescritura.
- Revisa especialmente el primer párrafo, el cierre, el título y la bajada.
- Devuelve el reporte; no edita el archivo.

### editor
- Permisos: lectura y escritura en `notas/`.
- Toma el borrador ya verificado y pulido, y propone 3 opciones de título y bajada siguiendo `voz/guia-de-voz.md`, más volanta e intertítulos si corresponde.
- Ajusta el largo según el tipo de nota y revisa ortografía y reglas de `manual-de-estilo.md`.
- No agrega información nueva y no cambia la voz.
- Guarda la versión final en `notas/<fecha>-<tema>.md`, con la tabla de verificación y la lista de fuentes al final.

## Paso 5: las skills

Cada skill es una carpeta en `.agents/skills/<nombre>/` con un `SKILL.md` que tiene su `name` y `description` en el encabezado, según el formato de la documentación. La `description` tiene que dejar claro cuándo usarla.

IMPORTANTE: Codex lanza subagentes solo cuando se le pide explícitamente. Por eso cada skill tiene que nombrar a cada subagente y decir cuándo lanzarlo, con frases del tipo "lanzá el subagente `verificador` con este borrador". No dejes nada librado a que lo deduzca.

### nota (recibe un tipo de nota y un tema, por ejemplo: "crónica: la feria de los domingos en el centro")
El tipo de nota es opcional: si no viene, elegí el más adecuado y decilo en el resumen final. También tiene que andar con solo el tema, por ejemplo "nota: paro de colectivos". Flujo completo, en este orden y sin saltear pasos:
1. Elegí 2 o 3 ángulos según el tema y el tipo de nota, y lanzá un subagente `investigador` por cada ángulo, EN PARALELO.
2. Esperá a que terminen todos, juntá los resultados y lanzá el subagente `redactor` con ese material y el tipo de nota.
3. Lanzá el subagente `verificador` con el borrador.
4. Si hay ⚠️ o ❌, lanzá de nuevo el `redactor` con el borrador y el reporte para corregir. Máximo 2 vueltas; si siguen los problemas, frená y avisanos.
5. Lanzá el subagente `estilista` con el borrador verificado y el tipo de nota.
6. Si el puntaje del estilista es menor a 8, lanzá el `redactor` con el reporte del estilista para reescribir solo lo marcado, sin tocar datos ni citas. Máximo 2 vueltas.
7. Lanzá el subagente `editor`.
8. Al final mostrá un resumen corto: dónde quedó la nota, cuántos datos se verificaron, el puntaje de voz final y qué quedó pendiente o dudoso.

### investigar (recibe un tema)
Solo el paso 1 de `nota`, sin redactar. Sirve cuando queremos escribir nosotros.

### verificar (recibe la ruta de una nota)
Lanzá el subagente `verificador` sobre una nota que escribimos nosotros y mostranos la tabla.

### pulir (recibe la ruta de una nota y su tipo)
Lanzá el subagente `estilista` sobre una nota nuestra y mostranos el reporte. No reescribas la nota salvo que lo pidamos.

### aprender-voz (recibe la ruta de una nota de `notas/` y la de su versión publicada en `publicadas/`)
Es opcional, pero es lo que hace que la voz mejore con el uso. Si nos pasa solo la nota publicada, buscá vos la versión correspondiente en `notas/`:
1. Compará lo que entregó el sistema con lo que publicamos nosotros, frase por frase.
2. Detectá patrones en nuestros cambios: qué palabras sacamos, cómo reescribimos el primer párrafo, qué cortamos, qué agregamos, cómo cambiamos el título.
3. Proponé reglas nuevas para `voz/guia-de-voz.md` (sección "Correcciones aprendidas") y frases nuevas para `voz/lista-negra.md`, cada una con el ejemplo de antes y después.
4. Mostranos las propuestas y aplicá solo las que aprobemos.
5. Copiá la nota publicada a `voz/ejemplos/<tipo>/`, así el banco de ejemplos crece.

### desgrabar (recibe la ruta de una transcripción en `entrevistas/`)
Devuelve un resumen, las 5 a 10 citas más fuertes (textuales, con contexto), posibles ángulos de nota y los datos a chequear. No inventa ni retoca citas.

### redes (recibe la ruta de una nota final)
Adapta la nota a un posteo para X, uno para Instagram, un hilo y un párrafo para newsletter, respetando la voz de `voz/guia-de-voz.md`. No agrega información que no esté en la nota.

## Paso 6: el circuito de mejora (feedback loop)

El sistema tiene que mejorar con cada nota sin que tengamos que acordarnos de nada. Escribí estas reglas en AGENTS.md, porque las aplica el orquestador (la conversación principal), no los subagentes.

### 6.1 Mapa: qué se corrige dónde
Incluí esta tabla en AGENTS.md. Es lo que usa el orquestador para saber en qué archivo guardar cada corrección:

| Si la corrección es sobre... | Se guarda en... |
|---|---|
| Cómo suena: tono, ritmo, largo de oraciones, registro | `voz/guia-de-voz.md`, sección "Correcciones aprendidas" |
| Una palabra o frase que no queremos ver nunca más | `voz/lista-negra.md` |
| La estructura o el largo de un tipo de nota | `voz/tipos/<tipo>.md` |
| Ortografía, siglas, números, cargos, mayúsculas | `manual-de-estilo.md` |
| Una fuente que conviene usar o evitar | `fuentes-confiables.md` |
| Cómo busca información (qué ángulos, qué profundidad) | `agentes/investigador.md` |
| Cómo escribe el borrador (más allá de la voz) | `agentes/redactor.md` |
| Qué chequear o qué tan estricto ser con los datos | `agentes/verificador.md` |
| Cómo evalúa la voz o qué tan exigente es el puntaje | `agentes/estilista.md` |
| Títulos, bajadas, intertítulos, largo final | `agentes/editor.md` |
| El orden de los pasos o cuántas vueltas se hacen | `.agents/skills/<skill>/SKILL.md` |
| Una regla general que vale para todo | `AGENTS.md` |

Si una corrección toca dos cosas, se guarda en los dos archivos. Si no queda claro dónde va, preguntá en una línea dando las dos opciones más probables.

### 6.2 Cuando corregimos algo durante el trabajo
Cada vez que digamos algo como "no uses esa palabra", "esto es muy largo", "nosotros no arrancamos así" o "esa fuente no sirve":
1. Aplicá la corrección a la nota en curso.
2. Si no es obvio, preguntá en una línea: "¿Esto es solo para esta nota o lo anoto para siempre?". Si la corrección es claramente general ("nunca...", "siempre...", "nosotros no..."), no preguntes: anotala.
3. Ubicá el archivo correcto con la tabla 6.1 y agregá la regla escrita en positivo, concreta y con un ejemplo de antes y después tomado de la nota.
4. Antes de agregarla, revisá que no contradiga una regla que ya existe. Si la contradice, mostranos las dos y preguntá cuál queda.
5. Avisá en una línea dónde quedó, por ejemplo: "Anotado en voz/lista-negra.md: no usar 'en el marco de'".
6. Registralo en `feedback/registro.md` con fecha, la corrección, el archivo que cambió y el texto agregado, así podemos revisarlo o deshacerlo.

### 6.3 Al terminar cada nota
Después de entregar la nota final, hacé una ronda corta de preguntas. Es opcional: si respondemos "ok", "nada" o seguimos con otra cosa, no insistas.
- Hacé como máximo 3 preguntas, elegidas según lo que haya pasado en esta nota. Por ejemplo: ¿el arranque suena a ustedes?, ¿el título lo usarían o lo cambiarían?, ¿hay alguna frase que no dirían?, ¿faltó algún dato o alguna fuente?
- Priorizá las partes donde el estilista o el verificador marcaron dudas.
- Cada respuesta pasa por el proceso de 6.2: se aplica, se guarda en el archivo que corresponde y se registra.

### 6.4 Al empezar cada sesión
- Si hay notas en `publicadas/` que todavía no pasaron por `aprender-voz` (fijate en `feedback/registro.md`), ofrecé correrlo en una línea.
- Si `feedback/registro.md` tiene 15 entradas o más desde la última limpieza, ofrecé ordenar: juntar reglas repetidas, resolver contradicciones y pasar a la guía principal las correcciones que se repiten. Mostranos los cambios antes de aplicarlos.

### 6.5 Límites
- Nunca se borra una regla sin preguntarnos.
- Las correcciones nunca habilitan a inventar datos ni a tocar citas: las reglas de oro están por encima de todo.
- Las reglas nuevas se escriben cortas y concretas. Nada de "escribir mejor"; sí "el primer párrafo no pasa de 40 palabras".

## Paso 7: configuración

- Verificá que la búsqueda web esté habilitada para los subagentes que la necesitan. Si hace falta tocar `.codex/config.toml` o la configuración global, decime exactamente qué cambiar y por qué antes de hacerlo.
- No toques configuración fuera de esta carpeta sin preguntarme.

## Paso 8: LEEME.md

Escribí una guía corta, en castellano simple, para gente no técnica:
- Cómo abrir Codex en esta carpeta y cómo invocar cada skill, con ejemplos concretos de lo que hay que escribir.
- Cómo funciona la voz: qué hay en la carpeta `voz/` y por qué es lo más importante.
- Un "Uso rápido" al principio: con escribir `nota: <tema>` alcanza; todo lo demás es opcional.
- Consejos para que suene más a nosotros (recomendados, no obligatorios): sumar notas propias a `voz/ejemplos/`, indicar el tipo de nota y, después de publicar, guardar la versión publicada en `publicadas/` y correr `aprender-voz`.
- Cómo funciona el circuito de mejora: cuando corregimos algo queda guardado; al terminar cada nota Codex pregunta qué mejorar, y podemos ver todo lo que aprendió en `feedback/registro.md`.
- Cómo deshacer una regla que no nos gustó.
- Cómo agregar ejemplos nuevos o una frase a la lista negra a mano.
- Cómo editar el manual de estilo, la lista de fuentes o el comportamiento de un agente: qué archivo tocar y qué parte.
- Qué hacer si un subagente no se lanza o da error.
- Recordatorio: todo es borrador y lo revisa una persona antes de publicar.

## Paso 9: prueba

Cuando termines de crear todo:
1. Corré la skill `nota` con un tema de actualidad real, fácil de verificar, usando el tipo de nota que más escribimos.
2. Mostrame qué subagentes se lanzaron y en qué orden, el resultado de la verificación, el reporte del estilista y la nota final.
3. Si hay notas nuestras del mismo tipo en `voz/ejemplos/`, poné una al lado para que comparemos la voz.
4. Hacé la ronda de preguntas del paso 6.3 y, con lo que respondamos, mostrá cómo quedó guardado cada cambio y en qué archivo.
5. Decime qué falló, si algo falló, y qué ajustarías.

Trabajá de forma modular: cada agente tiene una sola responsabilidad, así después podemos agregar o cambiar uno sin tocar los demás.
