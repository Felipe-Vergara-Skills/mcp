---
name: escanear-marca
description: >
  
  Escanea automáticamente la web de una marca con Playwright para extraer su ADN: identidad visual
  (colores, tipografía, estilo de imagery), tono y voz de marca, avatar de cliente con los 16 Deseos
  de Reiss, nivel de consciencia dominante del copy, tipo de oferta, propuesta de valor, producto
  y precio. Best-effort scrape de Instagram y TikTok públicos para sumar tono real. Genera un HTML
  con el reporte completo y guarda `marca-cliente.json` para que las demás skills del plugin lo
  reutilicen sin tener que volver a explicar la marca. SIEMPRE usa este skill cuando el usuario
  mencione: escanear marca, ADN de marca, brand DNA, extraer marca, identidad de marca, perfil de
  marca, analizar marca, voz de marca, tono de marca, colores de marca, paleta de marca, tipografía
  de la marca, avatar del cliente, audiencia de la marca, propuesta de valor, o cuando esté arrancando
  con un cliente nuevo y quiera mapear la marca antes de hacer ads.
---

# escanear-marca

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"escanear-marca"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
