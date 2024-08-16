# Stash avanzado

### **Stash Avanzado en Git**

1. **Limpiar todos los stashes existentes**:
   ```bash
   git stash clear
   ```
   - Este comando elimina todos los stashes que se hayan guardado previamente en el repositorio. Es útil para limpiar tu lista de stashes antes de comenzar a trabajar con nuevos.

2. **Ver el registro de referencia (`reflog`)**:
   ```bash
   git reflog
   ```
   - `git reflog` muestra un registro de todos los cambios y movimientos en las referencias del repositorio, incluidos commits, merges, y stashes. Es útil para recuperar un estado anterior si algo sale mal.

3. **Guardar múltiples stashes**:
   ```bash
   git stash
   git stash
   git stash
   ```
   - Estos comandos guardan el estado actual del directorio de trabajo tres veces, creando tres stashes diferentes en la pila de stashes. Cada uno de ellos es independiente y puede ser aplicado, eliminado o inspeccionado más tarde.

4. **Listar todos los stashes**:
   ```bash
   git stash list
   ```
   - Muestra una lista de todos los stashes que has creado, ordenados por el más reciente (`stash@{0}`) al más antiguo. Esto te permite identificar cada stash por su posición en la pila.

5. **Aplicar un stash específico**:
   ```bash
   git stash apply stash@{2}
   ```
   - Aplica el stash en la posición `stash@{2}` (el tercer stash más antiguo). A diferencia de `git stash pop`, `git stash apply` no elimina el stash después de aplicarlo.

6. **Guardar otro stash**:
   ```bash
   git stash
   ```
   - Este comando guarda el estado actual del directorio de trabajo como un nuevo stash, incrementando la pila.

7. **Eliminar un stash específico**:
   ```bash
   git stash drop stash@{0}
   ```
   - Elimina el stash en la posición `stash@{0}` (el más reciente). Es útil cuando ya no necesitas un stash específico y quieres limpiar la pila.

8. **Mostrar detalles de un stash específico**:
   ```bash
   git stash show stash@{1}
   git stash show stash@{2}
   ```
   - Estos comandos muestran los cambios incluidos en los stashes `stash@{1}` y `stash@{2}`. Esto te permite ver qué modificaciones fueron guardadas en esos stashes sin aplicarlos.

9. **Guardar un stash con un mensaje descriptivo**:
   ```bash
   git stash save "Agregamos a Loki en villanos"
   ```
   - Guarda el estado actual con un mensaje que describe el stash. Esto es útil para identificar fácilmente el contenido del stash cuando revises la lista más adelante.

10. **Listar los stashes con estadísticas**:
    ```bash
    git stash list --stat
    ```
    - Este comando muestra una lista de todos los stashes junto con un resumen estadístico de los cambios en cada uno, como las líneas añadidas o eliminadas.

11. **Aplicar y eliminar el stash más reciente**:
    ```bash
    git stash pop
    ```
    - Aplica el stash más reciente (`stash@{0}`) y lo elimina de la pila. Es útil cuando estás listo para reincorporar los cambios guardados a tu área de trabajo.

12. **Confirmar los cambios aplicados desde el stash**:
    ```bash
    git commit -am "Agregamos a Loki en los villanos"
    ```
    - Después de aplicar el stash, confirmas los cambios, asegurando que las modificaciones se guarden en el historial de commits.

13. **Limpiar todos los stashes**:
    ```bash
    git stash clear
    ```
    - Este comando final elimina cualquier stash restante, asegurando que no haya stashes innecesarios ocupando espacio.

### **Resumen**

El manejo avanzado de `git stash` te permite trabajar con múltiples stashes, aplicar o eliminar stashes específicos, inspeccionar los cambios guardados, y mantener un flujo de trabajo limpio y organizado. Usar mensajes descriptivos para los stashes facilita recordar qué cambios se guardaron, mientras que los comandos `apply`, `pop`, y `drop` te dan flexibilidad para manejar estos cambios cuando sea necesario.