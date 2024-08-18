# Labels - Etiquetas

Las **etiquetas (labels)** en GitHub son herramientas fundamentales para organizar y gestionar los issues de un repositorio. Te permiten clasificar y filtrar los issues de manera eficiente, facilitando su seguimiento y resolución.

### Cómo Configurar y Usar Etiquetas en GitHub

1. **Acceder a las Etiquetas:**
   - Ve a la página principal de tu repositorio en GitHub.
   - Haz clic en la pestaña **"Issues"** (Problemas).
   - Luego, haz clic en **"Labels"** (Etiquetas) para ver y gestionar las etiquetas existentes.

2. **Crear o Editar Etiquetas:**
   - Para **crear una nueva etiqueta**, haz clic en **"New label"** (Nueva etiqueta).
     - **Nombre:** Introduce el nombre de la etiqueta.
     - **Descripción:** Agrega una breve descripción sobre el propósito de la etiqueta.
     - **Color:** Puedes seleccionar un color predefinido o ingresar un código hexadecimal para personalizar el color de la etiqueta.
   - Para **editar una etiqueta existente**, haz clic en el nombre de la etiqueta y luego en **"Edit"** (Editar). Aquí puedes cambiar el nombre, la descripción y el color.

3. **Aplicar Etiquetas a Issues:**
   - Cuando creas o editas un issue, puedes seleccionar etiquetas en el panel derecho bajo **"Labels"** (Etiquetas). Esto te permite clasificar el issue según su tipo, estado, prioridad, etc.
   - También puedes **buscar y filtrar issues** usando etiquetas. Esto es útil para ver todos los issues con una etiqueta específica, como todos los errores (`bug`) o solicitudes de características (`feature request`).

4. **Usar Etiquetas en Plantillas de Issues:**
   - Puedes configurar plantillas de issues para que asignen automáticamente una etiqueta específica al crear un nuevo issue. Esto se hace desde la sección **"Issue templates"** en la configuración del repositorio.
   - Al editar una plantilla, encontrarás una sección para **"Labels"** donde puedes seleccionar etiquetas que se asignarán automáticamente a los issues creados con esa plantilla.

5. **Ejemplos de Etiquetas Comunes:**
   - **Bug:** Para problemas o errores en el código.
   - **Feature Request:** Para solicitudes de nuevas características.
   - **Documentation:** Para problemas o mejoras en la documentación.
   - **Duplicate:** Para marcar issues que ya han sido reportados.
   - **Help Wanted:** Para solicitar ayuda o colaboración en la resolución de un problema.

6. **Beneficios de Usar Etiquetas:**
   - **Organización:** Mantén tus issues organizados y fáciles de encontrar.
   - **Filtrado:** Filtra issues según etiquetas para una mejor gestión y revisión.
   - **Automatización:** Configura etiquetas predeterminadas para ahorrar tiempo y estandarizar el proceso de reporte.

### Ejemplo de Configuración de Etiquetas

1. **Crear una Etiqueta:**
   - **Nombre:** `bug`
   - **Descripción:** "Indica un problema o error en el código."
   - **Color:** `#e11d48` (Rojo)

2. **Aplicar Etiquetas a un Issue:**
   - Al crear un issue, selecciona la etiqueta `bug` para indicar que se trata de un error.

3. **Configurar Etiquetas en Plantillas:**
   - En una plantilla de reporte de errores, agrega la etiqueta `bug` para que todos los issues creados con esta plantilla se marquen automáticamente como errores.

### Cómo Revisar y Gestionar Issues por Etiquetas

1. **Buscar Issues por Etiquetas:**
   - En la pestaña **"Issues"**, usa la barra de búsqueda para encontrar issues con etiquetas específicas. Por ejemplo, `label:bug` mostrará todos los issues etiquetados como errores.

2. **Filtrar Issues:**
   - Usa los filtros disponibles para ver issues con una combinación de etiquetas, como `label:bug label:high-priority`.