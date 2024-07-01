# Actualizar mensaje del commit y revertir commits

### Actualización de Mensaje de Commit y Reversión de Commits

#### Crear un Commit y Ver el Historial

1. **Crear un commit con cambios y un mensaje inicial**:
   ```sh
   git commit -am "Instalaciones actualiz"
   ```
   - **Propósito:** Crear un commit con todos los cambios rastreados y añadir un mensaje.
   - **Efecto:** Guarda una nueva versión del proyecto con el mensaje "Instalaciones actualiz".

2. **Ver el historial de commits**:
   ```sh
   git log
   ```
   - **Propósito:** Ver el historial de commits en el repositorio.
   - **Efecto:** Muestra todos los commits realizados, incluyendo el commit recién creado.

#### Actualizar el Mensaje del Commit

3. **Actualizar el mensaje del commit más reciente**:
   ```sh
   git commit --amend -m "Instalaciones actualizadas"
   ```
   - **Propósito:** Modificar el mensaje del commit más reciente.
   - **Efecto:** Cambia el mensaje del commit anterior a "Instalaciones actualizadas".

4. **Verificar el historial de commits**:
   ```sh
   git log
   ```
   - **Propósito:** Verificar que el mensaje del commit se haya actualizado.
   - **Efecto:** Muestra el historial con el commit actualizado.

5. **Actualizar el mensaje del commit más reciente nuevamente**:
   ```sh
   git commit --amend -m "Notas añadidas a las instalaciones"
   ```
   - **Propósito:** Modificar nuevamente el mensaje del commit más reciente.
   - **Efecto:** Cambia el mensaje del commit anterior a "Notas añadidas a las instalaciones".

6. **Verificar el historial de commits**:
   ```sh
   git log
   ```
   - **Propósito:** Verificar que el mensaje del commit se haya actualizado nuevamente.
   - **Efecto:** Muestra el historial con el commit actualizado.

#### Revertir un Commit

7. **Revertir el commit más reciente, manteniendo los cambios en el área de preparación**:
   ```sh
   git reset --soft HEAD^
   ```
   - **Propósito:** Revertir el commit más reciente pero mantener los cambios en el área de preparación.
   - **Efecto:** El commit se deshace, pero los cambios quedan listos para un nuevo commit.

8. **Verificar el estado del repositorio**:
   ```sh
   git status
   ```
   - **Propósito:** Ver el estado del repositorio después del reset.
   - **Efecto:** Muestra que los cambios están en el área de preparación.

9. **Verificar el historial de commits**:
   ```sh
   git log
   ```
   - **Propósito:** Verificar que el commit ha sido revertido.
   - **Efecto:** El commit más reciente no aparece en el historial.

#### Rehacer el Commit con un Nuevo Mensaje

10. **Añadir todos los cambios al área de preparación nuevamente**:
    ```sh
    git add .
    ```
    - **Propósito:** Añadir todos los cambios al área de preparación.
    - **Efecto:** Los cambios están listos para ser confirmados en un nuevo commit.

11. **Crear un nuevo commit con los cambios y un mensaje diferente**:
    ```sh
    git commit -m "Notas añadidas de nuevo a las instalaciones"
    ```
    - **Propósito:** Crear un nuevo commit con los cambios y un nuevo mensaje.
    - **Efecto:** Guarda una nueva versión del proyecto con el mensaje "Notas añadidas de nuevo a las instalaciones".

12. **Verificar el historial de commits**:
    ```sh
    git log
    ```
    - **Propósito:** Verificar el historial de commits después de crear el nuevo commit.
    - **Efecto:** Muestra el historial con el nuevo commit.

### Flujo Completo de Comandos

```sh
# Crear un commit con un mensaje inicial
git commit -am "Instalaciones actualiz"

# Ver el historial de commits
git log

# Actualizar el mensaje del commit más reciente
git commit --amend -m "Instalaciones actualizadas"

# Verificar el historial de commits
git log

# Actualizar el mensaje del commit más reciente nuevamente
git commit --amend -m "Notas añadidas a las instalaciones"

# Verificar el historial de commits
git log

# Revertir el commit más reciente, manteniendo los cambios en el área de preparación
git reset --soft HEAD^

# Verificar el estado del repositorio
git status

# Verificar el historial de commits
git log

# Añadir todos los cambios al área de preparación nuevamente
git add .

# Crear un nuevo commit con los cambios y un nuevo mensaje
git commit -m "Notas añadidas de nuevo a las instalaciones"

# Verificar el historial de commits
git log
```

### Conclusión

Estos comandos permiten modificar el mensaje de un commit, revertir un commit reciente y rehacer el commit con un nuevo mensaje. Este flujo es útil para corregir errores en los mensajes de commit o ajustar los cambios antes de confirmarlos definitivamente.