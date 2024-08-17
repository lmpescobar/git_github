# Feature Branch - Revisando el Trabajo de Otros Compañeros

### Revisar y Manejar Ramas de Otros Compañeros

1. **Crear y Cambiar a una Nueva Rama:**
   - **Crear una nueva rama** en el repositorio remoto usando la interfaz de GitHub (o tu plataforma de Git). Por ejemplo, puedes crear una rama llamada `rama-misiones`.
   - **Cambiar a la nueva rama** y agregar un archivo con el contenido relevante. Luego, realiza un commit y un push de los cambios para actualizar la rama en el repositorio remoto.

2. **Trabajar con el Repositorio Local:**
   - **Hacer un pull** para traer los cambios del repositorio remoto a tu repositorio local:
     ```bash
     git pull
     ```
   - Si la nueva rama no aparece automáticamente en tu repositorio local después del pull, usa el comando:
     ```bash
     git fetch --all
     ```
   - Para ver todas las ramas remotas disponibles, usa:
     ```bash
     git branch -r
     ```
   - Para cambiar a una rama remota y crear una copia local, usa:
     ```bash
     git checkout -b rama-misiones origin/rama-misiones
     ```

3. **Revisar y Modificar el Trabajo de Otros:**
   - Una vez en la rama `rama-misiones`, puedes revisar el código y hacer cambios adicionales según sea necesario.
   - Realiza un commit y un push de tus modificaciones para actualizar la rama remota con los nuevos cambios:
     ```bash
     git commit -am "Descripción de los cambios realizados"
     git push
     ```

4. **Crear un Pull Request:**
   - Para integrar los cambios en la rama principal (`main`), crea un pull request en la plataforma de Git (por ejemplo, GitHub).
   - Inicia el pull request desde la rama `rama-misiones` hacia la rama `main`.
   - Revisa los cambios en el pull request, agrega comentarios si es necesario, y completa el proceso de pull request para fusionar los cambios.

5. **Eliminar Ramas que ya No se Necesitan:**
   - Después de fusionar los cambios, puedes eliminar la rama tanto en el repositorio remoto como local:
     - **Eliminar la rama remota:**
       ```bash
       git push origin --delete rama-misiones
       ```
     - **Eliminar la rama local:**
       ```bash
       git branch -d rama-misiones
       ```

6. **Limpiar Ramas Locales Obsoletas:**
   - Para ver todas las ramas locales, incluyendo las que han sido eliminadas remotamente:
     ```bash
     git branch -a
     ```
   - Para limpiar ramas locales obsoletas (aquellas que ya no están en el repositorio remoto):
     ```bash
     git fetch -p
     ```

### Conceptos Clave

- **Rama Remota:** Una rama que existe en el repositorio remoto (e.g., GitHub).
- **Rama Local:** Una copia de la rama remota que resides en tu máquina local.
- **Pull Request:** Un mecanismo para solicitar la revisión e integración de cambios en la rama principal (`main` o `master`).