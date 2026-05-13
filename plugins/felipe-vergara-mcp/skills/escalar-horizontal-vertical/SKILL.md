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

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"escalar-horizontal-vertical"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
