---
name: analizar-campana
description: >
  
  Analiza campañas activas de Meta Ads usando la metodología 3 Q's de Felipe Vergara.
  Diagnostica el problema exacto (presupuesto, público, creativos o destino) y genera
  un plan de acción concreto: optimizar o escalar. Úsalo cuando el alumno diga cosas
  como "analiza mis campañas", "revisa cómo van mis anuncios", "no entiendo mis
  resultados de Meta Ads", "mis campañas no rinden", "¿qué hago con mis campañas?",
  "diagnostica mi cuenta de Ads", "aplícame las 3 Q's", o cuando pregunte si sus
  campañas están bien o mal. También dispárala si el alumno sube un CSV exportado
  de Ads Manager y pide revisión.
---

# analizar-campana

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"analizar-campana"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
