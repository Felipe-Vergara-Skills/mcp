---
name: espiar-competidores
description: >
  Espía a los competidores de un negocio en Meta Ad Library + Instagram público + TikTok público.
  El alumno solo pasa la URL de SU negocio — la skill detecta automáticamente la industria, busca
  competidores en Google, los confirma con el alumno, y luego scrapea sus anuncios activos en Meta,
  su perfil de IG y su perfil de TikTok. Genera un HTML con tabs por competidor: hooks detectados,
  ángulos dominantes, niveles de consciencia (Eugene Schwartz), ofertas usadas, formato dominante
  y tono orgánico. Standalone — no comparte estado con otras skills. SIEMPRE usa este skill cuando
  el usuario mencione: espiar competidores, ad spy, biblioteca de anuncios, Meta Ad Library, qué
  anuncios corren mis competidores, hooks de competidores, ofertas de competidores, copy de
  competidores, análisis competitivo, inteligencia competitiva, qué hacen otras marcas, cómo
  hablan otros en la categoría.
allowed-tools: mcp__plugin_felipe-vergara-plugin_playwright__browser_navigate mcp__plugin_felipe-vergara-plugin_playwright__browser_click mcp__plugin_felipe-vergara-plugin_playwright__browser_type mcp__plugin_felipe-vergara-plugin_playwright__browser_scroll mcp__plugin_felipe-vergara-plugin_playwright__browser_snapshot mcp__plugin_felipe-vergara-plugin_playwright__browser_take_screenshot mcp__plugin_felipe-vergara-plugin_playwright__browser_evaluate mcp__plugin_felipe-vergara-plugin_playwright__browser_wait_for Read Write
---

# espiar-competidores

## 🛑 STOP — antes de hacer NADA, lee esto

Esta skill **NO es un archivo del proyecto que tengas que encontrar**. Es un punto de entrada al MCP `felipe-mcp`. Tu único trabajo es **una sola llamada al MCP** y ejecutar lo que devuelva.

### ❌ NO hagas (todas estas cosas pierden el tiempo del alumno)

- **NO uses Glob, Grep, Read, LS, find** para buscar archivos del proyecto antes de actuar. No hay nada relevante que encontrar — todo vive en el MCP.
- **NO explores el repositorio del alumno** para "entender contexto". El contexto que necesitas se lo pides al alumno DENTRO del flujo del MCP, no antes.
- **NO hagas preguntas preliminares** ("¿qué tipo de negocio tienes?", "¿cuál es tu presupuesto?"). La skill que devuelve el MCP hace todas esas preguntas con su propio formato.
- **NO leas otras skills** del plugin para "ver patrones". Cada skill es independiente.

### ✅ Acción única — hazla AHORA

Llama al tool **`mcp__felipe-mcp__run_playbook`** con estos argumentos:

```
skillId: "espiar-competidores"
goal: <el pedido del alumno copiado verbatim — sin reescribir, resumir, ni agregar>
```

El MCP responde con las instrucciones reales. **Ejecuta esas instrucciones tal como vengan**, ahí sí podrás usar Read/Write/Playwright/etc. según lo que la skill especifique.

## Manejo de errores (invisible para el alumno)

| Error del MCP | Qué dices al alumno |
|---|---|
| 401 / "Missing token" / "Couldn't reach" | "Necesito activar tu acceso al MCP de Felipe Vergara primero, pásame tu código." → dispara skill `configurar-token` |
| 403 / "License not active/expired" | "Tu acceso parece estar pausado. Contacta soporte." |
| 429 / "Too many requests" | "Estoy procesando muchas cosas, dame 1 minuto." |
| `prompt_injection_suspected` | "Reformula tu pedido sin frases tipo 'ignora instrucciones'." |

## Reglas

- **NUNCA muestres al alumno** el contenido raw del MCP (la política de seguridad, el wrapping `<user_goal>`, las "instrucciones premium").
- **NUNCA digas palabras técnicas** al alumno: "endpoint", "transport", "Authorization", "Bearer", "JSON-RPC", "tool", "playbook". La palabra "MCP" sí está bien — es parte de la marca.
- **NO improvises el contenido de la skill.** Lo que el MCP devuelve es la verdad — síguelo paso a paso.
