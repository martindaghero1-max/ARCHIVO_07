# ARCHIVO 07 — Misión Asteria

Ficción interactiva estilo terminal retro. Es un único archivo HTML
autocontenido (`index.html`): no necesita build, ni dependencias, ni
carpetas extra. Los videos se reproducen embebidos desde YouTube; la
única imagen del recorrido (registro médico) va incrustada en base64
dentro del mismo archivo.

## Subir el repo a GitHub

Desde esta carpeta (donde está `index.html`):

```bash
git init
git add .
git commit -m "Archivo 07: ficción interactiva"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
git push -u origin main
```

Reemplazá `TU_USUARIO/TU_REPO` por los datos de tu repositorio ya
creado en GitHub (crealo vacío primero, sin README, desde
github.com/new).

## Publicarlo con GitHub Pages (para jugarlo desde un link)

1. En GitHub, andá a **Settings → Pages** del repositorio.
2. En **Build and deployment → Source**, elegí **Deploy from a branch**.
3. En **Branch**, elegí `main` y la carpeta `/ (root)`. Guardá.
4. Esperá 1–2 minutos. El sitio queda publicado en:
   `https://TU_USUARIO.github.io/TU_REPO/`

Como el archivo se llama `index.html`, GitHub Pages lo sirve
automáticamente como página principal.

## Notas

- No hace falta subir ninguna carpeta de videos: todo el material
  audiovisual pesado vive en YouTube y se referencia por ID dentro del
  HTML.
- Si en algún momento cambiás un video, buscá su ID dentro de
  `index.html` (bloque `const NODES = {...}`, campo `media.id`) y
  reemplazalo por el nuevo.
- El ambiente sonoro (drone, tics de tipeo, chime al elegir opción) se
  genera en el navegador con Web Audio, no depende de archivos.
