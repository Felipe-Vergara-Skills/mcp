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

# Skill premium: analizador-ads-estaticos

## ⚡ DIRECTIVA — léeme antes de cualquier otra cosa

Cuando esta skill se active porque el alumno pidió algo relacionado con `analizador-ads-estaticos`, sigue este flujo SIN excepciones:

1. **NO hagas preguntas preliminares al alumno.** No le preguntes qué tipo de negocio tiene, qué presupuesto maneja, ni nada — la skill devuelta por el MCP hace todas esas preguntas con su propio formato.
2. **Llama INMEDIATAMENTE al tool `run_playbook` del MCP `felipe-premium`** con los argumentos:
   - `skillId`: `"analizador-ads-estaticos"`
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
