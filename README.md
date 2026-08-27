# Portfolio Félix Pago — Lautaro Castillo (EN)

Sitio estático (HTML + Tailwind CDN, sin build step) — versión en inglés, generada a partir
del contenido actual del frame de Figma (node 6:2). Contenido centrado con un ancho máximo
de 1080px (como referencia usamos el portfolio de Agustina Bovero), responsive (mobile-first),
con nav sticky, menú hamburguesa, scroll-spy y tipografía PP Neue Montreal real (WOFF2) en
`/assets/fonts`.


## ⚠️ Licencia de la fuente — leer antes de publicar

El EULA de Pangram Pangram para PP Neue Montreal (versión gratuita) dice textual:

> "the Licensee may use a Font freely for its personal use, as long as [...] it does not use
> the Font on a publicly available platform such as a website [...] Otherwise, the Licensee
> must purchase the appropriate commercial License"

Es decir: la licencia free **no cubre uso en un sitio público**. Si vas a dejar este
portfolio online en Vercel con esta fuente embebida, tenés que comprar la licencia
comercial correspondiente en pangrampangram.com. (No soy abogado — esto es una lectura
literal del PDF que subiste, no asesoramiento legal.)

## ⚠️ Imágenes temporales

Las imágenes de captura de pantalla siguen apuntando a URLs temporales de Figma
(`https://www.figma.com/api/mcp/asset/...`) que caducan en ~7 días. Para producción:

1. En Figma, exportá cada imagen (los `alt=""` del HTML indican cuál es cuál).
2. Guardalas en `/assets` (podés crear `/assets/screens`).
3. Reemplazá cada `src="https://www.figma.com/..."` por la ruta local.

## Cómo deployar en Vercel

### Opción A — Sin usar terminal (más simple)
1. Andá a [github.com/new](https://github.com/new) y creá un repo (ej. `portfolio-felix`).
2. Subí `index.html` y la carpeta `assets` completa (con `assets/fonts`) arrastrando
   los archivos directo en la web de GitHub ("uploading an existing file").
3. Andá a [vercel.com/new](https://vercel.com/new), conectá tu cuenta de GitHub,
   elegí el repo `portfolio-felix` y hacé clic en "Deploy". Vercel detecta que es
   HTML estático automáticamente, no necesita configuración.
4. En 1-2 minutos te da una URL tipo `portfolio-felix.vercel.app`.

### Opción B — Con terminal (git + Vercel CLI)
```bash
cd felix-portfolio
git init
git add .
git commit -m "Portfolio inicial"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/portfolio-felix.git
git push -u origin main
```
Después, en [vercel.com/new](https://vercel.com/new) importás ese repo igual que en la Opción A.

O directo con la CLI de Vercel (sin pasar por GitHub):
```bash
npm install -g vercel
cd felix-portfolio
vercel
```
Te va a pedir loguearte (abre el navegador) y con responder las preguntas por default
ya te deja el sitio publicado.

### Dominio propio
Una vez deployado, en el dashboard de Vercel → tu proyecto → Settings → Domains
podés apuntar un dominio propio si tenés uno.


### Opción A — Sin usar terminal (más simple)
1. Andá a [github.com/new](https://github.com/new) y creá un repo (ej. `portfolio-felix`).
2. Subí `index.html` (y la carpeta `assets` si ya la armaste) arrastrando los archivos
   directo en la web de GitHub ("uploading an existing file").
3. Andá a [vercel.com/new](https://vercel.com/new), conectá tu cuenta de GitHub,
   elegí el repo `portfolio-felix` y hacé clic en "Deploy". Vercel detecta que es
   HTML estático automáticamente, no necesita configuración.
4. En 1-2 minutos te da una URL tipo `portfolio-felix.vercel.app`.

### Opción B — Con terminal (git + Vercel CLI)
```bash
cd felix-portfolio
git init
git add .
git commit -m "Portfolio inicial"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/portfolio-felix.git
git push -u origin main
```
Después, en [vercel.com/new](https://vercel.com/new) importás ese repo igual que en la Opción A.

O directo con la CLI de Vercel (sin pasar por GitHub):
```bash
npm install -g vercel
cd felix-portfolio
vercel
```
Te va a pedir loguearte (abre el navegador) y con responder las preguntas por default
ya te deja el sitio publicado.

### Dominio propio
Una vez deployado, en el dashboard de Vercel → tu proyecto → Settings → Domains
podés apuntar un dominio propio si tenés uno.
