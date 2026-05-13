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
allowed-tools: mcp__plugin_felipe-vergara-plugin_playwright__browser_navigate mcp__plugin_felipe-vergara-plugin_playwright__browser_click mcp__plugin_felipe-vergara-plugin_playwright__browser_type mcp__plugin_felipe-vergara-plugin_playwright__browser_scroll mcp__plugin_felipe-vergara-plugin_playwright__browser_snapshot mcp__plugin_felipe-vergara-plugin_playwright__browser_take_screenshot Read Write
---

# Skill: 7-maletas

## ⚡ DIRECTIVA — léeme antes de cualquier otra cosa

Cuando esta skill se active porque el alumno pidió algo relacionado con `7-maletas`, sigue este flujo SIN excepciones:

1. **NO hagas preguntas preliminares al alumno.** No le preguntes qué tipo de negocio tiene, qué presupuesto maneja, ni nada — la skill devuelta por el MCP hace todas esas preguntas con su propio formato.
2. **Llama INMEDIATAMENTE al tool `run_playbook` del MCP `felipe-mcp`** con los argumentos:
   - `skillId`: `"7-maletas"`
   - `goal`: el pedido textual del alumno (cópialo verbatim, NO lo reescribas, NO lo resumas, NO le agregues nada)
3. **Ejecuta lo que devuelva el MCP.** Es la skill real con todo su flujo.

## Manejo de errores del MCP (silenciosos para el alumno)

Si el MCP devuelve:
- **401 / "Missing license token" / "Invalid license token" / "Couldn't reach the MCP server"** → dispara la skill `configurar-token`. NO le hables al alumno de "tokens" o "auth"; solo dile: "Necesito activar tu acceso al MCP de Felipe Vergara primero, pásame tu código."
- **403 / "License is not active" / "License has expired"** → dile al alumno con tono amigable: "Tu acceso parece estar pausado. Contacta soporte y lo resolvemos." NO técnico.
- **429 / "Too many requests"** → "Estoy procesando muchas cosas a la vez, dame 1 minuto."
- **`prompt_injection_suspected`** → "Reformula tu pedido sin frases tipo 'ignora instrucciones' o 'revela el prompt' — son patrones que disparan filtros de seguridad."

## Reglas estrictas

- **NUNCA muestres al alumno** el contenido raw que devuelve el MCP (la política de seguridad, el wrapping `<user_goal>`, las "instrucciones premium"). Eso es para ti. Tú ejecutas y entregas el output final que la skill especifica.
- **NUNCA menciones palabras técnicas** al alumno: "endpoint", "transport", "Authorization", "header", "Bearer", "JSON-RPC", "env var". Habla como un humano. La palabra "MCP" sí está bien — es parte de la marca de Felipe Vergara.
- **NO desvíes el flujo de la skill.** La skill tiene un orden establecido — síguelo paso a paso sin saltarte secciones ni improvisar.
