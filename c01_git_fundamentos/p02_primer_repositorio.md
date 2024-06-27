# Nuestro primer repositorio

### Secuencia de Comandos

1. **Navegar a la carpeta de trabajo**:
   ```sh
   cd
   ```
   El comando `cd` por sí solo te llevará a tu directorio de inicio. Generalmente, querrás navegar a la carpeta específica de tu proyecto.

2. **Inicializar un repositorio de Git**:
   ```sh
   git init
   ```
   Este comando inicializa un nuevo repositorio de Git en la carpeta actual.

3. **Ver el estado actual del repositorio**:
   ```sh
   git status
   ```
   Este comando muestra el estado de los archivos en el repositorio, indicándote cuáles han sido modificados, cuáles están en el área de preparación y cuáles no están siendo rastreados por Git.

4. **Añadir un archivo específico al área de preparación**:
   ```sh
   git add index.html
   ```
   Este comando añade el archivo `index.html` al área de preparación (staging area), preparándolo para ser incluido en el próximo commit.

5. **Ver el estado del repositorio nuevamente**:
   ```sh
   git status
   ```
   Este comando te mostrará que `index.html` ha sido añadido al área de preparación.

6. **Añadir todos los archivos modificados al área de preparación**:
   ```sh
   git add .
   ```
   Este comando añade todos los archivos modificados en el directorio actual y sus subdirectorios al área de preparación.

7. **Ver el estado del repositorio nuevamente**:
   ```sh
   git status
   ```
   Este comando te mostrará todos los archivos que están en el área de preparación, listos para ser comprometidos.

8. **Retirar un archivo específico del área de preparación**:
   ```sh
   git reset .DS_Store
   ```
   Este comando retira el archivo `.DS_Store` del área de preparación, deshaciéndose del `git add` previo para ese archivo en particular. `.DS_Store` es un archivo generado por macOS que no suele ser necesario en los repositorios de código.

9. **Ver el estado del repositorio nuevamente**:
   ```sh
   git status
   ```
   Este comando te mostrará que `.DS_Store` ha sido retirado del área de preparación.

10. **Añadir todos los archivos modificados al área de preparación nuevamente**:
    ```sh
    git add .
    ```
    Este comando asegura que todos los archivos deseados estén en el área de preparación.

11. **Hacer un commit de los cambios en el área de preparación**:
    ```sh
    git commit -m "Primer commit"
    ```
    Este comando crea un commit con los cambios en el área de preparación, con el mensaje "Primer commit".

12. **Ver el estado del repositorio nuevamente**:
    ```sh
    git status
    ```
    Este comando muestra que no hay cambios en el área de preparación ni en el directorio de trabajo.

13. **Ver el historial de commits**:
    ```sh
    git log
    ```
    Este comando muestra el historial de commits en el repositorio, incluyendo el hash del commit, el autor, la fecha y el mensaje del commit.

### Resumen de Comandos Usados

```sh
# Navegar al directorio de inicio (cambia a tu directorio de trabajo específico)
cd

# Inicializar un nuevo repositorio de Git
git init

# Ver el estado actual del repositorio
git status

# Añadir un archivo específico al área de preparación
git add index.html

# Ver el estado del repositorio nuevamente
git status

# Añadir todos los archivos modificados al área de preparación
git add .

# Ver el estado del repositorio nuevamente
git status

# Retirar un archivo específico del área de preparación
git reset .DS_Store

# Ver el estado del repositorio nuevamente
git status

# Añadir todos los archivos modificados al área de preparación nuevamente
git add .

# Hacer un commit con un mensaje descriptivo
git commit -m "Primer commit"

# Ver el estado del repositorio nuevamente
git status

# Ver el historial de commits
git log
```

Estos pasos te llevan a través del proceso de iniciar un nuevo repositorio de Git, añadir archivos, hacer commits y revisar el estado y el historial del repositorio.