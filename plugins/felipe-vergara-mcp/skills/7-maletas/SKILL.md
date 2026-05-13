---
name: 7-maletas
description: >
  
  Investiga automáticamente a tus clientes y mercado con las 7 Maletas de Cualquier Compra de Felipe Vergara.
  Analiza tu negocio, competidores, reviews de Google/Amazon, redes sociales y anuncios para generar un reporte completo
  de investigación de mercado listo para crear campañas publicitarias. SIEMPRE usa este skill cuando el usuario
  mencione: investigación de mercado, 7 maletas, analizar mi negocio, entender clientes, por qué me compran,
  buyer persona, investigar competidores, qué dicen mis clientes, análisis de mercado, crear buyer personas,
  o cuando esté a punto de crear anuncios/campañas y necesite entender primero a su audiencia. También úsala
  cuando el usuario quiera saber qué problemas resuelve su producto, qué diferenciales tiene, o cómo mejorar
  su comunicación en web o anuncios.
---

# 7-maletas

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"7-maletas"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
