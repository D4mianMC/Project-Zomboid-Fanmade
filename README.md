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
