---
name: metodologia-3qs
description: >
  
  Analiza campañas de Facebook e Instagram Ads usando la metodología de las 3 Q's
  de Felipe Vergara y un sistema de benchmarks semáforo (🔴/🟡/🟢). Trabajas con un
  reporte exportado de Ads Manager (CSV o Excel) — sin conectarte a la Meta API.
  Úsala SIEMPRE que el usuario quiera analizar o revisar campañas de Meta/Facebook/Instagram;
  diagnosticar por qué una campaña no convierte; evaluar ROAS, CPL, CPM, CPC, CTR, frecuencia,
  costo por conversación o costo por resultado; revisar adsets, anuncios o creativos; auditar
  el embudo de ventas (impresiones → clics → landing → checkout → compra); detectar fatiga
  de audiencia; recomendar qué pausar, escalar u optimizar. Actívala incluso si el usuario
  no dice "Meta" explícitamente pero habla de Facebook Ads, Instagram Ads, Business Manager,
  formularios instantáneos, campañas a WhatsApp, Advantage+, o píxel de Meta.
  No usar para Google Ads, TikTok Ads, LinkedIn Ads, ni para crear campañas — solo análisis
  y diagnóstico de campañas Meta existentes a partir del CSV/Excel exportado.
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
