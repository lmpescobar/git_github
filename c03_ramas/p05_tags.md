# Creando etiquetas - Tags

En Git, las etiquetas (*tags*) son una forma de marcar puntos específicos en la historia del repositorio, a menudo para representar versiones de un proyecto.

### **Secuencia de Comandos y Explicación**

1. **Ver el historial de commits**:
   ```bash
   git log
   ```
   - Esto te permite ver el historial de commits y encontrar el SHA-1 de los commits para etiquetarlos.

2. **Crear una etiqueta ligera llamada `super-release`**:
   ```bash
   git tag super-release
   ```
   - Una etiqueta ligera es simplemente un marcador en el commit actual. No tiene metadatos adicionales como un mensaje.

3. **Ver el historial de commits nuevamente**:
   ```bash
   git log
   ```

4. **Listar todas las etiquetas**:
   ```bash
   git tag
   ```

5. **Eliminar una etiqueta llamada `super-release`**:
   ```bash
   git tag -d super-release
   ```
   - Elimina la etiqueta `super-release` localmente.

6. **Listar las etiquetas nuevamente para confirmar la eliminación**:
   ```bash
   git tag
   ```

7. **Crear una etiqueta anotada `v1.0.0` con un mensaje**:
   ```bash
   git tag -a v1.0.0 -m "Version 1.0.0 lista"
   ```
   - Una etiqueta anotada incluye un mensaje, el nombre del creador y la fecha. Es útil para versiones de lanzamiento.

8. **Listar todas las etiquetas para confirmar la creación de la etiqueta anotada**:
   ```bash
   git tag
   ```

9. **Ver el historial de commits nuevamente para verificar la etiqueta**:
   ```bash
   git log
   ```

10. **Crear una etiqueta anotada `v0.1.0` en un commit específico (`701c885`) con un mensaje**:
    ```bash
    git tag -a v0.1.0 701c885 -m "Version Alpha de nuestra app"
    ```
    - Esto etiqueta el commit con el SHA-1 `701c885` con la versión `v0.1.0` y un mensaje descriptivo.

11. **Ver el historial de commits nuevamente para verificar la etiqueta**:
    ```bash
    git log
    ```

12. **Listar todas las etiquetas para confirmar la creación de la etiqueta `v0.1.0`**:
    ```bash
    git tag
    ```

13. **Mostrar la información de la etiqueta `v0.1.0`**:
    ```bash
    git show v0.1.0
    ```
    - Esto muestra el commit asociado con la etiqueta `v0.1.0`, junto con el mensaje de la etiqueta y otros detalles.

### **Explicación Adicional**

- **Etiquetas ligeras vs. Etiquetas anotadas**:
  - **Ligera**: Solo un puntero a un commit. No incluye información adicional.
  - **Anotada**: Un objeto completo en Git que incluye un mensaje, la fecha, el nombre del creador, etc. Se recomienda para versiones de lanzamiento.

- **Eliminar Etiquetas**:
  - Para eliminar una etiqueta localmente, usa `git tag -d <nombre-etiqueta>`.
  - Para eliminar una etiqueta remota, usa `git push origin --delete <nombre-etiqueta>`.

- **Ver Detalles de una Etiqueta**:
  - `git show <nombre-etiqueta>` te da información sobre la etiqueta, el commit al que apunta, y el mensaje.

### **Resumen de Comandos Relacionados con Etiquetas**

- **Crear una etiqueta ligera**: `git tag <nombre-etiqueta>`
- **Crear una etiqueta anotada**: `git tag -a <nombre-etiqueta> -m "mensaje"`
- **Eliminar una etiqueta local**: `git tag -d <nombre-etiqueta>`
- **Mostrar información de una etiqueta**: `git show <nombre-etiqueta>`
- **Listar todas las etiquetas**: `git tag`

Estos comandos te permiten gestionar versiones y puntos importantes en tu proyecto de manera organizada y fácil de acceder.