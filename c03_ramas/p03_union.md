# Merge: Union automática

### **Secuencia de Comandos y Explicación**

1. **Crear y cambiar a una nueva rama llamada `rama-villanos`**:
   ```bash
   git checkout -b rama-villanos
   ```
   - Esto crea una nueva rama llamada `rama-villanos` y cambia a ella. El `-b` es un atajo para crear y cambiar a una nueva rama en un solo comando.

2. **Listar todas las ramas para verificar que la nueva rama se creó correctamente**:
   ```bash
   git branch
   ```

3. **Realizar un commit con el mensaje "Agregamos a Doomsday"**:
   ```bash
   git commit -am "Agregamos a Doomsday"
   ```
   - El `-a` agrega automáticamente todos los archivos modificados al área de staging antes de hacer el commit. El `-m` especifica el mensaje del commit.

4. **Realizar un segundo commit con el mensaje "Notas en Villanos"**:
   ```bash
   git commit -am "Notas en Villanos"
   ```
   - Similar al anterior, este commit guarda cambios adicionales con un nuevo mensaje.

5. **Ver el historial de commits en la rama `rama-villanos`**:
   ```bash
   git log
   ```

6. **Listar todas las ramas para confirmar que estás en `rama-villanos`**:
   ```bash
   git branch
   ```

7. **Cambiar a la rama `master`**:
   ```bash
   git checkout master
   ```

8. **Realizar un commit en `master` con el mensaje "Borramos a Daredevil"**:
   ```bash
   git commit -am "Borramos a Daredevil"
   ```
   - Este commit se hace en la rama `master` y refleja cambios específicos en esta rama.

9. **Ver el historial de commits en la rama `master`**:
   ```bash
   git log
   ```

10. **Listar todas las ramas para confirmar que estás en `master`**:
    ```bash
    git branch
    ```

11. **Fusionar la rama `rama-villanos` en `master`**:
    ```bash
    git merge rama-villanos
    ```
    - Dado que no hay cambios en `master` que entren en conflicto con los cambios en `rama-villanos`, Git puede hacer un merge automático. Esto implica que Git aplicará los cambios de `rama-villanos` directamente en `master` sin necesidad de resolver conflictos.

12. **Ver el historial de commits después del merge**:
    ```bash
    git log
    ```
    - Ahora deberías ver los commits de `rama-villanos` en el historial de `master`, reflejando la integración exitosa de los cambios.

### **Explicación del Merge Automático**

Un merge automático ocurre cuando Git puede integrar los cambios de una rama en otra sin conflictos. Esto sucede cuando:

- Los cambios en las dos ramas no afectan las mismas líneas del mismo archivo.
- La rama que estás fusionando (`rama-villanos` en este caso) se creó a partir de un commit que está en la historia de la rama en la que estás haciendo el merge (`master`).

### **Resumen de Comandos Importantes**

- **Crear y cambiar de rama**: `git checkout -b <rama>`
- **Listar ramas**: `git branch`
- **Hacer commits**: `git commit -am "mensaje"`
- **Ver el historial de commits**: `git log`
- **Cambiar de rama**: `git checkout <rama>`
- **Fusionar ramas**: `git merge <rama>`

Estos pasos y comandos te permiten gestionar el flujo de trabajo en Git, asegurando que puedas integrar cambios de diferentes ramas de manera eficiente. El merge automático es una característica útil cuando trabajas en ramas paralelas que no tienen conflictos entre sí.