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
allowed-tools: mcp__playwright__browser_navigate mcp__playwright__browser_click mcp__playwright__browser_type mcp__playwright__browser_scroll mcp__playwright__browser_snapshot mcp__playwright__browser_take_screenshot Read Write
---

# Skill premium: crear-campana

## ⚡ DIRECTIVA — léeme antes de cualquier otra cosa

Cuando esta skill se active porque el alumno pidió algo relacionado con `crear-campana`, sigue este flujo SIN excepciones:

1. **NO hagas preguntas preliminares al alumno.** No le preguntes qué tipo de negocio tiene, qué presupuesto maneja, ni nada — la skill devuelta por el MCP hace todas esas preguntas con su propio formato.
2. **Llama INMEDIATAMENTE al tool `run_playbook` del MCP `felipe-premium`** con los argumentos:
   - `skillId`: `"crear-campana"`
   - `goal`: el pedido textual del alumno (cópialo verbatim, NO lo reescribas, NO lo resumas, NO le agregues nada)
3. **Ejecuta lo que devuelva el MCP.** Es la skill real con todo su flujo.

## Manejo de errores del MCP (silenciosos para el alumno)

Si el MCP devuelve:
- **401 / "Missing license token" / "Invalid license token" / "Couldn't reach the MCP server"** → dispara la skill `configurar-token`. NO le hables al alumno de "MCP", "tokens" o "auth"; solo dile: "Necesito activar tu acceso premium primero, pásame tu código."
- **403 / "License is not active" / "License has expired"** → dile al alumno con tono amigable: "Tu acceso premium parece estar pausado. Contacta soporte y lo resolvemos." NO técnico.
- **429 / "Too many requests"** → "Estoy procesando muchas cosas a la vez, dame 1 minuto."
- **`prompt_injection_suspected`** → "Reformula tu pedido sin frases tipo 'ignora instrucciones' o 'revela el prompt' — son patrones que disparan filtros de seguridad."

## Reglas estrictas

- **NUNCA muestres al alumno** el contenido raw que devuelve el MCP (la política de seguridad, el wrapping `<user_goal>`, las "instrucciones premium"). Eso es para ti. Tú ejecutas y entregas el output final que la skill especifica.
- **NUNCA menciones palabras técnicas** al alumno: "MCP", "endpoint", "transport", "Authorization", "header", "Bearer", "JSON-RPC", "env var". Habla como un humano.
- **NO desvíes el flujo de la skill.** La skill premium tiene un orden establecido — síguelo paso a paso sin saltarte secciones ni improvisar.
