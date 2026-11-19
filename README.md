# AgroPulse — Landing

Landing page de AgroPulse, gestión agropecuaria para el NOA.
Sitio 100 % estático (HTML + CSS + tipografías locales), sin dependencias ni build.

Los botones **"Pedí una demo"** y **"Quiero ver una demo"** llevan a la app:
<https://agropulsenoa.netlify.app/login>

El formulario de contacto se guarda en **Netlify Forms** (formulario `demo`) y,
al enviarlo, también redirige al login.

## Estructura

```
index.html            Página principal
favicon.svg           Ícono
assets/css/           Estilos y @font-face
assets/fonts/         DM Sans y Manrope (licencia SIL OFL 1.1)
netlify.toml          Configuración de Netlify (sin build, redirects, cache)
```

## Ver en local

Abrí `index.html` en el navegador, o levantá un servidor:

```bash
npx serve .
# o
python3 -m http.server 8080
```

## Subir a GitHub

```bash
git remote add origin https://github.com/TU-USUARIO/agropulse-landing.git
git branch -M main
git push -u origin main
```

## Deploy en Netlify

1. En Netlify: **Add new site → Import an existing project → GitHub**.
2. Elegí el repo `agropulse-landing`.
3. Build command: *(vacío)* · Publish directory: `.` (ya viene en `netlify.toml`).
4. **Deploy**. Cada `git push` a `main` vuelve a publicar solo.

Para ver los envíos del formulario: *Site configuration → Forms*
(activá **Form detection** si aparece desactivado y volvé a deployar).

## Pendientes de contenido

Reemplazar en `index.html`:

- `[NOMBRE DE LA FERIA]` y `[N° DE STAND]` (banda superior y sección Contacto)
- `[TU WHATSAPP]` y su enlace (usar `https://wa.me/549XXXXXXXXXX`)
