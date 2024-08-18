# Cerrar un issue

### Método 1: Cierre Manual desde la Interfaz Web

1. **Accede al Repositorio:**
   - Ve al repositorio en GitHub donde se encuentra el issue.

2. **Dirígete a la Sección de Issues:**
   - Haz clic en la pestaña "Issues" en la parte superior del repositorio.

3. **Selecciona el Issue que Quieres Cerrar:**
   - Encuentra el issue que deseas cerrar y haz clic en él para abrirlo.

4. **Cierra el Issue:**
   - Haz clic en el botón "Close issue" ubicado en la parte inferior derecha del issue.

### Método 2: Cierre Automático mediante un Commit

1. **Realiza Cambios y Realiza un Commit:**
   - En tu repositorio local, realiza los cambios necesarios en el código que resuelven el issue.
   - Haz un commit de estos cambios con un mensaje que incluya la referencia al issue. Por ejemplo: `git commit -m "Soluciona el problema de Nick Fury en el issue #3"`.

2. **Empuja los Cambios al Repositorio Remoto:**
   - Usa el comando `git push` para subir los cambios al repositorio en GitHub.

3. **Automáticamente Cierra el Issue:**
   - Cuando el mensaje del commit incluye `Fixes #<número del issue>`, GitHub cerrará automáticamente el issue asociado cuando se realice el merge del commit.

### Notas Adicionales:

- **Referencias en Commits:** Puedes hacer referencia a un issue en un commit usando `#<número del issue>`. Esto crea un enlace en el commit que apunta al issue, facilitando el seguimiento de cambios.

- **Cierre con Mensaje de Comentario:**
   - Si prefieres no usar la referencia automática, puedes añadir un comentario en el issue mencionando que el problema ha sido resuelto y cerrarlo manualmente después.

- **Eliminar Issues:**
   - Los issues no se pueden borrar fácilmente a menos que seas un administrador del repositorio. Para eliminar un issue, ve al issue, haz clic en los tres puntos en la esquina superior derecha y selecciona "Delete issue". Esto es irreversible, así que úsalo con precaución.

Estas técnicas te permitirán gestionar eficazmente los issues en GitHub, asegurando que los problemas se resuelvan y se registren adecuadamente en el repositorio.