# Portafolio — CNO IV Seguridad Informática

Mi portafolio, primer parcial (apartado Inicio). Sitio estático hecho con HTML, CSS y JS.

## Archivos
- `index.html`, `styles.css`, `script.js` — el sitio
- `worker.js` — proxy que reenvía el formulario a mi Telegram sin exponer el token
- Autorespuesta al visitante vía EmailJS

## Publicación
Lo subo a un repo en GitHub y activo Pages (Settings → Pages → Deploy from branch → main). GitHub emite el HTTPS solo; nada más confirmo "Enforce HTTPS". La URL que entrego es la que da esa pantalla.

## Formulario de contacto
- El aviso a mí no sale directo del navegador (el token del bot quedaría expuesto en el código público). Pasa por un Worker de Cloudflare que guarda el token como secreto y reenvía a Telegram.
- La autorespuesta al visitante sí corre en el navegador, con EmailJS (su Public Key está pensada para ser pública).
- Las claves de ambos van en `script.js`; mientras no las ponga, esa parte se desactiva sola sin tronar el resto.

## Pendiente antes de entregar
- Poner mi correo y links reales en el footer.
- Configurar el Worker (token + chat_id) y EmailJS.
- Probar en móvil y confirmar el candado 🔒 en la URL final.
