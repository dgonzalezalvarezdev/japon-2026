# Ruta Japón 2026

Itinerario del viaje a Japón (28 oct → 16 nov 2026). Web estática de un solo archivo, sin build.

```
index.html      la web completa (HTML + CSS + JS inline)
og-image.png    imagen de vista previa al compartir el enlace
.nojekyll       evita que GitHub Pages procese el sitio con Jekyll
```

## Publicarlo en GitHub Pages

**Desde la terminal**

```bash
cd japon-2026
git init -b main
git add .
git commit -m "Ruta Japón 2026"
gh repo create japon-2026 --public --source=. --push   # o crea el repo en github.com y haz git remote add + git push
```

**Activar Pages:** en el repo, *Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save*.
En 1–2 minutos estará en:

```
https://TU-USUARIO.github.io/japon-2026/
```

## Un último ajuste para la vista previa en WhatsApp

WhatsApp y Telegram necesitan la URL absoluta de la imagen. En `index.html` cambia:

```html
<meta property="og:image" content="og-image.png">
```

por:

```html
<meta property="og:image" content="https://TU-USUARIO.github.io/japon-2026/og-image.png">
```

y añade debajo:

```html
<meta property="og:url" content="https://TU-USUARIO.github.io/japon-2026/">
```

## Notas

- El repo tiene que ser público para usar Pages gratis. Si no quieres que se indexe, añade `<meta name="robots" content="noindex">` en el `<head>`.
- Lo que cada uno marca en la pestaña Reservas se guarda en su propio navegador (localStorage), no se comparte entre vosotros.
- Enlaces directos a una pestaña: `#itinerario`, `#viabilidad`, `#transporte`, `#comida`, `#pop`, `#reservas`.
- Para actualizar: edita `index.html`, `git commit` y `git push`. Pages se redespliega solo.
