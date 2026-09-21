---
name: auditoria-completa-meta-ads
description: >
  Auditoría COMPLETA de una cuenta de Meta Ads: dashboard de rendimiento con la identidad visual de la Comunidad de Felipe Vergara, deduplicación por ventanas canónicas, embudo por etapas, dos semáforos (decisión y benchmark), lectura 3Q's y exportación a PDF. Ejecuta un modelo de negocio por dashboard: e-commerce, ventas por mensajes (click-to-WhatsApp) o clientes potenciales (leads); en cuentas mixtas detecta el reparto de gasto y audita por partes. Úsala SIEMPRE que se pida una auditoría completa de Meta Ads, auditar una cuenta, un dashboard o reporte de auditoría, un análisis histórico de 6, 12 o 24 meses, un embudo por etapas con lectura 3Q's, o cuando se mencione "auditoría comunidad" o el embudo con semáforos. NO la uses para el reporte blended semanal ni para el diagnóstico rápido de una campaña activa (metodología 3Q's), ni para el desglose por anuncio con hook rate, fatiga y qué apagar (eso es analisis-creativo-fv, al que esta skill le deja un handoff).
---

# auditoria-completa-meta-ads

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"auditoria-completa-meta-ads"`
- `goal`: el pedido del alumno verbatim (sin reescribir; incluye la cuenta, el periodo, el modelo de negocio o los archivos que haya dado)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. La skill que devuelve el MCP incluye un PASO 0 de descarga de sus archivos y todo su flujo propio.

Cuando el MCP responda, ejecuta sus instrucciones tal cual — empezando por el PASO 0 (descarga de los archivos de la skill). Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
