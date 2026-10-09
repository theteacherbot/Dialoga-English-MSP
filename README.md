# DIALOGA English MSP

**Herramienta web interactiva para desarrollar la producción e interacción oral en inglés mediante el «Modelo de Microdiálogos Situacionales Progresivos (MSP)».**

Genera microdiálogos en inglés con **2 o 3 interlocutores** ambientados en situaciones cotidianas y, para cada situación, produce **tres versiones del mismo escenario**. Lo que cambia entre versiones no es el vocabulario: es la **demanda cognitiva y comunicativa**.

Trae **42 situaciones listas para usar** (126 microdiálogos: 42 × 3 niveles) repartidas en 6 categorías, desde la vida diaria y los servicios hasta el conflicto y la negociación, pasando por la vida escolar y la proyección profesional.

> **Principio pedagógico clave:** el diálogo **no es el producto final**, es el **andamiaje** hacia la comunicación espontánea.
> Secuencia: `Contexto → Modelo → Comprensión → Práctica guiada → Sustitución → Personalización → Interacción → Improvisación → Producción espontánea`.

---

## Tabla de contenidos

- [Lo que hace](#lo-qué-hace)
- [Cómo se usa](#cómo-se-usa)
- [Los tres niveles](#los-tres-niveles)
- [Las 9 fases de cada nivel](#las-9-fases-de-cada-nivel)
- [Situaciones incluidas](#situaciones-incluidas)
- [Guía docente y rúbrica](#guía-docente-y-rúbrica)
- [Guardar, compartir e importar](#guardar-compartir-e-importar)
- [API key y flujo BYOP](#api-key-y-flujo-byop)
- [Requisitos y arranque](#requisitos-y-arranque)
- [Arquitectura](#arquitectura)
- [Detalles técnicos de la API](#detalles-técnicos-de-la-api)
- [Scripts y pruebas](#scripts-y-pruebas)
- [Solución de problemas](#solución-de-problemas)
- [Privacidad y seguridad](#privacidad-y-seguridad)

---

## Lo que hace

- **42 situaciones listas para usar** repartidas en 6 categorías, cada una con sus tres niveles completos. Funcionan **sin conexión y sin API key**, son instantáneas y sirven de referencia del modelo.
- **Catálogo filtrable**: chips por categoría y buscador que entiende español e inglés, para encontrar la situación en segundos.
- **Generación con IA** de cualquier situación que escribas (en español o en inglés), también con los tres niveles completos.
- **Vista lado a lado** de los tres niveles para que el estudiante *vea* su progresión, o **pestañas** para trabajar uno a uno.
- **Modo práctica**: oculta las líneas de un personaje para que el estudiante las produzca, con botón para revelarlas de una en una.
- **Lectura en voz alta** del diálogo completo o de una línea suelta (SpeechSynthesis del navegador).
- **Ilustración de la escena** generada por IA, con indicador de carga y respaldo amable si falla.
- **Copiar, descargar en `.txt` e imprimir** el material (con hoja de estilos de impresión para el plan de aula).
- **Diagnóstico integrado** con 20 comprobaciones ejecutables desde la propia página.
- **Guía docente por nivel**: rúbrica de evaluación oral y secuencia de sesión minuto a minuto, lista para imprimir.
- **Biblioteca local**: guarda los microdiálogos que generes y recupéralos cuando quieras.
- **Compartir por enlace**: el microdiálogo viaja dentro del propio enlace (comprimido), sin servidor ni API key. También exporta e importa `.json`.

---

## Cómo se usa

1. Abre `microdialogos-msp.html` en el navegador.
2. **Elige una situación** del catálogo (instantánea, sin coste) o **escribe la tuya**. Ajusta **2 o 3 interlocutores** y, si quieres, el modelo de IA.
3. Pulsa **✨ Generar los tres niveles**. Con el catálogo es inmediato; con IA suele tardar entre 15 y 60 segundos.
4. Muévete entre **🟢 / 🟡 / 🔴** o pulsa **👁️ Ver los tres niveles** para comparar la progresión.
5. Activa **🎭 Modo práctica** y elige el personaje cuyas líneas se ocultarán.
6. Usa **🔊 Escuchar diálogo** para modelar la pronunciación.
7. Baja hasta **👩‍🏫 Guía docente** para la rúbrica y la secuencia de sesión, y pulsa **🖨️ Imprimir guía**.
8. Lleva el material al aula con **📋 Copiar todo**, **⬇️ Descargar .txt** o **🖨️ Imprimir**; guarda lo que quieras conservar con **💾 Guardar** y compártelo con **🔗 Compartir**.

> **Atajo:** pulsando **🧪 Diagnóstico** en la barra superior la propia herramienta se autocomprueba delante de ti.

---

## Los tres niveles

| Nivel | Lema | CEFR | Interacción esperada |
|---|---|---|---|
| 🟢 `survival` | **I can say it** | A1–A2 | Reproducir → sustituir → responder |
| 🟡 `functional` | **I can interact** | A2–B1 | Adaptar → ampliar → negociar significado |
| 🔴 `communicative` | **I can improvise** | B1–B2 | Interpretar → reaccionar → construir significado |

**Ejemplo de progresión («En el restaurante»), idéntico escenario en los tres casos:**

- 🟢 Pedir una hamburguesa y una bebida con estructuras modelo.
- 🟡 Preguntar ingredientes, declarar una restricción alimentaria, cambiar el plato y justificar con conectores.
- 🔴 El plato llega equivocado: queja razonada, dos soluciones sobre la mesa y negociación de una compensación.

---

## Las 9 fases de cada nivel

| # | Fase | Qué aporta |
|---|---|---|
| 1 | **Contexto** | Sitúa la escena y el propósito comunicativo. |
| 2 | **Modelo** | El diálogo ejemplar: input comprensible y modelado. |
| 3 | **Comprensión** | Preguntas literales **e inferenciales**. |
| 4 | **Práctica guiada** | Marcos de frase y ejemplo para producir con apoyo. |
| 5 | **Sustitución** | Cambiar un elemento del patrón y volver a producir. |
| 6 | **Personalización** | Llevar el lenguaje a la vida real del estudiante. |
| 7 | **Interacción** | Role-play entre iguales con tarea comunicativa. |
| 8 | **Improvisación** | Giro inesperado: obliga a reaccionar sin guion. |
| 9 | **Producción espontánea** | Transferencia a una situación nueva y auténtica. |

Cada nivel añade además **lenguaje clave**, **foco de pronunciación**, **errores frecuentes** de hispanohablantes y **notas para el docente**.

---

## Situaciones incluidas

**42 escenarios**, todos con sus tres niveles completos (126 microdiálogos). El reparto procede del cuadro de escenarios del proyecto (`escenarios_microdialogos_MSP.xlsx`) y respeta sus criterios de selección: equilibra funciones comunicativas (pedir, informar, narrar, opinar, quejarse, negociar, disculparse y planear), alterna **23 escenarios con 2 interlocutores y 19 con 3** —con tres se trabajan turnos, interrupciones y toma de posición— y reserva los de conflicto para escalar de verdad.

Los ocho escenarios originales se redactaron antes de fijar las seis categorías del cuadro, así que su categoría se normaliza automáticamente al cargarlos: el catálogo y su filtro hablan un único idioma. La categoría original queda documentada en la tabla de cada escenario de esta sección cuando difiere.

### Escenarios originales (8)

| `id` | Situación | Voces | Categoría en el cuadro |
|---|---|---|---|
| `restaurant` | At a restaurant / En el restaurante | 2 | Vida diaria y servicios |
| `introductions` | Meeting new people / Presentarse | 3 | Vida social y personal |
| `shopping` | Shopping for clothes / De compras | 2 | Vida diaria y servicios |
| `directions` | Asking for directions / Pedir indicaciones | 3 | Cultura y entorno |
| `routines` | Daily routines / Rutinas diarias | 2 | Vida diaria y servicios |
| `problem-solving` | Solving a problem / Resolver un problema | 2 | Conflicto o negociación |
| `opinions` | Giving opinions / Dar tu opinión | 3 | Vida social y personal |
| `health-emergency` | At the doctor's / En la consulta médica | 2 | Vida diaria y servicios |

### Vida diaria y servicios (11)

| `id` | Situación | Voces |
|---|---|---|
| `hotel-checkin` | Checking in at a hotel / Registrarse en un hotel | 2 |
| `airport` | At the airport / En el aeropuerto | 2 |
| `public-transport` | Taking public transport / Usar transporte público | 3 |
| `phone-call` | Making a phone call / Hacer una llamada | 2 |
| `bank-post-office` | At the bank or post office / En el banco o correo | 2 |
| `pharmacy` | At the pharmacy / En la farmacia | 2 |
| `lost-item` | Reporting a lost item / Reportar un objeto perdido | 2 |
| *(más los 4 originales)* | `restaurant`, `shopping`, `routines`, `health-emergency` | 8 |

### Vida social y personal (8)

| `id` | Situación | Voces |
|---|---|---|
| `making-plans` | Making plans with friends / Hacer planes con amigos | 3 |
| `party-invitation` | Inviting someone to a party / Invitar a una fiesta | 2 |
| `hobbies` | Talking about hobbies / Hablar de pasatiempos | 2 |
| `social-media` | Talking about social media / Hablar de redes sociales | 3 |
| `weekend-news` | Telling a story about your weekend / Contar tu fin de semana | 2 |
| `family-dinner` | Family gathering / Reunión familiar | 3 |
| *(más los 2 originales)* | `introductions`, `opinions` | 6 |

### Vida escolar y académica (5)

| `id` | Situación | Voces |
|---|---|---|
| `classroom` | In the classroom / En el salón de clases | 3 |
| `group-project` | Working on a group project / Trabajo en grupo | 3 |
| `asking-teacher` | Asking a teacher for help / Pedir ayuda al profesor | 2 |
| `exchange-student` | Meeting an exchange student / Conocer a un estudiante de intercambio | 3 |
| `school-event` | Organizing a school event / Organizar un evento escolar | 3 |

### Proyección futura y mundo laboral (5)

| `id` | Situación | Voces |
|---|---|---|
| `job-interview` | At a job interview / En una entrevista de trabajo | 2 |
| `future-plans` | Talking about future plans / Hablar de planes de futuro | 2 |
| `career-advice` | Asking for career advice / Pedir consejo vocacional | 3 |
| `university-admission` | Applying to university / Postularse a la universidad | 2 |
| `volunteering` | Volunteering / Hacer voluntariado | 3 |

### Conflicto o negociación, nivel avanzado (7)

Pensados para escalar: simples en el nivel básico y una negociación completa en el avanzado.

| `id` | Situación | Voces |
|---|---|---|
| `complaint` | Making a complaint / Presentar una queja | 2 |
| `returning-product` | Returning a product / Devolver un producto | 2 |
| `disagreement` | Disagreeing politely / Estar en desacuerdo con respeto | 3 |
| `negotiating-price` | Bargaining at a market / Regatear en un mercado | 2 |
| `apology` | Apologizing and forgiving / Disculparse | 2 |
| `misunderstanding` | Clearing up a misunderstanding / Aclarar un malentendido | 3 |
| *(más el original)* | `problem-solving` | 2 |

### Cultura y entorno (6)

| `id` | Situación | Voces |
|---|---|---|
| `tourist-info` | Helping a tourist / Ayudar a un turista | 3 |
| `weather-plans` | Weather and changing plans / El clima y cambio de planes | 2 |
| `environment` | Talking about the environment / Hablar del medio ambiente | 3 |
| `technology` | Talking about technology / Hablar de tecnología | 3 |
| `news-discussion` | Discussing a news story / Comentar una noticia | 3 |
| *(más el original)* | `directions` | 3 |

> El contenido clínico (`health-emergency`, `pharmacy`) se mantiene en síntomas cotidianos y benignos, y cada nivel recuerda que es **práctica de lengua**, no consejo médico.

### Cómo se comprobó la progresión

No basta con que el nivel avanzado tenga frases más largas: tiene que exigir más. Una auditoría automática (`node _audit.js`) verifica en los 42 escenarios que

- la longitud media de las intervenciones **crece de forma monótona** en los tres niveles (global: ~5,5 → ~13,0 → ~18,9 palabras),
- el nivel avanzado crece de media **×3,43** respecto al básico,
- **los 42** niveles avanzados contienen estrategias discursivas reales: matizar, conceder, rebatir o pedir aclaración,
- el nivel básico **no** depende de esos matices, que son propios de los niveles superiores.

---

## Guía docente y rúbrica

Cada nivel de cada microdiálogo trae su **guía docente** ya redactada, derivada del propio material: como la guía se calcula a partir del diálogo, **nunca puede contradecirlo**. Se abre al final de la tarjeta de nivel, bajo el bloque «👩‍🏫 Guía docente», con tres profundidades:

| Pestaña | Qué ofrece |
|---|---|
| 🎯 **Sentido de la sesión** | Para qué sirve este nivel, tu papel como docente, agrupamiento, qué conviene evitar, cómo saber que funcionó y tarea para casa. |
| ⏱️ **Secuencia** | Las 9 fases MSP con **minutos asignados** (entre 48 y 62 según el nivel), y qué hace el docente y qué hacen los estudiantes en cada una. |
| 📊 **Rúbrica oral** | Los criterios de evaluación con sus cuatro grados, y un **cálculo automático** del resultado al ir marcando. |

**La rúbrica se adapta al nivel**, no es la misma plantilla para los tres:

| Nivel | Criterios (con su peso) |
|---|---|
| 🟢 Survival | Cumplimiento de la tarea (3) · Vocabulario y estructuras (3) · Fluidez y pronunciación (2) · Interacción (2) · Autonomía (2) |
| 🟡 Functional | Cumplimiento de la tarea (3) · Riqueza y corrección (3) · Fluidez (2) · Negociación de significado (3) · Autonomía (2) |
| 🔴 Communicative | Cumplimiento de la tarea (3) · Argumentación y matiz (3) · Desacuerdo y estrategias discursivas (3) · Fluidez y control del discurso (2) · Adecuación y registro (2) · Autonomía (2) |

Cada criterio describe los cuatro grados de la escala —**○ Emergente · ◔ En desarrollo · ◕ Conseguido · ● Destacado**— en términos observables. Por ejemplo, en *Communicative / Argumentación y matiz*, va desde «Afirma sin dar ninguna razón» hasta «Jerarquiza razones, concede lo válido del otro y defiende su postura con matices».

La secuencia también cambia de equilibrio según el nivel: **Survival dedica más tiempo al input** (fases 1-3) y **Communicative más a la producción** (fases 7-9). Una comprobación automática verifica ese reparto en los 42 escenarios.

**Para el aula**, el botón **🖨️ Imprimir guía** abre una hoja A4 con la secuencia, la rúbrica con casillas para marcar a mano, espacio para firmas y la cabecera del escenario. También puedes **marcar en pantalla** y dejar que la herramienta calcule el porcentaje y la banda global, o **📋 Copiar valoración** para pegar el resultado en tu registro.

---

## Guardar, compartir e importar

Como los microdiálogos generados con IA son material que has pagado con tu pollen, la herramienta no los pierde al cerrar la página.

### Biblioteca local

**💾 Guardar** almacena el microdiálogo completo en el `localStorage` del navegador, con el nombre que le pongas. Desde **📚 Biblioteca** (también en la barra superior) puedes abrirlo, compartirlo, renombrarlo o borrarlo. No se envía nada a ningún servidor.

> Si el almacenamiento está lleno o el navegador lo bloquea, la herramienta te avisa y te propone descargar el `.json` en lugar de perder el trabajo.

### Compartir por enlace

**🔗 Compartir** mete el microdiálogo **dentro de la propia URL**, comprimido con `deflate`:

```
https://…/microdialogos-msp.html#s=msp1.zQ29tcGxlc3NlZC…
```

Quien abra ese enlace ve el microdiálogo con sus tres niveles, **sin API key y sin conexión**. El enlace no apunta a ningún servidor: el contenido viaja en el fragmento de la URL, que ni siquiera se envía al servidor de la página. La herramienta limpia la dirección en cuanto lo lee.

Los tres niveles de un escenario ocupan entre **12 y 14 KB de enlace**. Funciona en correo, aula virtual y mensajería, pero si tu canal lo corta tienes alternativas:

- **⬇️ Descargar `.json`** y enviar el archivo (también puedes exportar **toda la biblioteca** de una vez).
- **📋 Copiar como texto legible**, para pegar el material en un documento o en el chat del aula.
- **⬆️ Importar un `.json`** cuando lo recibas.

---

## API key y flujo BYOP

La herramienta usa **BYOP (Bring Your Own Pollen)**: la clave es tuya y **nunca se escribe en el código**.

Pulsa el chip **«Sin API key»** en la barra superior. Hay tres caminos:

| Camino | Cuándo usarlo | Cómo funciona |
|---|---|---|
| **🚀 Obtener API key** (un clic) | Lo normal | Redirige a `enter.pollinations.ai/authorize`; al volver, la clave llega en el **fragmento de la URL** (`#api_key=…`), se guarda y la URL se limpia. No necesita registro previo. |
| **⚙️ OAuth con PKCE (S256)** | Si eres desarrollador | Requiere registrar una **App Key** (`pk_…`) con tu Redirect URI. Es el flujo recomendado por Pollinations para apps web. |
| **📱 Código de dispositivo** | Si la redirección falla o no vuelve | Abre Pollinations en otra pestaña con un código corto; la app lo detecta sola. |

Se valida el **formato** de la clave (debe empezar por `sk_`; una `pk_` es una App Key y no autoriza llamadas) y se verifica contra la API sin gastar pollen. También se comprueba el parámetro `state` como protección CSRF: si no coincide, **la clave no se guarda**.

**¿Dónde consigo una clave a mano?** En [enter.pollinations.ai](https://enter.pollinations.ai). Referencia oficial: [BRING_YOUR_OWN_POLLEN.md](https://github.com/pollinations/pollinations/blob/main/BRING_YOUR_OWN_POLLEN.md).

---

## Requisitos y arranque

- Un **navegador moderno** (Chrome, Edge, Firefox o Safari actuales). Sin instalación, sin `npm`, sin servidor.
- Conexión a Internet **solo** para generar con IA y para las ilustraciones. El catálogo y todas las actividades funcionan sin conexión.
- El archivo pesa alrededor de **1,7 MB** porque lleva dentro las 42 situaciones completas, para que funcione sin conexión. Es normal: no necesita ninguna descarga adicional.

**Opción A — doble clic.** Abre `microdialogos-msp.html`. Verás `file://` en la barra de direcciones. Todo funciona salvo la **redirección** de autorización (necesita una dirección `http(s)`): en ese caso pega la clave a mano.

**Opción B — servidor local (recomendado para BYOP).**

```bash
python -m http.server 8000
# o bien:  npx serve .
```

Y abre `http://localhost:8000/microdialogos-msp.html`.

---

## Arquitectura

El entregable es **un único archivo HTML** con HTML + CSS + JavaScript vanilla. Para poder mantenerlo y probarlo, se compila a partir de fuentes separadas:

```
shell.html ─┐
ui.css ─────┤
core.js ────┼──► build.js ──► microdialogos-msp.html   ← ENTREGABLE
_content_*.js ┤
ui.js ──────┘
```

| Archivo | Papel |
|---|---|
| `microdialogos-msp.html` | **Entregable final.** Un solo archivo, autónomo. |
| `shell.html` | Esqueleto HTML con los puntos de montaje. |
| `ui.css` | Estilos: diseño, animaciones, responsive y hoja de impresión. |
| `core.js` | **Núcleo sin DOM**: motor MSP, capa de API, parseo de JSON, BYOP/OAuth/PKCE, guía docente, biblioteca y enlaces compartidos. |
| `ui.js` | Interfaz: render, pestañas, modo práctica, TTS, copiar/imprimir, imágenes, guía, biblioteca, compartir y diagnóstico. |
| `_content_a.js` … `_content_i.js` | Las 42 situaciones con sus tres niveles, repartidas en 9 archivos de contenido. |
| `build.js` | Ensambla el entregable y verifica su integridad (incluida la sintaxis real del JavaScript). |
| `validate_scenarios.js` | Validador del esquema de contenido. |
| `_audit.js` | Auditoría pedagógica: comprueba la progresión real y las bandas de longitud. |
| `_leer_xlsx.js` | Utilidad sin dependencias para volcar el cuadro de escenarios a texto. |
| `tests_core.js` | Pruebas del núcleo (se ejecutan en Node, sin navegador). |
| `tests_build.js` | Pruebas **sobre el archivo ya generado**. |
| `verificar_navegador.js` | Verificación **funcional en Chrome real** por el protocolo de DevTools. |
| `microdiálogos_V1.txt` | Especificación original del encargo. |
| `escenarios_microdialogos_MSP.xlsx` | Cuadro de escenarios: los 42 con su categoría, `id`, títulos y número de personajes, y los criterios de selección. Es la fuente de la lista de arriba. |

Al reconstruir, `build.js` **compila y valida el JavaScript de verdad** de cada bloque, comprueba que no queden marcadores de plantilla, que ningún bloque `<script>` se rompa, que no haya backticks impares que abran una plantilla sin cerrar y que **no haya ninguna API key incrustada**.

---

## Detalles técnicos de la API

- **Texto — siempre `POST`** (los prompts son largos y un `GET` provoca HTTP 414):

  ```
  POST https://gen.pollinations.ai/v1/chat/completions
  Headers: Content-Type: application/json
           Authorization: Bearer {API_KEY}
  Body:    { "model": "openai", "messages": [ { "role": "user", "content": "{prompt}" } ] }
  ```

- **Imágenes — `GET` dentro de `<img src>`**: `https://image.pollinations.ai/prompt/{prompt}`.
- **Autorización**: `https://enter.pollinations.ai/authorize` · **Token**: `https://enter.pollinations.ai/api/oauth/token`.
- **Modelo por defecto**: `openai` (alias oficial de `openai/gpt-5.4-nano`).

El parseo de la respuesta es defensivo: quita cercas ```` ```json ````, texto de cortesía alrededor, comas finales, comillas tipográficas y **repara JSON truncado** (cuando la respuesta se corta por límite de tokens). Los errores HTTP se traducen a mensajes en español con pista accionable: `401/403` clave inválida, `402` sin pollen, `429` demasiadas solicitudes, `5xx` error temporal del servicio.

---

## Scripts y pruebas

```bash
# Reconstruir el entregable (descubre solo los _content_*.js)
node build.js

# Validar el esquema de todos los archivos de contenido
node validate_scenarios.js _content_*.js

# Auditoría pedagógica: progresión real entre los tres niveles
node _audit.js

# Pruebas del núcleo (155 pruebas)
node tests_core.js

# Pruebas sobre el archivo ya generado (40 pruebas)
node tests_build.js

# Verificación funcional en Chrome real, por el protocolo de DevTools (14 comprobaciones)
node verificar_navegador.js
```

> En PowerShell, `_content_*.js` no se expande solo: pásale la lista completa, por ejemplo
> `node validate_scenarios.js _content_a.js _content_b.js _content_c.js _content_d.js _content_e.js _content_f.js _content_g.js _content_h.js _content_i.js`.

Estado actual, todo en verde:

| Comprobación | Resultado |
|---|---|
| Validación de esquema | `OK: 42 escenarios validos en 9 archivo(s)` |
| Auditoría pedagógica | `Auditoría correcta: la progresión es real en los 42 escenarios` |
| Pruebas del núcleo | `155 pruebas correctas, 0 fallidas` |
| Pruebas del entregable | `40 pruebas correctas, 0 fallidas` |
| Verificación en Chrome real | `TODO CORRECTO` (14 comprobaciones) |
| Autodiagnóstico de la app | `21 de 21` comprobaciones |

Las pruebas cubren: parseo de JSON (limpio, con cercas, con texto alrededor, truncado, corrupto), normalización de respuestas pobres de la IA, construcción del prompt y del cuerpo `POST`, validación de claves, PKCE con vector de prueba, lectura de la redirección, protección `state`, canje de código, `device flow`, clasificación de errores, escapado anti-XSS, limpieza de la URL y ausencia de claves incrustadas.

Sobre el contenido: que estén los 42 `id` esperados, sin duplicados, con 2 o 3 personajes, las 6 categorías pobladas y el filtro y el buscador devolviendo lo que deben.

Sobre la guía docente: que se genere para **los 42 escenarios × 3 niveles** (126 guías), que cada rúbrica tenga sus cuatro grados descritos en todos los criterios, que el cálculo de la nota dé los extremos correctos (100 % con todo «Destacado», 25 % con todo «Emergente», 0 % sin marcar), que los pesos sumen y que la secuencia cubra las 9 fases con docente y estudiantes en cada una.

Sobre compartir y guardar: ida y vuelta completa del escenario por `localStorage` y por enlace comprimido, rechazo de tokens vacíos, con formato desconocido, dañados o con basura en base64, y que un enlace abierto en una **carga limpia del navegador** traiga el microdiálogo con sus tres niveles y limpie la URL.

---

## Solución de problemas

| Síntoma | Causa y solución |
|---|---|
| «Aún no hay API key» al generar una situación propia | El catálogo funciona sin clave; para generar con IA necesitas una. Pulsa **Obtener API key**. |
| El botón de autorización no vuelve con la clave | Estás en `file://`. Sirve la carpeta por `http` (ver [arranque](#requisitos-y-arranque)) o usa el **código de dispositivo** o el pegado manual. |
| «Ese formato no es válido» | Una clave de usuario empieza por `sk_`. Si empieza por `pk_` es una App Key y no sirve para llamar a la API. |
| La clave no se guarda al volver | El `state` no coincidió (protección CSRF). Vuelve a empezar la autorización. |
| «Sin conexión con el servicio» | Sin Internet solo está disponible el catálogo; el resto de la herramienta sigue funcionando. |
| La ilustración no carga | El material es completamente usable sin ella. Pulsa **Reintentar imagen**. |
| No se oye la lectura en voz alta | El navegador no tiene voces en inglés instaladas o no soporta SpeechSynthesis. Puedes comprobarlo en **🧪 Diagnóstico**. |
| La generación tarda mucho | Prueba un modelo más rápido (`openai-fast` o `mistral`) en el selector. |
| Una situación generada con IA ha desaparecido | No se guarda sola: pulsa **💾 Guardar** para conservarla en la biblioteca. |
| «No se pudo guardar: el almacenamiento está lleno» | El navegador no tiene espacio o bloquea `localStorage`. Descarga el `.json` y borra entradas antiguas de la biblioteca. |
| El enlace compartido no abre nada o llega cortado | Tu canal (chat, correo) lo truncó. Manda el `.json` o usa **📋 Copiar como texto legible**. |
| Un enlace antiguo dice que el formato no se reconoce | El contenido llegó incompleto. Pide que lo reenvíen, o usa el `.json`. |
| Quiero reutilizar la rúbrica en papel | Pulsa **🖨️ Imprimir guía** dentro del bloque de guía docente: sale en A4 con casillas para marcar a mano. |

---

## Privacidad y seguridad

- La API key **nunca está escrita en el código**. Vive solo en el `localStorage` (y `sessionStorage`) de tu navegador y se envía **únicamente** a `gen.pollinations.ai` como cabecera `Authorization` en tus propias peticiones.
- Al volver de la autorización, la clave viaja en el **fragmento** de la URL (que no llega a los registros del servidor) y la dirección se **limpia inmediatamente** con `history.replaceState`.
- Todo el contenido generado por la IA se **escapa antes de pintarse**, para que una respuesta maliciosa no pueda inyectar HTML.
- `build.js` rechaza la compilación si detecta una clave con pinta de real incrustada en el entregable.
- Existe un botón para **borrar la clave** del navegador en cualquier momento.
- La **biblioteca** y los **microdiálogos compartidos** se quedan en tu navegador: el contenido del enlace viaja en el fragmento de la URL, que no se envía al servidor que sirve la página, y la dirección se limpia en cuanto se lee.
- La herramienta **no tiene backend ni analítica**: no hay ningún servidor propio que reciba tus datos.

---

## Créditos

- Texto, imágenes y autorización: [Pollinations.AI](https://pollinations.ai) · [documentación BYOP](https://github.com/pollinations/pollinations/blob/main/BRING_YOUR_OWN_POLLEN.md)
- Diseño instruccional, interfaz y desarrollo: Profesor Édgar Herrera Morales from ELT/UX de Microdiálogos MSP
