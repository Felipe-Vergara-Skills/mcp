---
name: excel-de-estrategia
description: >
  
  Genera la estrategia completa de campañas de Meta Ads según la metodología de Felipe Vergara.
  Crea la estructura de campañas (Presentación, Evaluación, Conversión, Ascensión) con todos los
  parámetros: objetivo, presupuestos, conjuntos de anuncios, públicos, exclusiones y ubicaciones.
  Úsalo cuando el alumno quiera armar su estrategia de Facebook e Instagram Ads, no sepa cómo
  distribuir su presupuesto, quiera saber cuántas campañas crear, qué audiencias usar, o quiera
  replicar el Excel de estrategia de Felipe Vergara.
---

# excel-de-estrategia

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"excel-de-estrategia"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
