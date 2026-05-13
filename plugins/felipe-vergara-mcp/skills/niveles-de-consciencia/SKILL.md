---
name: niveles-de-consciencia
description: >
  
  Diagnostica el nivel de consciencia del mercado y genera ad copy persuasivo + estrategia de campaña
  para Facebook e Instagram Ads usando los 5 niveles de consciencia de Felipe Vergara.
  SIEMPRE usa este skill cuando el usuario mencione: niveles de consciencia, copy para anuncios,
  textos para ads, copywriting para Facebook o Instagram, textos persuasivos, mercado frío,
  mercado caliente, tráfico frío, tráfico caliente, crear anuncios, escribir copy, texto para campaña,
  ad copy, anuncio inconsciente, anuncio de problema, anuncio de solución, anuncio de producto,
  anuncio de decisión, detectar nivel de consciencia, qué tipo de anuncio hacer, cómo hablarle
  a mi mercado, o cuando quiera crear copy para sus campañas en Meta Ads.
  También úsalo cuando el usuario ya tenga el reporte de /7-maletas y quiera pasar a crear anuncios.
---

# niveles-de-consciencia

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"niveles-de-consciencia"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
