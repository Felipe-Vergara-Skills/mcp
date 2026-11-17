---
name: playbook-errores-meta
description: >
  Traduce cualquier error, aviso o código de Meta Ads a qué significa, por qué te pasa y cómo lo arreglas paso a paso, para que el alumno lo resuelva solo y no dependa del soporte de Meta. Trae un banco de 110 errores ya resueltos (los 44 del Playbook de Errores de Meta Ads de Felipe Vergara más la referencia oficial de la Marketing API); si el error no está, lo investiga en internet con jerarquía de fuentes —primero Meta, después operadores reales, al final blogs—, descarta los mitos de foro, arma la ficha y la guarda en el banco para que la próxima vez la respuesta sea instantánea. Actívala cuando el alumno pegue un código tipo #1487246, #200, #100.33 o cualquier número de error, cuando diga "me sale este error", "no me deja publicar", "qué significa este mensaje", "no puedo guardar la campaña", "error al crear el anuncio", "Meta me dice que...", cuando suba una captura del Administrador de Anuncios con un aviso en rojo, o cuando pida el checklist antes de publicar. También para "busca errores nuevos" o "actualiza el banco de errores". NO resuelve anuncios rechazados por políticas (eso es `revisor-politicas-meta`) ni cuentas inhabilitadas o restringidas: lo dice y deriva.
---

# playbook-errores-meta

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"playbook-errores-meta"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye el código de error, el mensaje o la descripción de la captura que haya dado)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. La skill que devuelve el MCP incluye un PASO 0 de descarga de sus archivos y todo su flujo propio.

Cuando el MCP responda, ejecuta sus instrucciones tal cual — empezando por el PASO 0 (descarga del banco de errores y sus scripts). Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
