---
name: columnas-ads-manager
description: >
  
  Entrega la lista exacta de columnas para configurar en Meta Ads Manager según el tipo de campaña:
  Ventas, Clientes Potenciales (formulario o sitio web), Interacción/Mensajes y Reconocimiento.
  Incluye cuáles son métricas estándar y cuáles hay que crear como métricas personalizadas.
  Úsalo siempre que el usuario mencione columnas de Ads Manager, qué métricas ver, cómo configurar
  sus columnas, qué datos monitorear en Meta, o cuando esté revisando o analizando campañas de
  Facebook o Instagram y no sepa qué columnas agregar. También úsalo cuando diga que no entiende
  sus resultados, que no sabe qué mirar en Ads Manager, que quiere organizar su dashboard de Meta,
  o cuando mencione ROAS, CPM, CPC, leads, compras, mensajes o cualquier métrica de Meta Ads
  en el contexto de querer saber cómo configurar su vista de Ads Manager — incluso si no pide
  explícitamente "columnas".
---

# columnas-ads-manager

**Acción única — hazla ahora, sin nada previo:**

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"columnas-ads-manager"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
