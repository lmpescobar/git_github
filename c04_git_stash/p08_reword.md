# Rebase - Reword

El proceso de "reword" en Git Rebase permite modificar los mensajes de commit sin cambiar su contenido. Esto es útil si quieres clarificar o corregir un mensaje de commit anterior sin alterar el historial de cambios.

### **Rebase - Reword: Pasos Detallados**

1. **Revisar el historial de commits**:
   ```bash
   git log
   ```
   - Este comando muestra el historial de commits. Esto te permite identificar los commits cuyos mensajes deseas editar.

2. **Iniciar un rebase interactivo**:
   ```bash
   git rebase -i HEAD~4
   ```
   - Este comando inicia un rebase interactivo para los últimos 4 commits. Puedes ajustar `HEAD~4` para incluir más o menos commits según sea necesario.
   - Se abrirá un editor de texto que mostrará una lista de los últimos 4 commits, cada uno precedido por la palabra `pick`.

3. **Seleccionar commits para modificar**:
   - Cambia `pick` a `reword` (o `r`) para los commits cuyo mensaje deseas modificar.
   - Guarda y cierra el editor para proceder.

4. **Editar los mensajes de commit**:
   - Para cada commit que marcaste con `reword`, el editor se abrirá de nuevo permitiéndote modificar el mensaje de ese commit.
   - Edita el mensaje según lo necesites, guarda y cierra el editor.
   - Repite este paso para cada commit seleccionado.

5. **Revisar el historial después del rebase**:
   ```bash
   git log
   ```
   - Después de completar el rebase, revisa el historial de commits para confirmar que los mensajes han sido modificados correctamente.

### **Resumen**

El uso de "reword" en un rebase interactivo es una manera efectiva de mantener tus mensajes de commit claros y precisos, mejorando así la comprensión del historial de cambios. Como con otros tipos de rebase, ten en cuenta que estás reescribiendo el historial de commits, lo que puede afectar a otros si los commits ya han sido compartidos. Por lo tanto, es mejor hacer estas modificaciones antes de realizar un `git push`.

### **Ejemplo: Modificando un Mensaje de Commit con `git rebase -i`**

Supongamos que tienes el siguiente historial de commits:

```bash
$ git log --oneline
c3d8f56 (HEAD -> master) Actualización final del README
a6b1e29 Ajustes en el archivo de configuración
9f6f7c3 Corrección de errores en la función X
b1e2e8d Agregando nueva funcionalidad Y
```

Quieres modificar el mensaje del commit `b1e2e8d` ("Agregando nueva funcionalidad Y") para que sea más descriptivo.

### **Paso 1: Iniciar un rebase interactivo**

Ejecuta el siguiente comando:

```bash
git rebase -i HEAD~4
```

Esto abrirá un editor de texto (puede ser Vim, Nano, o el que tengas configurado). Verás algo parecido a esto:

```
pick b1e2e8d Agregando nueva funcionalidad Y
pick 9f6f7c3 Corrección de errores en la función X
pick a6b1e29 Ajustes en el archivo de configuración
pick c3d8f56 Actualización final del README
```

### **Paso 2: Seleccionar el commit a modificar**

Cambia `pick` a `reword` en el commit que quieres modificar. El archivo se verá así:

```
reword b1e2e8d Agregando nueva funcionalidad Y
pick 9f6f7c3 Corrección de errores en la función X
pick a6b1e29 Ajustes en el archivo de configuración
pick c3d8f56 Actualización final del README
```

Guarda y cierra el editor.

### **Paso 3: Editar el mensaje del commit**

Después de cerrar el editor, se abrirá automáticamente un nuevo editor con el mensaje del commit que seleccionaste. Verás algo como esto:

```
Agregando nueva funcionalidad Y
```

Modifica el mensaje para que sea más descriptivo, por ejemplo:

```
Añadiendo nueva funcionalidad Y para mejorar el rendimiento
```

Guarda y cierra el editor.

### **Paso 4: Completar el rebase**

Git completará el rebase y aplicará los cambios. Puedes revisar el nuevo historial de commits usando:

```bash
git log --oneline
```

Ahora el historial debería verse así:

```bash
c3d8f56 (HEAD -> master) Actualización final del README
a6b1e29 Ajustes en el archivo de configuración
9f6f7c3 Corrección de errores en la función X
b1e2e8d Añadiendo nueva funcionalidad Y para mejorar el rendimiento
```

El mensaje del commit `b1e2e8d` ha sido actualizado con el nuevo texto que especificaste. 

Este proceso de rebase interactivo te permite modificar el historial de commits para mejorar la claridad y precisión de los mensajes, lo que es especialmente útil en un equipo de desarrollo o cuando deseas mantener un historial de commits limpio y legible.