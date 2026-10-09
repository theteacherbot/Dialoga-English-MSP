# DIALOGA English MSP

**Interactive web tool for developing spoken production and interaction in English through the "Progressive Situational Micro-Dialogues (MSP) Model".**

It generates English micro-dialogues with **2 or 3 speakers** set in everyday situations and, for each situation, produces **three versions of the same scenario**. What changes between versions is not the vocabulary: it is the **cognitive and communicative demand**.

It comes with **42 ready-to-use situations** (126 micro-dialogues: 42 × 3 levels) spread across 6 categories, from daily life and services to conflict and negotiation, including school life and professional outlook.

> **Key pedagogical principle:** the dialogue is **not the final product**, it is the **scaffold** toward spontaneous communication.
> Sequence: `Context → Model → Comprehension → Guided practice → Substitution → Personalization → Interaction → Improvisation → Spontaneous production`.

---

## Table of contents

- [What it does](#what-it-does)
- [How to use it](#how-to-use-it)
- [The three levels](#the-three-levels)
- [The 9 phases of each level](#the-9-phases-of-each-level)
- [Included situations](#included-situations)
- [Teacher guide and rubric](#teacher-guide-and-rubric)
- [Save, share and import](#save-share-and-import)
- [API key and BYOP flow](#api-key-and-byop-flow)
- [Requirements and getting started](#requirements-and-getting-started)
- [Architecture](#architecture)
- [API technical details](#api-technical-details)
- [Scripts and tests](#scripts-and-tests)
- [Troubleshooting](#troubleshooting)
- [Privacy and security](#privacy-and-security)

---

## What it does

- **42 ready-to-use situations** spread across 6 categories, each with its three complete levels. They work **offline and without an API key**, are instant, and serve as a reference for the model.
- **Filterable catalog**: category chips and a search box that understands Spanish and English, to find a situation in seconds.
- **AI generation** of any situation you type (in Spanish or English), also with all three levels complete.
- **Side-by-side view** of the three levels so students can *see* their progression, or **tabs** to work on one at a time.
- **Practice mode**: hides one character's lines so the student has to produce them, with a button to reveal them one at a time.
- **Read aloud** of the whole dialogue or a single line (browser SpeechSynthesis).
- **AI-generated scene illustration**, with a loading indicator and a friendly fallback if it fails.
- **Copy, download as `.txt` and print** the material (with a print stylesheet for the lesson plan).
- **Built-in diagnostics** with 20 checks that can be run from the page itself.
- **Teacher guide per level**: oral assessment rubric and a minute-by-minute session sequence, ready to print.
- **Local library**: save the micro-dialogues you generate and retrieve them whenever you want.
- **Share by link**: the micro-dialogue travels inside the link itself (compressed), with no server and no API key. It also exports and imports `.json`.

---

## How to use it

1. Open `microdialogos-msp.html` in your browser.
2. **Choose a situation** from the catalog (instant, free) or **write your own**. Set **2 or 3 speakers** and, if you want, the AI model.
3. Press **✨ Generate the three levels**. With the catalog it is immediate; with AI it usually takes between 15 and 60 seconds.
4. Move between **🟢 / 🟡 / 🔴** or press **👁️ View the three levels** to compare the progression.
5. Turn on **🎭 Practice mode** and choose the character whose lines will be hidden.
6. Use **🔊 Listen to dialogue** to model pronunciation.
7. Scroll down to **👩‍🏫 Teacher guide** for the rubric and the session sequence, and press **🖨️ Print guide**.
8. Take the material to the classroom with **📋 Copy all**, **⬇️ Download .txt** or **🖨️ Print**; save what you want to keep with **💾 Save** and share it with **🔗 Share**.

> **Shortcut:** by pressing **🧪 Diagnostics** in the top bar, the tool checks itself in front of you.

---

## The three levels

| Level | Motto | CEFR | Expected interaction |
|---|---|---|---|
| 🟢 `survival` | **I can say it** | A1–A2 | Reproduce → substitute → respond |
| 🟡 `functional` | **I can interact** | A2–B1 | Adapt → expand → negotiate meaning |
| 🔴 `communicative` | **I can improvise** | B1–B2 | Interpret → react → build meaning |

**Example of progression ("At the restaurant"), identical scenario in all three cases:**

- 🟢 Order a hamburger and a drink using model structures.
- 🟡 Ask about ingredients, state a dietary restriction, change the dish and justify it with connectors.
- 🔴 The wrong dish arrives: reasoned complaint, two solutions on the table and negotiation of compensation.

---

## The 9 phases of each level

| # | Phase | What it provides |
|---|---|---|
| 1 | **Context** | Sets the scene and the communicative purpose. |
| 2 | **Model** | The exemplary dialogue: comprehensible input and modeling. |
| 3 | **Comprehension** | Literal **and inferential** questions. |
| 4 | **Guided practice** | Sentence frames and an example to produce with support. |
| 5 | **Substitution** | Change one element of the pattern and produce again. |
| 6 | **Personalization** | Bring the language into the student's real life. |
| 7 | **Interaction** | Peer role-play with a communicative task. |
| 8 | **Improvisation** | Unexpected twist: forces a reaction without a script. |
| 9 | **Spontaneous production** | Transfer to a new, authentic situation. |

Each level also adds **key language**, a **pronunciation focus**, **common errors** of Spanish speakers and **teacher notes**.

---

## Included situations

**42 scenarios**, all with their three complete levels (126 micro-dialogues). The distribution comes from the project's scenario table (`escenarios_microdialogos_MSP.xlsx`) and respects its selection criteria: it balances communicative functions (asking, informing, narrating, giving opinions, complaining, negotiating, apologizing and planning), alternates **23 scenarios with 2 speakers and 19 with 3** — with three, turn-taking, interruptions and taking sides are practiced — and reserves the conflict scenarios for genuine escalation.

The eight original scenarios were written before the six categories of the table were fixed, so their category is automatically normalized on load: the catalog and its filter speak a single language. The original category is documented in the table of each scenario in this section when it differs.

### Original scenarios (8)

| `id` | Situation | Voices | Category in the table |
|---|---|---|---|
| `restaurant` | At a restaurant | 2 | Daily life and services |
| `introductions` | Meeting new people | 3 | Social and personal life |
| `shopping` | Shopping for clothes | 2 | Daily life and services |
| `directions` | Asking for directions | 3 | Culture and environment |
| `routines` | Daily routines | 2 | Daily life and services |
| `problem-solving` | Solving a problem | 2 | Conflict or negotiation |
| `opinions` | Giving opinions | 3 | Social and personal life |
| `health-emergency` | At the doctor's | 2 | Daily life and services |

### Daily life and services (11)

| `id` | Situation | Voices |
|---|---|---|
| `hotel-checkin` | Checking in at a hotel | 2 |
| `airport` | At the airport | 2 |
| `public-transport` | Taking public transport | 3 |
| `phone-call` | Making a phone call | 2 |
| `bank-post-office` | At the bank or post office | 2 |
| `pharmacy` | At the pharmacy | 2 |
| `lost-item` | Reporting a lost item | 2 |
| *(plus the 4 originals)* | `restaurant`, `shopping`, `routines`, `health-emergency` | 8 |

### Social and personal life (8)

| `id` | Situation | Voices |
|---|---|---|
| `making-plans` | Making plans with friends | 3 |
| `party-invitation` | Inviting someone to a party | 2 |
| `hobbies` | Talking about hobbies | 2 |
| `social-media` | Talking about social media | 3 |
| `weekend-news` | Telling a story about your weekend | 2 |
| `family-dinner` | Family gathering | 3 |
| *(plus the 2 originals)* | `introductions`, `opinions` | 6 |

### School and academic life (5)

| `id` | Situation | Voices |
|---|---|---|
| `classroom` | In the classroom | 3 |
| `group-project` | Working on a group project | 3 |
| `asking-teacher` | Asking a teacher for help | 2 |
| `exchange-student` | Meeting an exchange student | 3 |
| `school-event` | Organizing a school event | 3 |

### Future outlook and the working world (5)

| `id` | Situation | Voices |
|---|---|---|
| `job-interview` | At a job interview | 2 |
| `future-plans` | Talking about future plans | 2 |
| `career-advice` | Asking for career advice | 3 |
| `university-admission` | Applying to university | 2 |
| `volunteering` | Volunteering | 3 |

### Conflict or negotiation, advanced level (7)

Designed to escalate: simple at the basic level and a full negotiation at the advanced level.

| `id` | Situation | Voices |
|---|---|---|
| `complaint` | Making a complaint | 2 |
| `returning-product` | Returning a product | 2 |
| `disagreement` | Disagreeing politely | 3 |
| `negotiating-price` | Bargaining at a market | 2 |
| `apology` | Apologizing and forgiving | 2 |
| `misunderstanding` | Clearing up a misunderstanding | 3 |
| *(plus the original)* | `problem-solving` | 2 |

### Culture and environment (6)

| `id` | Situation | Voices |
|---|---|---|
| `tourist-info` | Helping a tourist | 3 |
| `weather-plans` | Weather and changing plans | 2 |
| `environment` | Talking about the environment | 3 |
| `technology` | Talking about technology | 3 |
| `news-discussion` | Discussing a news story | 3 |
| *(plus the original)* | `directions` | 3 |

> The clinical content (`health-emergency`, `pharmacy`) is kept to everyday, benign symptoms, and each level reminds learners that it is **language practice**, not medical advice.

### How the progression was verified

It is not enough for the advanced level to have longer sentences: it has to demand more. An automatic audit (`node _audit.js`) verifies across all 42 scenarios that

- the average length of turns **grows monotonically** across the three levels (overall: ~5.5 → ~13.0 → ~18.9 words),
- the advanced level grows on average **×3.43** relative to the basic level,
- **all 42** advanced levels contain real discourse strategies: hedging, conceding, rebutting or asking for clarification,
- the basic level does **not** depend on those nuances, which belong to the higher levels.

---

## Teacher guide and rubric

Each level of each micro-dialogue comes with its own **teacher guide** already written, derived from the material itself: since the guide is computed from the dialogue, it **can never contradict it**. It opens at the end of the level card, under the "👩‍🏫 Teacher guide" block, with three depths:

| Tab | What it offers |
|---|---|
| 🎯 **Purpose of the session** | What this level is for, your role as teacher, grouping, what to avoid, how to know it worked, and homework. |
| ⏱️ **Sequence** | The 9 MSP phases with **allotted minutes** (between 48 and 62 depending on the level), and what the teacher and the students do in each. |
| 📊 **Oral rubric** | The assessment criteria with their four grades, and an **automatic calculation** of the result as you mark. |

**The rubric adapts to the level**; it is not the same template for all three:

| Level | Criteria (with weight) |
|---|---|
| 🟢 Survival | Task completion (3) · Vocabulary and structures (3) · Fluency and pronunciation (2) · Interaction (2) · Autonomy (2) |
| 🟡 Functional | Task completion (3) · Richness and accuracy (3) · Fluency (2) · Negotiation of meaning (3) · Autonomy (2) |
| 🔴 Communicative | Task completion (3) · Argumentation and nuance (3) · Disagreement and discourse strategies (3) · Fluency and control of discourse (2) · Appropriateness and register (2) · Autonomy (2) |

Each criterion describes the four grades of the scale — **○ Emerging · ◔ Developing · ◕ Achieved · ● Outstanding** — in observable terms. For example, in *Communicative / Argumentation and nuance*, it goes from "States a position without giving any reason" to "Ranks reasons, concedes what is valid in the other person's view and defends their position with nuance".

The sequence also changes its balance according to the level: **Survival devotes more time to input** (phases 1-3) and **Communicative more to production** (phases 7-9). An automatic check verifies this distribution across all 42 scenarios.

**For the classroom**, the **🖨️ Print guide** button opens an A4 sheet with the sequence, the rubric with boxes to tick by hand, space for signatures and the scenario header. You can also **mark on screen** and let the tool calculate the percentage and the overall band, or **📋 Copy assessment** to paste the result into your records.

---

## Save, share and import

Since AI-generated micro-dialogues are material you have paid for with your pollen, the tool does not lose them when you close the page.

### Local library

**💾 Save** stores the complete micro-dialogue in the browser's `localStorage`, under the name you give it. From **📚 Library** (also in the top bar) you can open, share, rename or delete it. Nothing is sent to any server.

> If storage is full or the browser blocks it, the tool warns you and suggests downloading the `.json` instead of losing your work.

### Share by link

**🔗 Share** puts the micro-dialogue **inside the URL itself**, compressed with `deflate`:

```
https://…/microdialogos-msp.html#s=msp1.zQ29tcGxlc3NlZC…
```

Whoever opens that link sees the micro-dialogue with its three levels, **without an API key and offline**. The link does not point to any server: the content travels in the URL fragment, which is not even sent to the page's server. The tool cleans the address as soon as it reads it.

The three levels of a scenario take up between **12 and 14 KB of link**. It works in email, virtual classrooms and messaging, but if your channel cuts it off you have alternatives:

- **⬇️ Download `.json`** and send the file (you can also export **the whole library** at once).
- **📋 Copy as readable text**, to paste the material into a document or the class chat.
- **⬆️ Import a `.json`** when you receive it.

---

## API key and BYOP flow

The tool uses **BYOP (Bring Your Own Pollen)**: the key is yours and is **never written in the code**.

Press the **"No API key"** chip in the top bar. There are three paths:

| Path | When to use it | How it works |
|---|---|---|
| **🚀 Get API key** (one click) | The usual case | Redirects to `enter.pollinations.ai/authorize`; on return, the key arrives in the **URL fragment** (`#api_key=…`), is saved and the URL is cleaned. No prior registration needed. |
| **⚙️ OAuth with PKCE (S256)** | If you are a developer | Requires registering an **App Key** (`pk_…`) with your Redirect URI. It is the flow recommended by Pollinations for web apps. |
| **📱 Device code** | If the redirect fails or doesn't come back | Opens Pollinations in another tab with a short code; the app detects it on its own. |

The key's **format** is validated (it must start with `sk_`; a `pk_` is an App Key and does not authorize calls) and it is verified against the API without spending pollen. The `state` parameter is also checked as CSRF protection: if it does not match, **the key is not saved**.

**Where do I get a key by hand?** At [enter.pollinations.ai](https://enter.pollinations.ai). Official reference: [BRING_YOUR_OWN_POLLEN.md](https://github.com/pollinations/pollinations/blob/main/BRING_YOUR_OWN_POLLEN.md).

---

## Requirements and getting started

- A **modern browser** (current Chrome, Edge, Firefox or Safari). No installation, no `npm`, no server.
- Internet connection **only** for AI generation and for illustrations. The catalog and all activities work offline.
- The file weighs around **1.7 MB** because it carries all 42 complete situations inside, so that it works offline. This is normal: no additional download is needed.

**Option A — double click.** Open `microdialogos-msp.html`. You will see `file://` in the address bar. Everything works except the authorization **redirect** (it needs an `http(s)` address): in that case, paste the key by hand.

**Option B — local server (recommended for BYOP).**

```bash
python -m http.server 8000
# or:  npx serve .
```

And open `http://localhost:8000/microdialogos-msp.html`.

---

## Architecture

The deliverable is a **single HTML file** with HTML + CSS + vanilla JavaScript. To make it maintainable and testable, it is compiled from separate sources:

```
shell.html ─┐
ui.css ─────┤
core.js ────┼──► build.js ──► microdialogos-msp.html   ← DELIVERABLE
_content_*.js ┤
ui.js ──────┘
```

| File | Role |
|---|---|
| `microdialogos-msp.html` | **Final deliverable.** A single, self-contained file. |
| `shell.html` | HTML skeleton with the mount points. |
| `ui.css` | Styles: layout, animations, responsive design and print stylesheet. |
| `core.js` | **DOM-free core**: MSP engine, API layer, JSON parsing, BYOP/OAuth/PKCE, teacher guide, library and shared links. |
| `ui.js` | Interface: rendering, tabs, practice mode, TTS, copy/print, images, guide, library, sharing and diagnostics. |
| `_content_a.js` … `_content_i.js` | The 42 situations with their three levels, spread across 9 content files. |
| `build.js` | Assembles the deliverable and verifies its integrity (including the real JavaScript syntax). |
| `validate_scenarios.js` | Content schema validator. |
| `_audit.js` | Pedagogical audit: checks the real progression and the length bands. |
| `_leer_xlsx.js` | Dependency-free utility to dump the scenario table to text. |
| `tests_core.js` | Core tests (run in Node, without a browser). |
| `tests_build.js` | Tests **on the already generated file**. |
| `verificar_navegador.js` | **Functional** verification in real Chrome via the DevTools protocol. |
| `microdiálogos_V1.txt` | Original specification of the commission. |
| `escenarios_microdialogos_MSP.xlsx` | Scenario table: all 42 with their category, `id`, titles and number of characters, plus the selection criteria. It is the source of the list above. |

When rebuilding, `build.js` **really compiles and validates the JavaScript** of each block, checks that no template markers remain, that no `<script>` block is broken, that there are no odd backticks opening an unclosed template, and that **no API key is embedded**.

---

## API technical details

- **Text — always `POST`** (prompts are long and a `GET` causes HTTP 414):

  ```
  POST https://gen.pollinations.ai/v1/chat/completions
  Headers: Content-Type: application/json
           Authorization: Bearer {API_KEY}
  Body:    { "model": "openai", "messages": [ { "role": "user", "content": "{prompt}" } ] }
  ```

- **Images — `GET` inside `<img src>`**: `https://image.pollinations.ai/prompt/{prompt}`.
- **Authorization**: `https://enter.pollinations.ai/authorize` · **Token**: `https://enter.pollinations.ai/api/oauth/token`.
- **Default model**: `openai` (official alias of `openai/gpt-5.4-nano`).

Response parsing is defensive: it strips ```` ```json ```` fences, courtesy text around the JSON, trailing commas and typographic quotes, and **repairs truncated JSON** (when the response is cut off by the token limit). HTTP errors are translated into messages in Spanish with an actionable hint: `401/403` invalid key, `402` no pollen, `429` too many requests, `5xx` temporary service error.

---

## Scripts and tests

```bash
# Rebuild the deliverable (discovers the _content_*.js files on its own)
node build.js

# Validate the schema of all content files
node validate_scenarios.js _content_*.js

# Pedagogical audit: real progression across the three levels
node _audit.js

# Core tests (155 tests)
node tests_core.js

# Tests on the already generated file (40 tests)
node tests_build.js

# Functional verification in real Chrome, via the DevTools protocol (14 checks)
node verificar_navegador.js
```

> In PowerShell, `_content_*.js` is not expanded automatically: pass it the full list, for example
> `node validate_scenarios.js _content_a.js _content_b.js _content_c.js _content_d.js _content_e.js _content_f.js _content_g.js _content_h.js _content_i.js`.

Current status, all green:

| Check | Result |
|---|---|
| Schema validation | `OK: 42 escenarios validos en 9 archivo(s)` |
| Pedagogical audit | `Auditoría correcta: la progresión es real en los 42 escenarios` |
| Core tests | `155 pruebas correctas, 0 fallidas` |
| Deliverable tests | `40 pruebas correctas, 0 fallidas` |
| Verification in real Chrome | `TODO CORRECTO` (14 checks) |
| App self-diagnostics | `21 of 21` checks |

*(The result strings are the literal output printed by the scripts, in Spanish.)*

The tests cover: JSON parsing (clean, fenced, with surrounding text, truncated, corrupt), normalization of poor AI responses, construction of the prompt and the `POST` body, key validation, PKCE with a test vector, redirect reading, `state` protection, code exchange, `device flow`, error classification, anti-XSS escaping, URL cleaning and absence of embedded keys.

On content: that all 42 expected `id`s are present, with no duplicates, with 2 or 3 characters, the 6 categories populated, and the filter and search returning what they should.

On the teacher guide: that it is generated for **all 42 scenarios × 3 levels** (126 guides), that each rubric has its four grades described in every criterion, that the score calculation gives the correct extremes (100% with everything "Outstanding", 25% with everything "Emerging", 0% with nothing marked), that the weights add up, and that the sequence covers the 9 phases with teacher and students in each.

On sharing and saving: full round trip of the scenario through `localStorage` and through the compressed link, rejection of empty tokens, tokens with an unknown format, damaged ones or ones with base64 garbage, and that a link opened in a **clean browser load** brings the micro-dialogue with its three levels and cleans the URL.

---

## Troubleshooting

| Symptom | Cause and solution |
|---|---|
| "There is no API key yet" when generating your own situation | The catalog works without a key; to generate with AI you need one. Press **Get API key**. |
| The authorization button doesn't come back with the key | You are on `file://`. Serve the folder over `http` (see [getting started](#requirements-and-getting-started)) or use the **device code** or manual paste. |
| "That format is not valid" | A user key starts with `sk_`. If it starts with `pk_` it is an App Key and cannot be used to call the API. |
| The key isn't saved on return | The `state` did not match (CSRF protection). Start the authorization again. |
| "No connection to the service" | Without Internet only the catalog is available; the rest of the tool keeps working. |
| The illustration doesn't load | The material is fully usable without it. Press **Retry image**. |
| Read-aloud can't be heard | The browser has no English voices installed or doesn't support SpeechSynthesis. You can check it in **🧪 Diagnostics**. |
| Generation takes too long | Try a faster model (`openai-fast` or `mistral`) in the selector. |
| An AI-generated situation has disappeared | It is not saved automatically: press **💾 Save** to keep it in the library. |
| "Could not save: storage is full" | The browser has no space or blocks `localStorage`. Download the `.json` and delete old library entries. |
| The shared link opens nothing or arrives cut off | Your channel (chat, email) truncated it. Send the `.json` or use **📋 Copy as readable text**. |
| An old link says the format isn't recognized | The content arrived incomplete. Ask for it to be resent, or use the `.json`. |
| I want to reuse the rubric on paper | Press **🖨️ Print guide** inside the teacher guide block: it comes out on A4 with boxes to tick by hand. |

---

## Privacy and security

- The API key is **never written in the code**. It lives only in your browser's `localStorage` (and `sessionStorage`) and is sent **only** to `gen.pollinations.ai` as an `Authorization` header in your own requests.
- When returning from authorization, the key travels in the URL **fragment** (which does not reach server logs) and the address is **cleaned immediately** with `history.replaceState`.
- All AI-generated content is **escaped before being rendered**, so that a malicious response cannot inject HTML.
- `build.js` refuses to build if it detects a real-looking key embedded in the deliverable.
- There is a button to **delete the key** from the browser at any time.
- The **library** and **shared micro-dialogues** stay in your browser: the link's content travels in the URL fragment, which is not sent to the server that serves the page, and the address is cleaned as soon as it is read.
- The tool has **no backend and no analytics**: there is no server of its own that receives your data.

---

## Credits

- Text, images and authorization: [Pollinations.AI](https://pollinations.ai) · [BYOP documentation](https://github.com/pollinations/pollinations/blob/main/BRING_YOUR_OWN_POLLEN.md)
- Instructional design, interface and development: Professor Édgar Herrera Morales from ELT/UX of Microdiálogos MSP
