# GitHub Pages - Para tu proyecto o repositorio

GitHub Pages también permite crear sitios web específicos para proyectos individuales o repositorios. Este tipo de sitio es ideal para documentar un proyecto, crear una página de aterrizaje para una aplicación o proporcionar información adicional sobre el código.

### 1. **Crear o Usar un Repositorio Existente**
Si ya tienes un proyecto en GitHub y deseas crear una página web para documentarlo o mostrarlo, puedes usar el repositorio existente. Si no, crea uno nuevo.

### 2. **Crear la Página del Proyecto**
Dentro del repositorio, puedes usar la rama `main` o una rama específica (por ejemplo, `gh-pages`) para almacenar el contenido de tu sitio web.

- **Estructura básica**:
  - **index.html**: Este es el archivo principal que servirá como página de inicio.
  - **CSS/JS**: Si necesitas estilos o scripts adicionales, crea carpetas para `css`, `js`, e imágenes.

### 3. **Agregar Contenido al Repositorio**
Agrega los archivos que deseas publicar en el sitio web, como `index.html`, hojas de estilo, scripts, imágenes, etc.

### 4. **Configurar GitHub Pages**
1. **Acceder a la Configuración del Repositorio**:
   - Ve al repositorio en GitHub.
   - Haz clic en la pestaña **Settings** (Configuración).
  
2. **Configurar la Fuente de GitHub Pages**:
   - En la sección **Pages** (GitHub Pages), selecciona la rama que deseas usar para GitHub Pages.
   - Puedes elegir la rama `main` o `gh-pages`, y seleccionar la carpeta desde donde quieres que se sirvan los archivos (por ejemplo, `/root` para la raíz del repositorio o `/docs` si los archivos están en una carpeta específica).
   - Guarda los cambios.

### 5. **Publicar el Sitio Web**
Después de configurar GitHub Pages, el sitio web se publicará automáticamente en la URL:
- **Para repositorios de usuario u organización**: `https://[tu-usuario].github.io/[nombre-repositorio]`
- **Para repositorios en organizaciones**: `https://[nombre-organización].github.io/[nombre-repositorio]`

### 6. **Personalización y Mantenimiento**
- **Actualizaciones**: Cada vez que hagas cambios en la rama configurada y los subas a GitHub, el sitio web se actualizará automáticamente.
- **Personalización**: Puedes personalizar el sitio con CSS, agregar páginas adicionales o integrar frameworks como Bootstrap.
- **Markdown**: Si no deseas escribir HTML, puedes utilizar archivos Markdown (`.md`), que GitHub Pages convertirá automáticamente a HTML.

### Ejemplo de Configuración Básica
1. **Crear un archivo `index.html`** en la raíz del repositorio:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>My Project</title>
   </head>
   <body>
       <h1>Welcome to My Project</h1>
       <p>This is the documentation for my amazing project!</p>
   </body>
   </html>
   ```
2. **Hacer commit y push de los cambios**:
   ```bash
   git add .
   git commit -m "Add initial GitHub Pages site"
   git push origin main
   ```

### Consejos Adicionales
- **Usar Jekyll**: Si quieres un sitio más dinámico, puedes configurar Jekyll para generar automáticamente páginas a partir de archivos Markdown, lo que facilita la creación de documentación.
- **Integración con CI/CD**: Puedes usar GitHub Actions para automatizar el despliegue de tu sitio web cada vez que se haga un commit en una rama específica.
- **Custom Domain**: Puedes configurar un dominio personalizado si quieres que tu sitio web del proyecto tenga su propio dominio.

### Uso Común
- **Documentación**: Muchas veces, los desarrolladores usan GitHub Pages para crear una documentación detallada para sus proyectos open-source.
- **Páginas de Proyecto**: Crear una página de aterrizaje para presentar un proyecto o aplicación de manera visual y atractiva.