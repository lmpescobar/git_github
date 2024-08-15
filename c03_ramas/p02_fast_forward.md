# Merge: Fast-Forward

### **1. Creación y Manejo de Ramas**

1. **Ver el historial de commits**:
   ```bash
   git log
   ```

2. **Crear una nueva rama llamada `rama-villanos`**:
   ```bash
   git branch rama-villanos
   ```

3. **Listar todas las ramas**:
   ```bash
   git branch
   ```

4. **Cambiar a la nueva rama `rama-villanos`**:
   ```bash
   git checkout rama-villanos
   ```

5. **Ver el historial de commits en la rama `rama-villanos`**:
   ```bash
   git log
   ```

### **2. Hacer Cambios en la Rama `rama-villanos`**

6. **Agregar todos los archivos al área de staging**:
   ```bash
   git add .
   ```

7. **Hacer un commit con un mensaje**:
   ```bash
   git commit -m "Villanos.md Agregado"
   ```

8. **Ver el historial de commits nuevamente**:
   ```bash
   git log
   ```

9. **Hacer un commit adicional con un mensaje diferente**:
   ```bash
   git commit -am "Villanos.md: Flash Reverso añadido"
   ```

10. **Ver el historial de commits nuevamente**:
    ```bash
    git log
    ```

### **3. Volver a la Rama Principal (`master`) y Hacer el Merge**

11. **Cambiar de vuelta a la rama `master`**:
    ```bash
    git checkout master
    ```

12. **Ver todas las ramas**:
    ```bash
    git branch
    ```

13. **Cambiar nuevamente a la rama `rama-villanos` (si es necesario para verificar o hacer más cambios)**:
    ```bash
    git checkout rama-villanos
    ```

14. **Cambiar de nuevo a la rama `master`**:
    ```bash
    git checkout master
    ```

15. **Ver todas las ramas**:
    ```bash
    git branch
    ```

16. **Hacer el merge de la rama `rama-villanos` en `master`**:
    ```bash
    git merge rama-villanos
    ```

17. **Ver el historial de commits después del merge**:
    ```bash
    git log
    ```

### **4. Borrar la Rama**

18. **Eliminar la rama `rama-villanos`**:
    ```bash
    git branch -d rama-villanos
    ```

19. **Forzar la eliminación de la rama `rama-villanos` (si no se ha eliminado porque aún no ha sido fusionada completamente)**:
    ```bash
    git branch -d rama-villanos -f
    ```

### **Explicación del Merge Fast-Forward**

Cuando haces un merge de una rama en Git y no hay commits adicionales en la rama principal desde que se creó la rama que estás fusionando, Git puede hacer un *fast-forward merge*. Esto significa que Git simplemente mueve el puntero de la rama principal hacia adelante hasta el último commit de la rama que estás fusionando. No se crea un nuevo commit de merge, ya que el historial de commits de la rama fusionada está directamente en línea con la rama principal.

### **Resumen de Comandos Importantes**

- `git branch`: Lista y maneja ramas.
- `git checkout <rama>`: Cambia de rama.
- `git merge <rama>`: Fusiona una rama en la rama actual.
- `git branch -d <rama>`: Elimina una rama local.
- `git branch -d <rama> -f`: Fuerza la eliminación de una rama local.

Estos comandos te ayudan a gestionar ramas, hacer cambios, fusionar cambios y mantener tu repositorio organizado.