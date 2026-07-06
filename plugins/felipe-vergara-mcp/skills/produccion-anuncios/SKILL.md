---
name: produccion-anuncios
description: >
  Produce una matriz completa de 30 anuncios estáticos para una marca: research estratégico vía MCP de Felipe (brand DNA + 30 hooks de 3 deseos × 2 perfiles × 5 niveles), detección de paleta real desde la URL, render de 30 imágenes on-brand con GPT Image 2 y Excel final. Úsala cuando el alumno diga: producción anuncios, matriz de anuncios, 30 imágenes, anuncio estudiante, o comparta una URL de marca pidiendo la matriz de ads. Solo imágenes estáticas (no video).
---

# produccion-anuncios

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"produccion-anuncios"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye la URL de la marca si la dio)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. La skill que devuelve el MCP incluye un PASO 0 de descarga de sus archivos y todo su flujo propio.

Cuando el MCP responda, ejecuta sus instrucciones tal cual — empezando por el PASO 0 (descarga del paquete de scripts). Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
