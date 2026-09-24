# Unificador de PDFs

Herramienta web para combinar varios archivos PDF en un único documento.

## Características

- Selección múltiple de archivos PDF.
- Arrastrar y soltar.
- Reordenamiento de archivos.
- Eliminación individual.
- Detección de PDFs protegidos/cifrados.
- Renderizado mediante PDF.js para PDFs protegidos.
- Procesamiento local en el navegador.
- No requiere servidor backend.

## Publicar en GitHub Pages

1. Cree un repositorio en GitHub.
2. Suba `index.html` a la rama `main`.
3. En el repositorio vaya a **Settings → Pages**.
4. En **Build and deployment**, seleccione:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Guarde los cambios.

GitHub Pages publicará la aplicación usando `index.html` como página principal.

## Dependencias

La versión actual carga `pdf-lib` y `PDF.js` desde CDN:

- pdf-lib 1.17.1
- PDF.js 4.10.38

Por ello, no se requiere un proceso de compilación ni Node.js.

## Privacidad

Los archivos seleccionados se procesan en el navegador. La aplicación no implementa una subida de archivos a un servidor.

## Limitación de PDFs protegidos

Los PDFs cifrados/protegidos que no pueden ser procesados directamente por pdf-lib se renderizan mediante PDF.js como imágenes. Esto puede aumentar el tamaño del documento y convertir el contenido de esas páginas en contenido gráfico.
