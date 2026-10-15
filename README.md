# Felipe Vergara — MCP

Acceso al MCP de Felipe Vergara con las skills premium del curso para Meta Ads.

---

## 🚀 Cómo instalarlo (3 pasos)

### Paso 1 — Generar tu token de acceso

Entra a **https://cuenta.felipevergara.co** con el email con el que pagaste el curso (te llega un código de 6 dígitos al correo).

→ En tu cuenta, en la sección **🔑 Tu token del MCP**, está tu token que empieza con `fv_…`. Cópialo (botón **Copiar**) y guárdalo bien — se genera una sola vez.

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

Una vez conectado, las 23 skills se disparan por lenguaje natural. Ejemplos:

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
| *"hazme una auditoría completa de mi cuenta"* | `auditoria-completa-meta-ads` |
| *"analiza mis creativos, cuáles están fatigados"* | `analisis-creativo-fv` |

…y 13 skills más. No tienes que memorizar nombres — habla natural y Claude detecta cuál usar.

---

## 🔄 Cómo actualizar (para recibir las skills nuevas)

Las actualizaciones **no llegan solas** a menos que actives la actualización automática. Cuando se anuncie una skill nueva:

1. Actualiza Claude Code a la versión **2.1.296 o superior** (las versiones anteriores tenían un error que hacía fallar las actualizaciones de plugins). En la terminal:
   ```
   claude update
   ```
2. Dentro de Claude Code, corre:
   ```
   /plugin marketplace update felipe-vergara-mcp
   ```
   ```
   /plugin update felipe-vergara-mcp@felipe-vergara-mcp
   ```
3. Reinicia Claude Code (o escribe `/reload-plugins`).

**Para no tener que hacerlo cada vez:** escribe `/plugin` → pestaña **Marketplaces** → elige `felipe-vergara-mcp` → **Enable auto-update**. Desde ahí las skills nuevas se instalan solas.

---

## 🆘 Problemas comunes

**"Couldn't reach the MCP server"** o **"Missing license token"**
→ Tu token no está registrado en este cliente. Repite el Paso 3 con tu token.

**"Este token ya no está activo" / "License is not active" / "License has expired"**
→ Tu token fue renovado (o tu acceso venció). Entra a https://cuenta.felipevergara.co, copia tu token actual en **🔑 Tu token del MCP** y vuelve a conectar: en Claude Code dile a Claude *"configura mi token"*; en Claude Desktop / Cowork edita el conector y vuelve a autorizar con el token nuevo.

**Las skills funcionan en una carpeta pero en otra no**
→ Tu token quedó registrado solo en la carpeta donde lo configuraste (pasaba con versiones del plugin anteriores a la 0.7.1). Actualiza el plugin (ver "Cómo actualizar") y dile a Claude *"configura mi token"* una vez más: ahora queda activo en todas las carpetas. Si en alguna carpeta puntual sigue fallando, repite *"configura mi token"* estando en esa carpeta.

**Las skills no se disparan automáticamente**
→ Reinicia Claude Code completamente (Cmd+Q en Mac; en Windows cierra todas sus ventanas) y vuelve a abrir.

**No me deja actualizar el plugin / sale un error al actualizar**
→ Actualiza primero Claude Code (`claude update`, necesitas la 2.1.296 o superior) y repite los pasos de "Cómo actualizar".

**No tengo el token / lo perdí**
→ Entra a https://cuenta.felipevergara.co con el **mismo email** con el que pagaste: el token está siempre en la sección **🔑 Tu token del MCP** (es el mismo, no se genera uno nuevo).

---

## 🔒 Seguridad

- El token nunca se sube a ningún archivo de tu sistema fuera de la configuración de tu cliente Claude
- El servidor MCP solo te entrega skills si tu token es válido — sin token no hay acceso
- Cada token va vinculado al email con el que pagaste — no se puede compartir entre cuentas

---

**Soporte:** Si algo no funciona, dile a Felipe o al equipo y te lo resolvemos.
