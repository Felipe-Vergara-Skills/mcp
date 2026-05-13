---
name: calculadora-de-presupuestos
description: >
  
  Calcula el presupuesto exacto para campañas de Facebook e Instagram Ads y el ROAS objetivo
  usando la calculadora de Felipe Vergara. Úsalo siempre que el usuario quiera saber cuánto
  invertir en Meta Ads, cuál es su presupuesto para anuncios, cuánto necesita gastar en Facebook
  o Instagram, cuál es su ROAS objetivo, cuál es su número mágico, costo por compra objetivo,
  costo por lead objetivo, costo por conversación objetivo, o cuando diga que no sabe cuánto
  presupuesto poner en sus campañas. También úsalo si menciona que quiere calcular su inversión
  en publicidad, rentabilidad de sus anuncios, o cuánto puede pagar por un cliente — incluso si
  no dice explícitamente "calculadora" o "presupuesto".
---

# calculadora-de-presupuestos

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"calculadora-de-presupuestos"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
