---
name: metodologia-3qs
description: >
  Analiza campañas de Meta Ads con la metodología 3 Q's y benchmarks semáforo (rojo/amarillo/verde). Trabaja con CSV/Excel de Ads Manager. Úsala cuando el alumno pida analizar Meta/Facebook/Instagram Ads, diagnosticar por qué no convierte, evaluar ROAS/CPL/CPC/CTR/CPM, auditar el embudo, detectar fatiga.
---


# metodologia-3qs

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"metodologia-3qs"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
