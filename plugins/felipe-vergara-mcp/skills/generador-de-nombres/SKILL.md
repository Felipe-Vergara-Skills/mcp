---
name: generador-de-nombres
description: >
  
  Genera nombres estandarizados para campañas, conjuntos de anuncios y anuncios de Facebook e
  Instagram Ads usando la nomenclatura de Felipe Vergara. Úsalo siempre que el usuario quiera
  nombrar campañas de Meta, crear nombres para sus ads, estandarizar nomenclatura de Facebook Ads,
  generar el nombre de un conjunto de anuncios o anuncio, o cuando mencione que no sabe cómo
  llamar su campaña, adset o anuncio en Ads Manager. También úsalo si el usuario dice "ponle nombre
  a mi campaña", "cómo nombro esto en Meta", "nomenclatura para mis anuncios" o cualquier variante
  de querer un nombre estructurado para sus elementos en Meta Ads Manager — incluso si no pide
  explícitamente un "generador de nombres".
---

# generador-de-nombres

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"generador-de-nombres"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
