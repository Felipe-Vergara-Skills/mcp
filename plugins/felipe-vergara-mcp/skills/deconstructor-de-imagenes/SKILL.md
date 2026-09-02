---
name: deconstructor-de-imagenes
description: >
  Convierte un anuncio estático que ya funciona en un PROMPT JSON listo para recrearlo con el producto del alumno; opcionalmente genera la imagen con Kie. Úsala cuando el alumno quiera REPLICAR o ADAPTAR un anuncio a su propio producto: "quiero replicar este anuncio", "adáptalo a mi producto", "dame el prompt de este anuncio", "recrea este creativo con mi marca". Entrega un .md con el análisis y el prompt JSON. NO la uses si el alumno solo quiere ENTENDER por qué funciona un anuncio o pide un análisis/estudio — para eso está analizador-ads-estaticos. Regla: si quiere un PROMPT o una IMAGEN, es esta skill; si quiere un ESTUDIO, es la otra.
---

# deconstructor-de-imagenes

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"deconstructor-de-imagenes"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye el anuncio, la URL del producto o los datos que haya dado)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. La skill que devuelve el MCP incluye un PASO 0 de descarga de sus archivos y todo su flujo propio.

Cuando el MCP responda, ejecuta sus instrucciones tal cual — empezando por el PASO 0 (descarga del paquete de scripts). Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
