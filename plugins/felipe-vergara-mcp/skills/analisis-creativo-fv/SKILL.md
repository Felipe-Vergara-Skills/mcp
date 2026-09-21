---
name: analisis-creativo-fv
description: >
  Dashboard de DESGLOSE CREATIVO de una cuenta de Meta Ads con la identidad visual de la Comunidad de Felipe Vergara. Trae de la cuenta cada anuncio con su nombre exacto, su copy real y sus métricas creativas (hook rate, retención, CTR saliente, frecuencia, rankings de Meta, CPA y ROAS) y saca en qué etapa pierde cada uno —gancho, retención, clic, landing o conversión—, qué formato y duración funcionan, cuáles están fatigados y qué hacer con cada uno: escalar, mantener, renovar, apagar o darle gasto. Todo sale de la cuenta vía MCP o CSV: no pide transcripciones ni investigación previa. Úsala cuando se pida análisis creativo, desglose por anuncio, tabla de anuncios con métricas, qué anuncio apagar o escalar, fatiga creativa, hook rate, retención de video o qué formato está funcionando. NO la uses para el dashboard de embudo y semáforos de la cuenta (eso es auditoria-completa-meta-ads) ni para construir personas desde reseñas y voz del cliente (eso es auditoria-creativa).
---

# analisis-creativo-fv

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"analisis-creativo-fv"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye la cuenta, el periodo, el modelo de negocio o los archivos que haya dado)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. La skill que devuelve el MCP incluye un PASO 0 de descarga de sus archivos y todo su flujo propio.

Cuando el MCP responda, ejecuta sus instrucciones tal cual — empezando por el PASO 0 (descarga de los archivos de la skill). Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
