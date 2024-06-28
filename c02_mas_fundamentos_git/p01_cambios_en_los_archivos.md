# Cambios en los archivos

### Comandos y Explicaciones

#### Inicialización y Primer Commit

1. **Inicializar un nuevo repositorio de Git**:
   ```sh
   git init
   ```
   - **Propósito:** Inicializa un nuevo repositorio de Git en el directorio actual.
   - **Efecto:** Crea una carpeta `.git` en el directorio actual.

2. **Añadir todos los archivos al área de preparación**:
   ```sh
   git add .
   ```
   - **Propósito:** Añade todos los archivos en el directorio actual y sus subdirectorios al área de preparación.
   - **Efecto:** Todos los archivos están listos para ser confirmados en el próximo commit.

3. **Crear un commit inicial**:
   ```sh
   git commit -m "Instalaciones.md agregado"
   ```
   - **Propósito:** Crea un commit con los archivos añadidos al área de preparación.
   - **Efecto:** Guarda una versión del proyecto con el mensaje "Instalaciones.md agregado".

#### Ver el Historial de Commits y Diferencias

4. **Ver el historial de commits**:
   ```sh
   git log
   ```
   - **Propósito:** Muestra el historial de commits en el repositorio.
   - **Efecto:** Proporciona información sobre los commits realizados, incluyendo el hash, autor, fecha y mensaje de cada commit.

5. **Ver diferencias entre el directorio de trabajo y el índice** (dos veces):
   ```sh
   git diff
   git diff
   ```
   - **Propósito:** Muestra las diferencias entre el archivo `instalaciones.md` en el directorio de trabajo y la última versión en el índice o el último commit.
   - **Efecto:** Muestra cualquier cambio no confirmado.

#### Añadir Cambios y Verificar Estado

6. **Añadir todos los cambios al área de preparación**:
   ```sh
   git add .
   ```
   - **Propósito:** Añade todos los archivos modificados y nuevos al área de preparación.
   - **Efecto:** Todos los cambios están listos para ser confirmados en el próximo commit.

7. **Ver diferencias entre el directorio de trabajo y el índice nuevamente**:
   ```sh
   git diff
   ```
   - **Propósito:** Muestra las diferencias entre los archivos en el directorio de trabajo y la última versión en el índice o el último commit.
   - **Efecto:** Proporciona una vista de los cambios no confirmados.

8. **Ver el estado del repositorio**:
   ```sh
   git status
   ```
   - **Propósito:** Muestra el estado actual del repositorio.
   - **Efecto:** Indica qué archivos han sido modificados, añadidos, eliminados y cuáles están en el área de preparación.

9. **Ver diferencias entre el índice (staging area) y el último commit**:
   ```sh
   git diff --staged
   ```
   - **Propósito:** Muestra las diferencias entre los archivos en el área de preparación y la última versión confirmada.
   - **Efecto:** Proporciona una vista de los cambios que están a punto de ser confirmados.

#### Crear un Segundo Commit y Revertir Cambios

10. **Crear un commit con los cambios en el área de preparación**:
    ```sh
    git commit -m "Instalaciones actualizadas"
    ```
    - **Propósito:** Crea un commit con los cambios añadidos al área de preparación.
    - **Efecto:** Guarda una nueva versión del proyecto con el mensaje "Instalaciones actualizadas".

11. **Ver diferencias después del segundo commit** (dos veces):
    ```sh
    git diff
    git diff
    ```
    - **Propósito:** Muestra las diferencias entre el directorio de trabajo y el índice después del commit.
    - **Efecto:** Confirma que no hay cambios adicionales no confirmados.

12. **Revertir todos los cambios no confirmados en el directorio de trabajo**:
    ```sh
    git checkout -- .
    ```
    - **Propósito:** Revertir todos los cambios no confirmados en el directorio de trabajo.
    - **Efecto:** Restaura todos los archivos a su estado en el último commit confirmado.

### Flujo Completo de Comandos

```sh
# Inicializar un nuevo repositorio de Git
git init

# Añadir todos los archivos al área de preparación
git add .

# Crear un commit inicial
git commit -m "Instalaciones.md agregado"

# Ver el historial de commits
git log

# Ver diferencias entre el directorio de trabajo y el índice (dos veces)
git diff
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

# Ver diferencias entre el directorio de trabajo y el índice después del commit (dos veces)
git diff
git diff

# Revertir todos los cambios no confirmados en el directorio de trabajo
git checkout -- .
```

### Conclusión

Estos comandos te permiten inicializar un repositorio, añadir archivos, crear commits, comparar cambios, y revertir cambios no deseados. Usar estos comandos te ayudará a gestionar tu proyecto de manera eficiente, manteniendo un historial claro y conciso de todas las modificaciones realizadas.