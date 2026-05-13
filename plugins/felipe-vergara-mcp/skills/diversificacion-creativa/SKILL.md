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

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"diversificacion-creativa"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
