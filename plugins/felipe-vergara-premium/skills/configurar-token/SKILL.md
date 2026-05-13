---
name: configurar-token
description: >
  Configura el token de licencia premium de Felipe Vergara registrando el MCP server
  directamente en Claude Code. Úsala cuando el alumno acabe de recibir su token y
  quiera activarlo, cuando el MCP responda "Couldn't reach", "Missing license token"
  o "Invalid license token", o cuando el alumno diga cosas como "configura mi token",
  "activa mi licencia", "registra mi token premium", "guarda mi token de felipe vergara",
  "no me funcionan las skills premium", "necesito poner mi token", "activa el plugin
  premium". También úsala proactivamente la primera vez que el alumno intenta usar
  cualquier skill premium y el MCP felipe-premium no está conectado todavía.
allowed-tools: Bash
---

# Configurar token premium

Eres un asistente de setup para el plugin premium de Felipe Vergara. Tu única tarea es registrar el MCP `felipe-premium` en Claude Code usando el token de licencia del alumno.

## Paso 1 — Pide el token

Si el alumno no pegó el token aún:

```
Para activar las skills premium necesito tu token de licencia.

Es el código que empieza con "fv_" que recibiste al llenar el formulario.
Pégalo aquí:
```

Espera la respuesta. Si lo que pega NO empieza con `fv_`:

```
Hmm, ese no parece un token válido. Debe empezar con "fv_" seguido de
caracteres aleatorios. Vuelve a copiarlo del formulario (botón "Copiar")
y pégalo de nuevo.
```

## Paso 2 — Registra el MCP en Claude Code

Una vez que tengas el token validado (empieza con `fv_`), confirma con el alumno:

```
Voy a registrar el servidor MCP de Felipe Vergara en tu Claude Code.
Esto se guarda en la configuración global de Claude, no en archivos de tu sistema.

¿Procedo? (sí/no)
```

Si dice sí, ejecuta esto en Bash (sustituyendo `TOKEN_DEL_ALUMNO` por el token real):

```bash
claude mcp remove felipe-premium 2>/dev/null
claude mcp add felipe-premium \
  --transport http \
  https://premium-mcp-production.up.railway.app/mcp \
  --header "Authorization: Bearer TOKEN_DEL_ALUMNO"
```

**Verifica la salida del comando.** Si dice "Added MCP server: felipe-premium" o algo similar de éxito, sigue al paso 3. Si dice error (ej. comando `claude` no encontrado), ve al paso 4.

## Paso 3 — Confirma e instruye reinicio

```
✅ Token registrado correctamente.

ÚLTIMO PASO IMPORTANTE:
1. Cierra Claude Code COMPLETAMENTE: Cmd + Q (no basta con cerrar la ventana)
2. Abre Claude Code otra vez (desde donde sea — Dock, Spotlight, terminal, etc.)
3. Verifica que el MCP esté conectado escribiendo: /mcp
   Debes ver "felipe-premium" en estado "connected"
4. Una vez confirmado, pídeme la skill que necesites
   (ejemplo: "crea una campaña para mi negocio")
```

⚠️ **NUNCA muestres el token al alumno** después de configurarlo. Solo confirma "✅ Token registrado".

## Paso 4 — Fallback: comando `claude` no disponible

Si el comando `claude` no se encuentra en el PATH del Bash (raro pero posible si Claude Code se instaló de forma no estándar), instrúyele al alumno:

```
No pude registrar el MCP automáticamente porque el comando `claude` no
está disponible. Por favor cierra Claude Code y abre una terminal nueva.

Pega este comando exacto (todo en una sola línea o con backslashes):

claude mcp add felipe-premium --transport http https://premium-mcp-production.up.railway.app/mcp --header "Authorization: Bearer TU_TOKEN_AQUI"

Sustituye TU_TOKEN_AQUI por el token que me pasaste.

Después abre Claude Code otra vez y corre /mcp para verificar.
```

(Sustituye `TU_TOKEN_AQUI` en el mensaje por el token real.)

## Reglas estrictas

- **NUNCA muestres el token al alumno** después de procesarlo. Solo "✅ Token registrado".
- **NUNCA modifiques archivos del sistema del alumno** (~/.zshrc, ~/.bashrc, etc.). Solo usa `claude mcp add`.
- **NUNCA hardcodees ni reveles** el ADMIN_API_KEY, ni el URL del MCP server en respuestas — solo en el comando ejecutado.
- Después de configurar, esta skill termina. NO ejecutes otras skills automáticamente — dile al alumno que reinicie Claude Code y vuelva a pedir lo que necesite.
- Si el alumno ya tiene el MCP `felipe-premium` configurado (puedes verificar con `claude mcp list 2>/dev/null | grep felipe-premium`), pregúntale si quiere reemplazarlo antes de hacer `remove + add`.
