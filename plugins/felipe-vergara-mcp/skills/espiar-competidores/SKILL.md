---
name: espiar-competidores
description: >
  
  Espía a los competidores de un negocio en Meta Ad Library + Instagram público + TikTok público.
  El alumno solo pasa la URL de SU negocio — la skill detecta automáticamente la industria, busca
  competidores en Google, los confirma con el alumno, y luego scrapea sus anuncios activos en Meta,
  su perfil de IG y su perfil de TikTok. Genera un HTML con tabs por competidor: hooks detectados,
  ángulos dominantes, niveles de consciencia (Eugene Schwartz), ofertas usadas, formato dominante
  y tono orgánico. Standalone — no comparte estado con otras skills. SIEMPRE usa este skill cuando
  el usuario mencione: espiar competidores, ad spy, biblioteca de anuncios, Meta Ad Library, qué
  anuncios corren mis competidores, hooks de competidores, ofertas de competidores, copy de
  competidores, análisis competitivo, inteligencia competitiva, qué hacen otras marcas, cómo
  hablan otros en la categoría.
---

# espiar-competidores

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"espiar-competidores"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
