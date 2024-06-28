# Cambios en los archivos

### Imágenes

1. **Primera Imagen:**
   - Se ha creado y editado el archivo `instalaciones.md` en el directorio `03-INSTALACIONES/`.
   - Contenido del archivo: Instrucciones para instalar usando `yarn install`.

2. **Segunda Imagen:**
   - Muestra las diferencias entre el archivo `instalaciones.md` en el área de preparación y el directorio de trabajo.
   - Adicionalmente, se han añadido comandos `npm install` y `npm start`.

### Comandos Usados

#### Inicialización y Primer Commit

1. **Inicializar un nuevo repositorio de Git**:
   ```sh
   git init
   ```

2. **Crear un commit inicial (Esto parece que fue un error, ya que no se añadió el archivo antes del commit)**:
   ```sh
   git commit -m "Instalaciones.md agragado"
   ```
   Debería haberse usado `git add .` antes de este commit para añadir el archivo `instalaciones.md` al área de preparación.

3. **Ver el historial de commits**:
   ```sh
   git log
   ```

#### Comparar Cambios

4. **Ver diferencias entre el directorio de trabajo y el índice (staging area)**:
   ```sh
   git diff
   ```
   Esto muestra las diferencias entre el archivo `instalaciones.md` en el directorio de trabajo y la última versión en el índice o el último commit.

5. **Añadir todos los cambios al área de preparación**:
   ```sh
   git add .
   ```

6. **Ver diferencias entre el directorio de trabajo y el índice nuevamente**:
   ```sh
   git diff
   ```

7. **Ver el estado del repositorio**:
   ```sh
   git status
   ```

8. **Ver diferencias entre el índice (staging area) y el último commit**:
   ```sh
   git diff --staged
   ```

#### Crear un Commit con Cambios

9. **Crear un commit con los cambios en el área de preparación**:
   ```sh
   git commit -m "Instalaciones actualizadas"
   ```

#### Verificar y Revertir Cambios

10. **Ver diferencias entre el directorio de trabajo y el índice después del commit**:
    ```sh
    git diff
    ```

11. **Revertir todos los cambios no confirmados en el directorio de trabajo**:
    ```sh
    git checkout -- .
    ```

### Flujo Completo de Comandos

```sh
# Inicializar un nuevo repositorio de Git
git init

# Añadir archivos al área de preparación
git add .

# Crear un commit inicial
git commit -m "Instalaciones.md agregado"

# Ver el historial de commits
git log

# Ver diferencias entre el directorio de trabajo y el índice
git diff

# Añadir todos los cambios al área de preparación
git add .

# Ver diferencias entre el directorio de trabajo y el índice
git diff

# Ver el estado del repositorio
git status

# Ver diferencias entre el índice y el último commit
git diff --staged

# Crear un commit con los cambios en el área de preparación
git commit -m "Instalaciones actualizadas"

# Ver diferencias entre el directorio de trabajo y el índice después del commit
git diff

# Revertir todos los cambios no confirmados en el directorio de trabajo
git checkout -- .
```

### Explicación del Proceso

1. **Inicialización y Preparación**:
   - `git init` inicializa un nuevo repositorio.
   - `git add .` añade todos los archivos al área de preparación.
   - `git commit -m "Instalaciones.md agregado"` crea el commit inicial (asegúrate de añadir los archivos primero).

2. **Comparar y Añadir Cambios**:
   - `git diff` muestra diferencias no confirmadas.
   - `git add .` añade todos los cambios al área de preparación.
   - `git status` muestra el estado actual del repositorio.
   - `git diff --staged` muestra diferencias entre el índice y el último commit.

3. **Confirmar Cambios**:
   - `git commit -m "Instalaciones actualizadas"` crea un commit con los cambios preparados.

4. **Verificar y Revertir**:
   - `git diff` después del commit para ver si hay diferencias adicionales.
   - `git checkout -- .` para revertir todos los cambios no confirmados en el directorio de trabajo.

### Conclusión

Este flujo de trabajo cubre la inicialización del repositorio, la adición de archivos, la comparación de cambios, la preparación de commits y la reversión de cambios no deseados. Estos comandos y pasos son esenciales para gestionar eficazmente un proyecto con Git, permitiendo un control preciso sobre el estado y la evolución del repositorio.