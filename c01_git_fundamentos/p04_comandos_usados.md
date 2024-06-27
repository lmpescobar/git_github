# Exposición sobre los comandos usados hasta el momento

### Exposición sobre los Comandos Usados hasta el Momento en Git

#### 1. `cd`
   - **Propósito:** Cambiar de directorio.
   - **Uso:** Navegar al directorio de trabajo donde se encuentra o se desea inicializar un repositorio de Git.
   - **Ejemplo:** 
     ```sh
     cd 01-BASES
     ```
     Esto cambia el directorio actual a `01-BASES`.

#### 2. `git init`
   - **Propósito:** Inicializar un nuevo repositorio de Git.
   - **Uso:** Crear un nuevo repositorio en el directorio actual.
   - **Ejemplo:**
     ```sh
     git init
     ```
     Esto crea una carpeta `.git` en el directorio actual, iniciando un nuevo repositorio.

#### 3. `git status`
   - **Propósito:** Ver el estado actual del repositorio.
   - **Uso:** Mostrar los archivos modificados, añadidos, eliminados y no rastreados.
   - **Ejemplo:**
     ```sh
     git status
     ```
     Esto muestra el estado actual de los archivos en el repositorio.

#### 4. `git add`
   - **Propósito:** Añadir archivos al área de preparación (staging area).
   - **Uso:** Preparar archivos específicos o todos los archivos modificados para el próximo commit.
   - **Ejemplos:**
     ```sh
     git add index.html
     ```
     Añade `index.html` al área de preparación.
     ```sh
     git add .
     ```
     Añade todos los archivos modificados en el directorio actual y sus subdirectorios al área de preparación.

#### 5. `git reset`
   - **Propósito:** Retirar archivos del área de preparación.
   - **Uso:** Deshacer el comando `git add` para archivos específicos.
   - **Ejemplo:**
     ```sh
     git reset .DS_Store
     ```
     Retira el archivo `.DS_Store` del área de preparación.

#### 6. `git commit`
   - **Propósito:** Crear un commit con los cambios en el área de preparación.
   - **Uso:** Guardar una versión del proyecto con un mensaje descriptivo.
   - **Ejemplo:**
     ```sh
     git commit -m "Primer commit"
     ```
     Crea un commit con el mensaje "Primer commit", incluyendo todos los cambios en el área de preparación.

#### 7. `git log`
   - **Propósito:** Ver el historial de commits.
   - **Uso:** Mostrar los commits realizados en el repositorio.
   - **Ejemplo:**
     ```sh
     git log
     ```
     Muestra el historial de commits, incluyendo el hash, autor, fecha y mensaje de cada commit.

#### 8. `git checkout -- .`
   - **Propósito:** Revertir todos los cambios no confirmados en el directorio actual y sus subdirectorios.
   - **Uso:** Restaurar archivos y directorios a su estado en el último commit confirmado.
   - **Ejemplo:**
     ```sh
     git checkout -- .
     ```
     Revierten todos los cambios no confirmados, restaurando los archivos y directorios al último commit.

### Ejemplo Práctico

#### Paso a Paso

1. **Navegar al Directorio de Trabajo:**
   ```sh
   cd 01-BASES
   ```
   Cambiamos al directorio `01-BASES`.

2. **Inicializar el Repositorio de Git:**
   ```sh
   git init
   ```
   Inicializamos un nuevo repositorio en `01-BASES`.

3. **Verificar el Estado Inicial:**
   ```sh
   git status
   ```
   Verificamos que no hay archivos rastreados aún.

4. **Añadir un Archivo al Área de Preparación:**
   ```sh
   git add index.html
   ```
   Añadimos `index.html` al área de preparación.

5. **Verificar el Estado Después de Añadir:**
   ```sh
   git status
   ```
   Verificamos que `index.html` está en el área de preparación.

6. **Añadir Todos los Archivos Modificados:**
   ```sh
   git add .
   ```
   Añadimos todos los archivos modificados al área de preparación.

7. **Verificar el Estado Después de Añadir Todos:**
   ```sh
   git status
   ```
   Verificamos que todos los archivos modificados están en el área de preparación.

8. **Retirar un Archivo del Área de Preparación:**
   ```sh
   git reset .DS_Store
   ```
   Retiramos `.DS_Store` del área de preparación.

9. **Verificar el Estado Después del Reset:**
   ```sh
   git status
   ```
   Verificamos que `.DS_Store` ya no está en el área de preparación.

10. **Añadir Todos los Archivos Modificados Nuevamente:**
    ```sh
    git add .
    ```
    Añadimos todos los archivos modificados al área de preparación.

11. **Crear un Commit:**
    ```sh
    git commit -m "Primer commit"
    ```
    Creamos un commit con el mensaje "Primer commit".

12. **Verificar el Estado Después del Commit:**
    ```sh
    git status
    ```
    Verificamos que no hay cambios pendientes en el área de preparación.

13. **Ver el Historial de Commits:**
    ```sh
    git log
    ```
    Vemos el historial de commits en el repositorio.

14. **Revertir Cambios No Confirmados:**
    ```sh
    git checkout -- .
    ```
    Revertimos todos los cambios no confirmados, restaurando el estado del último commit confirmado.

### Conclusión

Estos comandos de Git te permiten inicializar un repositorio, añadir archivos al área de preparación, confirmar cambios, verificar el estado del repositorio, revertir cambios no deseados y revisar el historial de commits. Git proporciona un control detallado sobre el estado de tu proyecto, facilitando la gestión de versiones y la colaboración con otros desarrolladores.