# Sunshine Coffee · Café de Origen Colombiano

Bienvenido al repositorio de **Sunshine Coffee**, un proyecto web diseñado para una marca o cafetería conceptual, destacando el café de origen colombiano (Boyacá · Bosa).

## 📄 ¿De qué se compone este proyecto?

Este proyecto es una **Single-File Web App (Aplicación de un solo archivo)**. Toda la página web está contenida y empaquetada dentro de un único archivo: **`index.html`**.

### Características técnicas:
- **Todo en uno:** En lugar de tener carpetas separadas para CSS, JavaScript e imágenes, todo el contenido ha sido agrupado en un solo lugar.
- **Assets integrados:** Los recursos gráficos y multimedia (como imágenes) están codificados directamente en el archivo usando formato **Base64**. Al abrir la página, un pequeño script interno se encarga de "desempaquetar" estos recursos y cargarlos dinámicamente en el navegador.
- **Carga inicial:** Durante los milisegundos en que se extraen los archivos, la página muestra un SVG liviano como pantalla de carga (`Unpacking...`) para una experiencia de usuario fluida.

## 🚀 Despliegue en Vercel

Dado que se trata de un archivo estático puro llamado `index.html`, está completamente optimizado para ser desplegado de manera automática y gratuita en plataformas como **Vercel** o GitHub Pages. No requiere configuración adicional, build steps (pasos de compilación), ni un servidor de base de datos.
