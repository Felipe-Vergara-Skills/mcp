---
name: auditoria-de-anuncios-meta
description: >
  Auditoría de anuncios en Meta por PERSONA y por CONCEPTO. Identifica las personas reales de una marca desde la voz del cliente, lee la comunicación que corre hoy en la Biblioteca de Anuncios de Meta y las métricas del conector MCP, y las cruza en una MATRIZ persona × concepto donde cada casilla vacía es un hueco de oportunidad. Entrega la brecha voz vs gasto, la matriz y las ideas para cada hueco en un HTML con gráficos. Activa si mencionan: auditoría de anuncios, auditoría de personas, buyer persona, a quién le hablo, voz del cliente, todos mis anuncios dicen lo mismo, se me estancó el alcance, ideas de anuncios, personas desatendidas, públicos sin atacar, matriz de cruce, huecos de oportunidad, qué concepto no he probado. NO es el dashboard por anuncio con hook rate y fatiga (analisis-creativo-fv) ni el de cuenta con embudo y 3Q's (auditoria-completa-meta-ads).
---

# auditoria-de-anuncios-meta

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"auditoria-de-anuncios-meta"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye la marca, la URL o el nombre de la cuenta si lo dio)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. La skill que devuelve el MCP incluye un PASO 0 de descarga de sus archivos y todo su flujo propio.

Cuando el MCP responda, ejecuta sus instrucciones tal cual — empezando por el PASO 0 (descarga del paquete de scripts y referencias). Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
