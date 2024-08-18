# GitHub Pages - Para tu usuario u Organización

GitHub Pages es una función de GitHub que permite alojar sitios web estáticos directamente desde un repositorio de GitHub. Es una excelente opción para crear un portafolio personal, documentación de proyectos, blogs, o incluso la página web de una organización.

### 1. **Crear un Repositorio**
- **Para tu usuario**: Si deseas crear un sitio web que represente tu perfil de GitHub, el repositorio debe tener el nombre `[tu-usuario].github.io`. Por ejemplo, si tu nombre de usuario es `johndoe`, el repositorio debe llamarse `johndoe.github.io`.
- **Para tu organización**: Si estás creando un sitio web para una organización, el repositorio debe llamarse `[nombre-organización].github.io`.

### 2. **Clonar el Repositorio (Opcional)**
Si prefieres trabajar localmente antes de subir los archivos, clona el repositorio a tu máquina:
```bash
git clone https://github.com/[tu-usuario]/[tu-usuario].github.io
```

### 3. **Agregar Contenido**
- **Index.html**: Crea un archivo `index.html` como el archivo principal del sitio web. Este archivo se cargará cuando alguien visite tu sitio web.
- **CSS y JavaScript**: Puedes agregar hojas de estilo CSS y scripts de JavaScript en la estructura de tu sitio web para personalizar su apariencia y funcionalidad.

### 4. **Publicar tu Sitio Web**
1. **Agregar y hacer commit de los cambios**:
   ```bash
   git add .
   git commit -m "Initial commit"
   ```

2. **Subir los cambios a GitHub**:
   ```bash
   git push origin main
   ```

### 5. **Configurar GitHub Pages**
- GitHub automáticamente detectará si tienes un repositorio llamado `[tu-usuario].github.io` o `[nombre-organización].github.io` y publicará el sitio web en la URL `https://[tu-usuario].github.io` o `https://[nombre-organización].github.io`.
- Si usas otra rama que no sea `main` o si quieres personalizar la configuración, ve a **Settings > Pages** dentro del repositorio y selecciona la rama y carpeta desde la cual deseas servir el contenido.

### 6. **Customizar tu Dominio (Opcional)**
Si deseas usar un dominio personalizado (por ejemplo, `www.tusitio.com`), puedes configurarlo:
1. Ve a **Settings > Pages** en tu repositorio.
2. En la sección "Custom domain", ingresa tu dominio personalizado.
3. Configura los registros DNS de tu dominio para que apunten a GitHub Pages.

### 7. **Ver y Mantener tu Sitio Web**
- Puedes acceder a tu sitio web en `https://[tu-usuario].github.io` o `https://[nombre-organización].github.io`.
- Cada vez que realices cambios en el repositorio y los subas, GitHub Pages actualizará automáticamente el sitio.

### Ejemplos de Uso
- **Portafolio Personal**: Muestra tus proyectos, habilidades, y experiencia.
- **Documentación de Proyectos**: Publica la documentación de tus proyectos de código abierto.
- **Blog**: Puedes usar generadores de sitios estáticos como Jekyll, que GitHub Pages soporta de forma nativa, para crear un blog.

### Consejos
- **Jekyll**: Si quieres crear un blog o un sitio más dinámico, considera aprender Jekyll, que es compatible con GitHub Pages y facilita la gestión de contenido.
- **Markdown**: Puedes escribir tu contenido en Markdown, que GitHub Pages convierte automáticamente a HTML.
- **Temas y Plantillas**: GitHub Pages ofrece temas que puedes utilizar para darle un diseño atractivo a tu sitio sin mucho esfuerzo.