# Kaizo IronMON para iPhone — paquete inicial

## Qué incluye
- `index.html`: interfaz en español, lanzador de EmulatorJS, panel de progreso, historial y lista de reglas.
- `manifest.webmanifest`, `icon.svg`, `sw.js`: metadatos de instalación y caché básica de la interfaz.

## Limitaciones importantes
- No incluye una ROM ni un juego comercial.
- El emulador se carga desde el CDN de EmulatorJS, así que se necesita conexión a Internet para cargarlo. La caché de esta versión no hace que el motor del emulador esté disponible offline.
- El cargador está preparado como prototipo. La carga de archivos locales mediante URL temporal debe probarse en el iPhone; si la versión de EmulatorJS/CDN no admite el flujo en tu dispositivo, se puede ajustar para alojar el runtime localmente.
- El guardado de progreso del panel usa almacenamiento local del navegador. Los guardados del juego dependen del emulador, de Safari y de la configuración de almacenamiento.
- La app no aleatoriza la ROM ni fuerza las reglas Kaizo IronMON. Debes usar una ROM preparada por ti con una herramienta/configuración compatible con las reglas elegidas.
- Para que el service worker y la instalación funcionen de forma fiable, publica los archivos en un sitio HTTPS. Abrir `index.html` directamente desde Archivos no es suficiente para instalarla como PWA.

## Cómo publicarla
1. Descomprime la carpeta.
2. Sube todos los archivos a un alojamiento web HTTPS estático (por ejemplo, GitHub Pages).
3. Abre la URL publicada en Safari.
4. Pulsa Compartir → Añadir a pantalla de inicio.

## Uso
1. Abre la web y selecciona tu archivo `.gba` o `.zip`.
2. Pulsa `Cargar juego`.
3. Para guardar notas, entra en `Mi intento`.
4. Exporta periódicamente el registro JSON para conservar una copia.

## Referencias
- EmulatorJS: https://emulatorjs.org/docs/
- Cómo añadir una web a la pantalla de inicio en iPhone: https://support.apple.com/guide/iphone/open-as-web-app-iphea86e5236/ios
