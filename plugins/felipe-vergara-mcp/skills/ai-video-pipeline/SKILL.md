---
name: ai-video-pipeline
description: >
  A video production house in one skill. Takes a brand from idea to a finished short AI video (ad, teaser) in any style, realistic or animated (claymation, 2D, 3D). Proposes video ideas from the brand or works from the user's own idea, writes the style block, the character, product and place sheet prompts, the video prompt in each model's own reference spelling (Wan, Seedance, Kling, Grok, Magnific), the ElevenLabs Eleven v4 voiceover script and the Suno V6 music brief; generates sheets, video and music on Kie only after an OK for each spend. Talks in Spanish by default. Use when the user says AI video, anuncio con IA, video con IA, idea para un video, hoja de personaje, character sheet, prompt de video, Seedance, Wan, Kling, voz en off, locución, ElevenLabs, música para el anuncio, Suno, "el personaje cambia entre tomas", or reports a bad generation. Not for static image ads (produccion-anuncios), the scripted fichas-de-consistencia renders, or storyboard boards (storyboard-de-anuncio).
---

# ai-video-pipeline

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"ai-video-pipeline"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye la marca, la idea, la URL o los datos que haya dado)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. La skill que devuelve el MCP incluye un PASO 0 de descarga de sus archivos y todo su flujo propio.

Cuando el MCP responda, ejecuta sus instrucciones tal cual — empezando por el PASO 0 (descarga del paquete de scripts y referencias). Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
