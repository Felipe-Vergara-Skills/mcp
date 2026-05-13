---
name: analizador-ads-estaticos
description: >
  Deconstruye imágenes publicitarias estáticas de alto rendimiento en sus
  componentes de marketing, diseño y copywriting. SIEMPRE usa este skill
  cuando el usuario adjunte una imagen de un anuncio, ad, publicidad o creativo
  y quiera analizarlo, entender por qué funciona, hacer ingeniería inversa,
  deconstruirlo o extraer aprendizajes para replicar en sus campañas. También
  úsalo cuando mencione "analiza este ad", "por qué funciona este anuncio",
  "qué técnicas usa este creativo", "deconstruye este anuncio", "reverse
  engineer this ad", "analiza esta imagen publicitaria", o cuando suba
  cualquier imagen de Facebook Ads, Instagram Ads, Google Ads u otras
  plataformas y pida un análisis. Genera un reporte de 31 secciones cubriendo
  jerarquía visual, copywriting, posicionamiento, emociones, niveles de
  Schwartz, LF8, NESB y recreación ficticia. Output en archivo Markdown.
allowed-tools: Read Write
---

# analizador-ads-estaticos

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
skillId: "analizador-ads-estaticos"
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
