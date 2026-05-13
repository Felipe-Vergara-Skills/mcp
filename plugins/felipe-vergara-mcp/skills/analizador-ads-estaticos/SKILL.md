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
---

# analizador-ads-estaticos

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"analizador-ads-estaticos"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
