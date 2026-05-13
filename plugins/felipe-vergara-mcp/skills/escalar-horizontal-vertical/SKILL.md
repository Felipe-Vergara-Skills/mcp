---
name: escalar-horizontal-vertical
description: >
  
  Genera un plan de escalado para campañas de Meta Ads rentables: cuánto subir el presupuesto,
  cada cuánto, y cómo diversificar con nuevos anuncios, públicos o campañas.
  Úsalo SOLO cuando el alumno la solicite explícitamente — quiera escalar sus campañas, no
  sepa cómo o cuánto subir el presupuesto, quiera invertir más en lo que ya le está
  funcionando, pregunte por escalar vertical u horizontalmente, o diga que sus anuncios
  van bien y quiere sacarles más provecho. NO se invoca automáticamente desde otras skills
  (incluido metodologia-3qs) — solo cuando el alumno la pide.
---

# escalar-horizontal-vertical

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"escalar-horizontal-vertical"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
