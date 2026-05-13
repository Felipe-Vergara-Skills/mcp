---
name: diversificacion-creativa
description: >
  
  Genera hooks y prompts de anuncios listos para usar en Meta Ads usando los 16 Deseos de Reiss
  y los 5 Niveles de Consciencia. Úsalo SIEMPRE que el alumno quiera ideas para anuncios, no sepa
  qué decir en sus creativos, sienta que sus anuncios se parecen demasiado entre sí, quiera
  diversificar sus creativos, mencione hooks, copies, textos de anuncios, ideas para Facebook o
  Instagram Ads, o cuando sus campañas hayan bajado de rendimiento por falta de variedad creativa.
  También úsalo cuando mencione la metodología de diversificación creativa, los deseos de Reiss,
  niveles de consciencia aplicados a anuncios, o pida una matriz de anuncios.
---

# diversificacion-creativa

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"diversificacion-creativa"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
