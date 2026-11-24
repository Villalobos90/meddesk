# Sitio web de MEDDESK (`web\`)

Sitio estático en un solo archivo (`index.html` + `icon.png`) sin dependencias externas ni rastreadores.

## Antes de publicar

1. Abre `web\index.html` y reemplaza `CONTACTO_AQUI` (al pie de la página) por el correo o enlace de contacto real.
2. Verifica la constante `DOWNLOAD_URL` al inicio de `web\index.html` y el atributo `href` de `#downloadLink`:
   ```js
   const DOWNLOAD_URL = "https://github.com/Villalobos90/meddesk/releases/latest/download/MEDDESK_Setup.exe";
   ```
3. Asegúrate de publicar el archivo `MEDDESK_Setup.exe` en un *Release* de GitHub en ese repositorio para que el enlace `/releases/latest/download/MEDDESK_Setup.exe` apunte siempre a la versión más reciente.

## Cómo publicar gratis en GitHub Pages

1. Sube la carpeta `web\` al repositorio de GitHub (en la rama principal, p. ej. `main`).
   - Nota: si la rama activa está en un repositorio distinto al de los releases, ajusta `DOWNLOAD_URL`.
2. En GitHub, entra a **Settings → Pages**.
3. En **Source**, elige **Deploy from a branch**.
4. Selecciona la rama principal y la carpeta `/web` (o copia `index.html` e `icon.png` a `/docs` o a la raíz de un repositorio `usuario.github.io` si tu plan de GitHub requiere `/docs` o raíz).
   - *Tip*: si GitHub Pages solo ofrece `/` (raíz) o `/docs`, puedes crear un repositorio público dedicado (por ejemplo `meddesk-web`) con únicamente `index.html` e `icon.png` en la raíz `/` y publicar el instalador en los Releases de `Villalobos90/meddesk`.
5. Guarda los cambios; en 1–2 minutos GitHub mostrará la URL pública HTTPS del sitio.
