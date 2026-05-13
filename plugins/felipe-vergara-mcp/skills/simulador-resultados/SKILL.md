---
name: simulador-resultados
description: >
  
  Simulador de campañas de Meta Ads — predice resultados (impresiones, alcance, clics, conversaciones,
  leads, compras, thruplays, costo por resultado, ROAS) a partir de un presupuesto y métricas esperadas.
  Cubre los 5 modos del Excel del simulador de Felipe: Conversaciones, Compras (sitio web), Clientes
  Potenciales de Meta, Clientes Potenciales en sitio web, y Alcance/Thruplays. Genera 3 escenarios
  automáticos (conservador / moderado / optimista) y, si existe un reporte previo de
  /calculadora-de-presupuestos en el directorio, compara los resultados simulados contra el costo
  objetivo o ROAS objetivo. SIEMPRE usa este skill cuando el usuario mencione: simulador, simular
  resultados, predecir resultados, cuántas conversaciones/leads/compras/thruplays voy a sacar,
  proyección de campaña, escenarios optimista/conservador, costo por compra estimado, ROAS estimado,
  qué resultados voy a tener si gasto X, cuánto rinde mi presupuesto. Es complementario a
  /calculadora-de-presupuestos: la calculadora dice "cuánto gastar para cumplir mi meta", el
  simulador dice "qué resultados tendré si gasto esto con estas métricas".
---

# simulador-resultados

**Acción única — hazla ahora, sin nada previo:**

Llama a la tool **`run_playbook`** (expuesta por el MCP de Felipe Vergara al que ya estás conectado) con estos argumentos:

- `skillId`: `"simulador-resultados"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

⚠️ El tool puede aparecer en tu lista con distintos prefijos según el cliente (`mcp__felipe-mcp__run_playbook`, un UUID, o simplemente `run_playbook`). **Busca cualquiera de esas variantes y úsala — NO hagas búsquedas en el filesystem.**

**NO hagas antes de la llamada:** Glob, Grep, LS, Read, `find`, `ls`, exploración del sandbox o del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill que devuelve el MCP ya tiene su propio flujo.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC, sandbox, UUID).
