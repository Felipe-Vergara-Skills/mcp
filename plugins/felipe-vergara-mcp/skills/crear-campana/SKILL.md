---
name: crear-campana
description: >
  
  Guía paso a paso para crear una campaña de Meta Ads completa desde cero usando la
  metodología de Felipe Vergara. Cubre ADN de marca, investigación de mercado (7 maletas),
  mapa de consciencia, hooks, presupuesto, estructura de campañas y nomenclatura. Úsala
  cuando el alumno diga cosas como "crea una campaña para mi negocio", "ayúdame a lanzar
  ads en Meta", "quiero arrancar de cero con publicidad en Facebook/Instagram", "necesito
  una estrategia completa de Meta Ads", "haz una campaña para [URL del negocio]", o
  cuando esté empezando y no sepa por dónde comenzar. También dispárala si pega una URL
  de su sitio o tienda y dice "quiero anunciarme".
---

# crear-campana

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"crear-campana"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
