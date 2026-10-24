# Spotify en Proyectos

La sección vive en `index.html` y reutiliza `.project-card` dentro de `.project-swiper`. La nueva tarjeta tiene `data-category="spotify"` y enlaza al artista https://open.spotify.com/artist/0xpHZtj5J58MrlpPzBWBZF.

Se agregó el filtro Spotify y se normalizó la etiqueta YouTube. La lógica existente en `assets/js/main.js` ya filtra por categoría y restaura todas las tarjetas con `all`; no requirió cambios. Se conservan los estilos, los tres proyectos en escritorio y el carrusel adaptable en móvil. Los enlaces externos de las tres tarjetas usan `noopener noreferrer`.

## Imagen

`assets/img/portfolio/spotify-viaje-nocturno.jpg`: JPEG de 1672 × 941, generado con la herramienta integrada imagegen y exportado a JPEG. El archivo original mencionado en la conversación no estaba disponible; esta es una nueva interpretación, no una recuperación del original.

Prompt: “Use case: photorealistic-natural. Create a landscape cinematic photograph for Joaco Avia's music project portfolio card. Night flight inside an airplane: close view of black over-ear headphones and a portable music player resting on the tray beside an oval aircraft window; through window see airplane wing and distant city lights at night. Moody deep charcoal blacks and rich dark red cabin illumination, subtle crimson reflections, realistic textures, polished editorial travel photography. Clear central subject legible at small card size with a wide crop. No text, no typography, no logos, no watermark. Landscape 16:9.”

## Validación local

Con un servidor estático y Chrome/Playwright, a 1440 y 390 píxeles:
- Todos: tres tarjetas; YouTube: dos; Spotify: una.
- Alternancia repetida entre filtros, reinicio al primer slide y ausencia de desbordamiento horizontal.
- Enlace exacto al artista, imagen cargada y cero errores JavaScript.
- Revisión visual de capturas en escritorio y móvil.
- `node --check assets/js/main.js` y `git diff --check` correctos.

Para repetir manualmente: servir el repositorio con `python3 -m http.server 8765`, abrir la página y alternar Todos → Spotify → YouTube → Todos en escritorio y móvil. En móvil, deslizar hasta la tercera tarjeta.

No se requiere compilación: el repositorio es HTML/CSS/JavaScript estático. La validación fue local; no implica despliegue en producción.
