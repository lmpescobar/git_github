# Git Stash

### **Comandos y Explicaciones**

1. **Ver el historial de commits**:
   ```bash
   git log
   ```
   - Esto muestra el historial de commits para que puedas ver en qué estado se encuentra tu repositorio antes de hacer cualquier cambio.

2. **Ver las ramas actuales**:
   ```bash
   git branch
   ```
   - Esto muestra la lista de ramas en tu repositorio y te indica en qué rama estás trabajando actualmente.

3. **Guardar cambios no confirmados en el stash**:
   ```bash
   git stash
   ```
   - Este comando guarda todos los cambios no confirmados (modificaciones y adiciones de archivos rastreados) en un stash, y restablece el área de trabajo al último commit. Esto te permite tener un espacio de trabajo limpio para realizar otras tareas sin perder tu trabajo en progreso.

4. **Ver el historial de commits nuevamente**:
   ```bash
   git log
   ```
   - Este comando verifica que el stash ha limpiado los cambios no confirmados de tu área de trabajo, por lo que el historial de commits permanece igual.

5. **Ver el estado del repositorio**:
   ```bash
   git status
   ```
   - Este comando muestra el estado actual del repositorio. Después de usar `git stash`, tu área de trabajo debe estar limpia, sin archivos modificados o agregados pendientes de commit.

6. **Listar todos los stashes guardados**:
   ```bash
   git stash list
   ```
   - Muestra todos los stashes que has creado. Cada stash se enumera con un identificador único, como `stash@{0}`.

7. **Hacer un commit**:
   ```bash
   git commit -am "Readme updated"
   ```
   - Este comando confirma todos los cambios en archivos rastreados y modifica el historial de commits. `-a` incluye todos los cambios en archivos rastreados, y `-m` proporciona un mensaje de commit.

8. **Ver el historial de commits nuevamente**:
   ```bash
   git log
   ```
   - Este comando verifica que el commit se ha realizado correctamente y se ha agregado al historial.

9. **Ver la lista de stashes nuevamente**:
   ```bash
   git stash list
   ```
   - Esto confirma que el stash todavía está guardado, incluso después de haber hecho un nuevo commit.

10. **Aplicar el stash más reciente y eliminarlo**:
    ```bash
    git stash pop
    ```
    - Este comando aplica el stash más reciente a tu área de trabajo y lo elimina de la lista de stashes. Es útil cuando estás listo para continuar trabajando en los cambios que habías guardado anteriormente.

11. **Ver el historial de commits nuevamente**:
    ```bash
    git log
    ```
    - Verifica que los cambios se han aplicado correctamente y que el historial de commits refleja cualquier cambio nuevo.

12. **Hacer un commit con los cambios recuperados del stash**:
    ```bash
    git commit -am "Misiones.md: Actualizada"
    ```
    - Confirma los cambios aplicados desde el stash, asegurando que los cambios estén ahora en el historial de commits.

13. **Ver el historial de commits final**:
    ```bash
    git log
    ```
    - Verifica el historial final para asegurarte de que todos los cambios se han comprometido correctamente.

### **Resumen de `git stash`**

- **Guardar cambios no confirmados**: `git stash`
- **Listar stashes**: `git stash list`
- **Aplicar y eliminar el stash más reciente**: `git stash pop`
- **Aplicar un stash sin eliminarlo**: `git stash apply`
- **Eliminar un stash específico**: `git stash drop stash@{n}`
- **Eliminar todos los stashes**: `git stash clear`

`git stash` es una herramienta esencial para mantener tu flujo de trabajo flexible, permitiéndote cambiar de contexto sin perder el trabajo en progreso.