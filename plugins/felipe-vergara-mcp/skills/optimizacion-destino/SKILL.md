---
name: optimizacion-destino
description: >
  
  Audita el destino real de los anuncios de Meta Ads (tienda online, formulario de leads,
  WhatsApp o tienda física en Google Maps) navegándolo con Playwright y genera
  recomendaciones específicas basadas en lo que encuentra (no genéricas).
  Úsalo SOLO cuando el alumno la solicite explícitamente — diga que sus anuncios funcionan
  pero no vende, que tiene muchos clics pero pocas compras, que su tasa de conversión es
  baja, que recibe muchos mensajes pero no cierra ventas, que sus leads no son calificados,
  o que quiere mejorar su página web, tienda online, formulario o proceso de ventas por
  WhatsApp. NO se invoca automáticamente desde otras skills (incluido metodologia-3qs) —
  solo cuando el alumno la pide.
---

# optimizacion-destino

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"optimizacion-destino"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
