# Project Zomboid Web Demo

Este proyecto es una página web estática. Para compartirla con un amigo hay dos formas principales:

## 1. Probar localmente

Si tu amigo está en la misma red local y quieres que lo abra desde tu PC:

1. Abre una terminal en `C:\Users\59263376\Desktop\project zomboid`
2. Ejecuta:

```powershell
python -m http.server 8000
```

3. Abre en tu navegador:

```text
http://localhost:8000/projectzomboid.html
```

Tu amigo solo podrá abrirlo si también puede acceder a tu equipo desde la red local. En ese caso usa la IP de tu PC en lugar de `localhost`, por ejemplo:

```text
http://192.168.1.100:8000/projectzomboid.html
```

## 2. Publicarlo en Internet (recomendado)

La mejor opción para enviar un link a un amigo es usar un servicio de hosting estático. GitHub Pages es el más sencillo:

1. Crea un repositorio en GitHub.
2. Sube todos los archivos del proyecto (`projectzomboid.html`, `css/`, `js/`, etc.).
3. En la configuración del repositorio activa GitHub Pages desde la rama `main` y la carpeta `/`.
4. El enlace quedará en la forma:

```text
https://<tu-usuario>.github.io/<tu-repo>/projectzomboid.html
```

También puedes usar Netlify o Vercel si prefieres.

## 3. Si solo quieres un link rápido desde tu PC

Puedes usar `ngrok` para exponer tu servidor local a Internet:

```powershell
ngrok http 8000
```

y compartir el link que `ngrok` genere.

---

### Nota
El proyecto ya está listo como página estática: `projectzomboid.html` con `css/style.css` y los scripts embebidos.

## 4. Preparar el repositorio con Git

Si quieres subirlo a GitHub, estos son los pasos básicos desde el directorio del proyecto:

```powershell
# instalar git si no lo tienes
# https://git-scm.com/downloads

git init
git add .
git commit -m "Initial project commit"
```

Luego crea el repositorio en GitHub y enlázalo con:

```powershell
git remote add origin https://github.com/<tu-usuario>/<tu-repo>.git
git branch -M main
git push -u origin main
```

Después activa GitHub Pages en la configuración del repositorio para servir la página.
