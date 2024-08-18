# Tarea: Preparar un Nuevo Repositorio en GitHub

Para reforzar lo aprendido sobre el manejo de repositorios en Git, realiza los siguientes pasos:

#### 1. **Descargar el Repositorio Original**

- Accede al material adjunto del repositorio que se te ha proporcionado.
- Descarga el repositorio como un archivo comprimido (ZIP).
- Descomprime el archivo en tu computadora.

#### 2. **Preparar el Repositorio Local**

- Mueve la carpeta descomprimida a tu directorio de trabajo, por ejemplo, `CursodeGit`.
- Renombra la carpeta a `11_Avenger` (si la parte de "master" está presente en el nombre, quítala).

#### 3. **Configurar el Repositorio Local en Git**

1. **Abre Visual Studio Code:**
   - Arrastra la carpeta `11_Avenger` dentro de Visual Studio Code o abre la carpeta desde el menú de VS Code.

2. **Inicializa el Repositorio Local:**
   - Abre una terminal en Visual Studio Code (o utiliza la línea de comandos) y navega a la carpeta del repositorio.
   - Ejecuta el comando para inicializar un nuevo repositorio Git:
     ```bash
     git init
     ```

3. **Crear un Archivo `.gitignore`:**
   - En el directorio del proyecto, crea un archivo llamado `.gitignore`.
   - Añade las reglas necesarias para ignorar archivos no deseados, como archivos temporales, configuraciones de IDE, etc. Por ejemplo:
     ```
     node_modules/
     .env
     *.log
     ```

4. **Agregar Archivos y Hacer el Primer Commit:**
   - Agrega todos los archivos al repositorio:
     ```bash
     git add .
     ```
   - Realiza el primer commit:
     ```bash
     git commit -m "Primer commit con archivos iniciales"
     ```

#### 4. **Crear un Nuevo Repositorio en GitHub**

1. **Accede a tu Cuenta de GitHub:**
   - Inicia sesión en GitHub.

2. **Crear un Nuevo Repositorio:**
   - Ve a la sección de repositorios y haz clic en "New" para crear un nuevo repositorio.
   - Asigna un nombre único, por ejemplo, `Avengers_Curso` o `Ejercicio_12`.
   - Configura el repositorio como público o privado según tu preferencia.

#### 5. **Subir el Repositorio Local a GitHub**

1. **Agregar el Repositorio Remoto:**
   - En tu terminal, añade la URL del nuevo repositorio de GitHub como remoto:
     ```bash
     git remote add origin https://github.com/tu_usuario/nuevo_repositorio.git
     ```

2. **Empujar los Cambios al Repositorio Remoto:**
   - Sube los cambios al repositorio remoto:
     ```bash
     git push -u origin master
     ```

#### 6. **Verificación y Continuación**

- Verifica en GitHub que el repositorio ha sido creado correctamente y que todos los archivos están presentes.
- Puedes continuar con el siguiente video para ver la solución y comparar con el procedimiento realizado.