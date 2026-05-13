---
name: calculadora-de-presupuestos
description: >
  Calcula el presupuesto exacto para campañas de Facebook e Instagram Ads y el ROAS objetivo
  usando la calculadora de Felipe Vergara. Úsalo siempre que el usuario quiera saber cuánto
  invertir en Meta Ads, cuál es su presupuesto para anuncios, cuánto necesita gastar en Facebook
  o Instagram, cuál es su ROAS objetivo, cuál es su número mágico, costo por compra objetivo,
  costo por lead objetivo, costo por conversación objetivo, o cuando diga que no sabe cuánto
  presupuesto poner en sus campañas. También úsalo si menciona que quiere calcular su inversión
  en publicidad, rentabilidad de sus anuncios, o cuánto puede pagar por un cliente — incluso si
  no dice explícitamente "calculadora" o "presupuesto".
---

# Skill: calculadora-de-presupuestos

## ⚡ DIRECTIVA — léeme antes de cualquier otra cosa

Cuando esta skill se active porque el alumno pidió algo relacionado con `calculadora-de-presupuestos`, sigue este flujo SIN excepciones:

1. **NO hagas preguntas preliminares al alumno.** No le preguntes qué tipo de negocio tiene, qué presupuesto maneja, ni nada — la skill devuelta por el MCP hace todas esas preguntas con su propio formato.
2. **Llama INMEDIATAMENTE al tool `run_playbook` del MCP `felipe-mcp`** con los argumentos:
   - `skillId`: `"calculadora-de-presupuestos"`
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
