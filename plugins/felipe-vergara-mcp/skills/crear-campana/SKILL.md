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

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"crear-campana"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
