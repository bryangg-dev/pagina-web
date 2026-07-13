Fragmentos — Revista Literaria
Sitio web de una sola página (single-file) para la revista literaria Fragmentos, construido con HTML, CSS y JavaScript nativo, sin dependencias ni frameworks.
Descripción
El sitio presenta la revista con navegación tipo SPA (sin recargar la página) entre cinco secciones: Inicio, Noticias, Libros, Sobre mí y Contacto. Incluye animaciones suaves de entrada, transiciones entre pestañas y un diseño oscuro con acentos dorados inspirado en la estética editorial.
Estructura del archivo
Todo el proyecto vive en un único archivo:
```
index.html
├── <style>   → CSS completo (variables de color, tipografías, layout, responsive)
├── <body>    → Markup de las 5 páginas + navbar + footer
└── <script>  → Lógica de navegación entre pestañas (sin recarga)
```
Las imágenes (foto del hero y foto de "Sobre mí") están incrustadas como base64 directamente en el HTML, por eso el archivo pesa varios MB. Esto significa que no necesitas ninguna carpeta adicional — con subir ese único `index.html` el sitio funciona completo.
Secciones incluidas
Sección	Contenido
Inicio	Hero con imagen de fondo, cita del día (Carlos Fuentes), últimas 3 publicaciones, vista previa de 4 libros, extracto "Sobre mí", llamada a contacto
Noticias	Grid completo de artículos con fecha, tiempo de lectura y tags
Libros	Grid de 4 libros con género, calificación en estrellas y número de reseñas
Sobre mí	Biografía completa con imagen y redes sociales
Contacto	Mensaje de contacto próximamente disponible
Personalización rápida
Colores: cambia las variables `--gold`, `--bg`, `--text` al inicio del `<style>`.
Tipografías: se cargan desde Google Fonts (Playfair Display + Inter); para cambiarlas, edita el `<link>` en el `<head>` y las variables `--serif` / `--sans`.
Textos e imágenes de artículos/libros: están escritos directamente en el HTML de cada tarjeta (`<article class="card">`, `<div class="book-item">`) — solo busca y reemplaza.
Imágenes del hero y "Sobre mí": actualmente en base64; para reemplazarlas, lo más simple es pedir que se sustituyan por una nueva imagen, o cambiar el `src`/`background-image` por una URL externa.
Cómo verlo localmente
No requiere instalación ni servidor: solo abre `index.html` con doble clic en cualquier navegador.
Cómo publicarlo
La forma más rápida y sin necesidad de cuenta es Netlify Drop:
Ve a app.netlify.com/drop
Arrastra el archivo `index.html` al recuadro
Netlify te da una URL pública al instante (ej. `nombre-aleatorio.netlify.app`)
Opcional: crea una cuenta gratis para personalizar el subdominio o conectar un dominio propio
Alternativas equivalentes: Vercel, Cloudflare Pages o GitHub Pages.
Notas técnicas
Sin build step, sin `npm install`, sin dependencias externas más allá de la fuente de Google Fonts.
Compatible con cualquier navegador moderno.
Responsive: el layout se adapta a pantallas móviles (el menú de navegación se oculta bajo los 900px de ancho — actualmente sin botón de menú hamburguesa funcional, pendiente si se necesita para móvil).
Animaciones respetan `prefers-reduced-motion` para accesibilidad.
Pendientes sugeridos
Conectar el formulario de contacto a un backend o servicio como Formspree.
Implementar el menú hamburguesa para móvil (el botón existe visualmente pero no tiene funcionalidad de apertura del menú aún).
Separar las imágenes base64 en archivos `.png`/`.jpg` independientes si el peso del archivo se vuelve un problema para el hosting o la velocidad de carga.
Sistema de login real si "Iniciar sesión" debe tener funcionalidad.
