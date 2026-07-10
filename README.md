# Ask-IA

Sesión de **espiritismo digital**: una sola página HTML que invoca entidades, voz sintética y chat vía [OpenRouter](https://openrouter.ai).

## Uso

1. Abre `index.html` en el navegador (o sirve la carpeta con cualquier servidor estático).
2. La API key de OpenRouter viene precargada para que funcione al instante; puedes cambiarla en el formulario.
3. Elige modelo (por defecto `deepseek/deepseek-v4-flash`) y sigue las instrucciones en pantalla.

## Archivos

- `index.html` — app completa (antes `hola-mundo-poseido.html` en el proyecto CURSED HELLO).

## Aviso

La clave en el HTML es de uso desechable; no la reutilices en producción ni la compartas si te importa el saldo de la cuenta.

## Deploy en Render (static site)

Este repo **no tiene build**: el sitio es solo `index.html` en la raíz.

### Blueprint (`render.yaml`)

Si conectas el repo como **Blueprint**, Render usará `staticPublishPath: .` (publicar la raíz del repo).

### Ajustes manuales en el dashboard

En **ask-ia** → **Settings**:

| Campo | Valor correcto |
|--------|----------------|
| **Environment** | Static Site |
| **Branch** | `main` |
| **Root Directory** | *(vacío)* |
| **Build Command** | *(vacío)* — no ejecutar `npm` ni otro build |
| **Publish Directory** | `.` |

Si **Publish Directory** apunta a `dist`, `build`, `public`, etc., o el **Build Command** falla, Render publica una carpeta vacía y verás **404**.

Tras cambiar settings: **Manual Deploy** → **Deploy latest commit**.
