# Rebase - Squash

### **Rebase - Squash**

El proceso de "squash" en `git rebase` permite combinar múltiples commits en uno solo. Esto es útil cuando tienes varios commits pequeños que en realidad deberían ser un solo commit más grande. Al hacer un squash, puedes mantener un historial de commits más limpio y organizado.

### **Pasos Detallados**

1. **Revisar el historial de commits**:
   ```bash
   git log
   ```
   - Esto te muestra el historial de commits reciente. Es importante revisar los commits para asegurarte de que estás incluyendo los correctos en el rebase.

2. **Hacer un nuevo commit (opcional)**:
   ```bash
   git commit -am "Actualizamos misiones completadas"
   ```
   - Este comando crea un nuevo commit con un mensaje, si necesitas agregar algo más antes de hacer el squash.

3. **Iniciar el rebase interactivo**:
   ```bash
   git rebase -i HEAD~4
   ```
   - El comando `git rebase -i HEAD~4` inicia un rebase interactivo para los últimos 4 commits (puedes ajustar el número según lo que necesites). Esto abrirá un editor de texto donde podrás decidir qué hacer con cada commit.

4. **Combinar los commits (squash)**:
   - En el editor que se abre, verás una lista de los últimos 4 commits. Cada línea comienza con la palabra `pick`. Para hacer un squash, cambia `pick` a `squash` (o simplemente `s`) en todos los commits que quieras combinar con el commit anterior.

   - Por ejemplo, si tienes algo así:
     ```
     pick 1a2b3c4 Actualizamos misiones completadas
     pick 2b3c4d5 Otro cambio menor
     pick 3c4d5e6 Ajustes en la interfaz
     pick 4d5e6f7 Corrección de errores
     ```
     Cambia a:
     ```
     pick 1a2b3c4 Actualizamos misiones completadas
     squash 2b3c4d5 Otro cambio menor
     squash 3c4d5e6 Ajustes en la interfaz
     squash 4d5e6f7 Corrección de errores
     ```

   - Esto indicará a Git que combine estos commits en un solo commit.

5. **Editar el mensaje del commit**:
   - Después de hacer el squash, Git te permitirá editar el mensaje del nuevo commit. Puedes combinar los mensajes de los commits anteriores o escribir uno nuevo que resuma los cambios.

6. **Revisar el nuevo historial de commits**:
   ```bash
   git log
   ```
   - Verifica que el historial de commits ahora muestra un único commit en lugar de los múltiples que combinaste.

### **Resumen**

El uso de `git rebase` con la opción de `squash` es una excelente manera de limpiar tu historial de commits. Esto es especialmente útil antes de fusionar cambios en la rama principal, ya que ayuda a mantener un historial limpio y fácil de seguir. Es importante recordar que esta operación reescribe la historia de los commits, por lo que es mejor hacerlo en ramas que no han sido compartidas con otros colaboradores.