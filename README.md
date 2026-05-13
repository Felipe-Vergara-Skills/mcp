# Felipe Vergara — MCP

Acceso al MCP de Felipe Vergara con las skills premium del curso para Meta Ads.

---

## 🚀 Cómo instalarlo (3 pasos)

### Paso 1 — Generar tu token de acceso

Entra a **https://felipevergara.co/formulario/** y llena el formulario con el email con el que pagaste el curso.

→ El form te entregará un token que empieza con `fv_…`. Cópialo (botón **Copiar**) y guárdalo bien — solo se muestra una vez.

### Paso 2 — Instalar el plugin

Abre **Claude Code** (o el cliente que uses) y corre:

```
/plugin marketplace add Felipe-Vergara-Skills/mcp
```

```
/plugin install felipe-vergara-mcp@felipe-vergara-mcp
```

### Paso 3 — Conectar el MCP con tu token

Tienes dos caminos según qué cliente uses:

#### 🅰️ Si usas Cowork / Claude Desktop (la app de Anthropic)

1. Ve a **Conectores → Agregar conector personalizado**
2. URL del servidor:
   ```
   https://premium-mcp-production.up.railway.app/mcp
   ```
3. Click **Conectar**
4. Se abre el navegador con un formulario de autorización — **pega tu token** y click **Autorizar**
5. Listo ✅

#### 🅱️ Si usas Claude Code CLI (terminal)

Después de instalar el plugin (Paso 2), dile a Claude en el chat:

> *configura mi token*

La skill `configurar-token` te pide el token, lo registra y te avisa cuándo reiniciar Claude Code.

---

## 🎯 Cómo usar las skills

Una vez conectado, las 16 skills se disparan por lenguaje natural. Ejemplos:

| Lo que dices | Skill que se activa |
|---|---|
| *"crea una campaña para mi negocio de pizzas en CDMX"* | `crear-campana` |
| *"analiza mis campañas activas"* | `analizar-campana` |
| *"investiga las 7 maletas para [URL]"* | `7-maletas` |
| *"calcula mi presupuesto"* | `calculadora-de-presupuestos` |
| *"dame hooks creativos"* | `diversificacion-creativa` |
| *"diagnostica el nivel de consciencia"* | `niveles-de-consciencia` |
| *"espiame los anuncios de competidores"* | `espiar-competidores` |
| *"genera nombres para mis campañas"* | `generador-de-nombres` |

…y 8 skills más. No tienes que memorizar nombres — habla natural y Claude detecta cuál usar.

---

## 🆘 Problemas comunes

**"Couldn't reach the MCP server"** o **"Missing license token"**
→ Tu token no está registrado en este cliente. Repite el Paso 3 con tu token.

**"License has expired" / "License is not active"**
→ Tu acceso fue revocado. Contacta soporte.

**Las skills no se disparan automáticamente**
→ Reinicia Claude Code completamente (Cmd+Q en Mac, salir de la app) y vuelve a abrir.

**No tengo el token / lo perdí**
→ Vuelve a llenar el formulario en https://felipevergara.co/formulario/ con el **mismo email**. El sistema te devolverá el mismo token (no genera uno nuevo).

---

## 🔒 Seguridad

- El token nunca se sube a ningún archivo de tu sistema fuera de la configuración de tu cliente Claude
- El servidor MCP solo te entrega skills si tu token es válido — sin token no hay acceso
- Cada token va vinculado al email con el que pagaste — no se puede compartir entre cuentas

---

**Soporte:** Si algo no funciona, dile a Felipe o al equipo y te lo resolvemos.
