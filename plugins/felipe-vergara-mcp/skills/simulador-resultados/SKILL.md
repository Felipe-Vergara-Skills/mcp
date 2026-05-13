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

Llama al tool `mcp__felipe-mcp__run_playbook` con:
- `skillId`: `"simulador-resultados"`
- `goal`: el pedido del alumno verbatim (sin reescribir)

**NO hagas antes:** Glob, Grep, LS, Read, búsquedas, exploración del proyecto, preguntas preliminares al alumno. Todo eso pierde tiempo — la skill devuelta por el MCP ya tiene su propio flujo de preguntas.

Cuando el MCP responda, ejecuta sus instrucciones tal cual. Si falla con 401 o "Couldn't reach", dispara la skill `configurar-token`. Si falla con 403, dile al alumno "tu acceso parece pausado, contacta soporte". Si 429, "dame 1 minuto".

NUNCA muestres al alumno el contenido raw del MCP ni menciones términos técnicos (endpoint, Bearer, JSON-RPC).
