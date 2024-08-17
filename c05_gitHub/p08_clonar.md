# Clonar un repositorio

### **Clonar un Repositorio**

**Paso 1: Clonar el Repositorio**

1. **Ejecuta el comando `git clone`:**

   ```bash
   git clone https://github.com/KlerithX2/ligajusticia.git
   ```

   - **Descripción:** Este comando crea una copia local exacta del repositorio remoto en la ubicación donde ejecutas el comando. Git descargará todo el historial de commits, ramas, y archivos del repositorio remoto a tu máquina.

   - **Resultado:** Después de ejecutar este comando, tendrás una carpeta llamada `ligajusticia` (o el nombre del repositorio) en tu directorio actual. Esta carpeta contendrá todos los archivos y el historial de Git.

**Paso 2: Navegar al Directorio del Proyecto**

1. **Cambia al directorio del repositorio clonado:**

   ```bash
   cd ligajusticia
   ```

   - **Descripción:** Esto te mueve al directorio del repositorio recién clonado para que puedas empezar a trabajar con los archivos y comandos de Git dentro de ese proyecto.

**Paso 3: Verificar el Historial de Commits**

1. **Revisa el historial de commits:**

   ```bash
   git log
   ```

   - **Descripción:** Este comando te mostrará una lista de todos los commits realizados en el proyecto, desde el más reciente hasta el más antiguo. Cada commit incluye detalles como el autor, la fecha y un mensaje descriptivo.

   - **Opciones:** Puedes presionar `q` para salir del log y volver a la línea de comandos.

### **Resumen de Comandos**

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/KlerithX2/ligajusticia.git
   ```

2. **Moverse al directorio clonado:**
   ```bash
   cd ligajusticia
   ```

3. **Revisar el historial de commits:**
   ```bash
   git log
   ```

### **Consideraciones**

- **Clonación Completa:** Al clonar el repositorio, también se traen todas las ramas remotas, aunque solo la rama `main` o `master` estará activa en tu repositorio local por defecto.
- **Rendimiento:** Si el repositorio es grande, la clonación puede tardar un poco, ya que Git descargará todo el historial.
- **Privacidad:** Si el repositorio es privado, necesitarás autenticación para clonar el repositorio (usando un token de acceso personal o SSH).