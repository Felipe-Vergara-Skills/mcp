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

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"optimizacion-destino"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
