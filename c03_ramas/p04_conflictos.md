# Merge: Uniones con conflictos

### **Secuencia de Comandos y Explicación**

1. **Crear y cambiar a una nueva rama llamada `rama-conflicto`**:
   ```bash
   git checkout -b rama-conflicto
   ```
   - Esto crea una nueva rama `rama-conflicto` y cambia a ella.

2. **Listar todas las ramas para confirmar la nueva rama**:
   ```bash
   git branch
   ```

3. **Realizar un commit en `rama-conflicto` con el mensaje "Misiones: Actualizada"**:
   ```bash
   git commit -am "Misiones: Actualizada"
   ```
   - Aquí, se guardan los cambios en la rama `rama-conflicto`.

4. **Listar las ramas nuevamente para confirmar que estás en `rama-conflicto`**:
   ```bash
   git branch
   ```

5. **Ver el historial de commits en `rama-conflicto`**:
   ```bash
   git log
   ```

6. **Cambiar a la rama `master`**:
   ```bash
   git checkout master
   ```

7. **Ver el historial de commits en `master`**:
   ```bash
   git log
   ```

8. **Realizar un commit en `master` con el mensaje "Misiones: Actualizada MASTER"**:
   ```bash
   git commit -am "Misiones: Actualizada MASTER"
   ```
   - Aquí, se realiza un cambio en la rama `master` que también afecta al archivo que se modificó en `rama-conflicto`.

9. **Ver el historial de commits en `master` nuevamente**:
   ```bash
   git log
   ```

10. **Listar las ramas para confirmar que estás en `master`**:
    ```bash
    git branch
    ```

11. **Fusionar `rama-conflicto` en `master`**:
    ```bash
    git merge rama-conflicto
    ```
    - Dado que has realizado cambios en `master` y en `rama-conflicto` en la misma parte del archivo, Git detectará un conflicto durante el merge.

12. **Ver el estado de los archivos después del merge**:
    ```bash
    git status
    ```
    - Esto mostrará que hay archivos con conflictos y necesitan ser resueltos.

13. **Resolver los conflictos manualmente**:
    - Abre los archivos que tienen conflictos. Verás marcadores como `<<<<<<<`, `=======`, y `>>>>>>>` en los archivos. Tendrás que editar estos archivos para resolver los conflictos y decidir qué cambios conservar.

14. **Agregar los archivos resueltos al área de staging**:
    ```bash
    git add <archivo-conflictivo>
    ```
    - Reemplaza `<archivo-conflictivo>` con los nombres de los archivos que resolviste.

15. **Hacer un commit para finalizar el merge**:
    ```bash
    git commit -am "Union con rama-conflicto"
    ```
    - Esto crea un nuevo commit de merge que incluye las resoluciones de conflictos.

16. **Ver el historial de commits después de resolver el conflicto y hacer el merge**:
    ```bash
    git log
    ```

17. **Eliminar la rama `rama-conflicto`**:
    ```bash
    git branch -d rama-conflicto
    ```
    - Elimina la rama `rama-conflicto` ya que sus cambios han sido integrados en `master`.

18. **Ver el historial de commits nuevamente para confirmar la eliminación de la rama**:
    ```bash
    git log
    ```

### **Explicación de Conflictos de Merge**

Un conflicto de merge ocurre cuando:

- **Cambios concurrentes**: Ambas ramas modifican la misma parte del archivo de manera diferente.
- **Resolución manual**: Debes abrir los archivos conflictivos, resolver los conflictos y luego hacer un commit para finalizar el merge.

### **Marcadores de Conflicto**

- `<<<<<<< HEAD`: Muestra los cambios en la rama actual (`master` en este caso).
- `=======`: Separa los cambios en la rama actual de los cambios en la rama que estás intentando fusionar (`rama-conflicto`).
- `>>>>>>> rama-conflicto`: Muestra los cambios en la rama que estás fusionando.

### **Resumen de Comandos Relacionados con Conflictos**

- **Ver estado del merge**: `git status`
- **Resolver conflictos manualmente**: Edita los archivos conflictivos.
- **Agregar archivos resueltos**: `git add <archivo-conflictivo>`
- **Hacer commit después del merge**: `git commit -am "mensaje"`

Estos pasos y comandos te ayudan a gestionar y resolver conflictos de merge en Git, asegurando que puedes integrar cambios de manera efectiva incluso cuando hay discrepancias entre ramas.