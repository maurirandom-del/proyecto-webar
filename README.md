# Proyecto WebAR con MindAR.js

Proyecto mínimo de realidad aumentada web: la cámara reconoce una imagen objetivo y muestra un modelo 3D sobre ella. Está hecho con HTML, A-Frame y MindAR.js; no necesita instalar Node.js.

## Archivos

- `index.html`: página principal.
- La imagen objetivo `.mind` y el modelo 3D de demostración se cargan desde el CDN público de MindAR. Para esta primera prueba no hace falta crear esos archivos manualmente.

## Probarlo en el celular usando GitHub Pages

1. Descarga y descomprime este proyecto.
2. En GitHub, crea un repositorio nuevo **público**, por ejemplo `proyecto-webar`.
3. Sube `index.html` y `README.md` a la raíz del repositorio (no subas únicamente la carpeta contenedora).
4. En el repositorio, entra a **Settings → Pages**.
5. En **Build and deployment**, selecciona **Deploy from a branch**.
6. Elige la rama `main` y la carpeta `/(root)`, y guarda.
7. Espera unos minutos. GitHub mostrará la URL publicada en esa misma sección, normalmente:
   `https://TU-USUARIO.github.io/proyecto-webar/`
8. Abre esa URL desde el celular y acepta el permiso de cámara. Usa Safari en iPhone o Chrome en Android, preferentemente actualizado.

## Imagen que debes mostrar a la cámara

Imprime o abre en otra pantalla la imagen de prueba oficial de MindAR:
https://cdn.jsdelivr.net/gh/hiukim/mind-ar-js@1.2.5/examples/image-tracking/assets/card-example/card.png

En la página WebAR, apunta la cámara a esa imagen. El modelo debería aparecer cuando la imagen sea detectada. Puedes probar primero con la imagen mostrada en una laptop o monitor.

## Si quieres usar tu propia imagen objetivo

1. Abre el compilador oficial: https://hiukim.github.io/mind-ar-js-doc/tools/compile/
2. Carga una imagen con detalles visuales bien distribuidos (evita imágenes casi lisas, repetitivas o con grandes zonas vacías).
3. Pulsa **Start** y después descarga el archivo `.mind`.
4. Sube el archivo, por ejemplo `assets/mi-target.mind`, al repositorio.
5. En `index.html`, cambia el valor `imageTargetSrc` para que apunte al archivo, por ejemplo:
   `imageTargetSrc: ./assets/mi-target.mind;`
6. Para que la experiencia use tu imagen, reemplaza también la URL de la tarjeta de demostración si decides mostrarla en la página.

## Si no funciona

- **No aparece el permiso de cámara:** confirma que abriste la URL `https://...github.io/...`, no una vista previa local ni un archivo `file://`.
- **Pantalla negra:** acepta el permiso, cierra otras aplicaciones que usen la cámara y vuelve a cargar la página.
- **No detecta la imagen:** usa la imagen exacta de prueba, con buena luz y sin reflejos; mantén la tarjeta completa dentro del encuadre.
- **El modelo no carga:** revisa tu conexión; el modelo de ejemplo y las bibliotecas se descargan de CDNs externos.
- **Primera carga lenta:** espera unos segundos; la primera carga descarga bibliotecas y recursos 3D.

## Tecnologías y referencias

- MindAR.js: https://github.com/hiukim/mind-ar-js
- Documentación de inicio rápido: https://hiukim.github.io/mind-ar-js-doc/quick-start/overview/
- GitHub Pages: https://docs.github.com/en/pages/quickstart

Este proyecto es una base didáctica. Requiere conexión a internet para descargar las bibliotecas y recursos de demostración.
