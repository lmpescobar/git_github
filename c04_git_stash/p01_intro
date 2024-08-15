# Introducción al stash

El comando `git stash` en Git es una herramienta poderosa que te permite guardar temporalmente los cambios en tu directorio de trabajo que aún no has confirmado (commit). Esto es útil cuando estás trabajando en algo, pero necesitas cambiar de contexto rápidamente, por ejemplo, para revisar otra rama, sin perder tus cambios no confirmados.

### **¿Qué es `git stash`?**

`git stash` guarda los cambios actuales en tu espacio de trabajo (es decir, cambios en archivos rastreados y nuevas adiciones, pero no nuevos archivos no rastreados) y restablece el directorio de trabajo al estado del último commit. Es como una "pausa" temporal para tus cambios, permitiéndote regresar al punto donde dejaste más tarde.

### **¿Cómo funciona `git stash`?**

Aquí hay una breve guía sobre cómo usar `git stash`:

1. **Guardar los cambios en el stash**:
   ```bash
   git stash
   ```
   - Esto guarda tus cambios no confirmados en un "stash" y limpia tu directorio de trabajo, dejándote con un espacio limpio para trabajar en otra cosa.

2. **Listar los stashes guardados**:
   ```bash
   git stash list
   ```
   - Muestra una lista de todos los stashes que has creado. Cada entrada en la lista tiene un nombre en el formato `stash@{n}`, donde `n` es el número del stash.

3. **Aplicar el stash más reciente**:
   ```bash
   git stash apply
   ```
   - Esto aplica los cambios más recientes en el stash a tu directorio de trabajo, pero no elimina el stash. Los cambios permanecerán en la lista de stashes hasta que los elimines.

4. **Aplicar y eliminar el stash más reciente**:
   ```bash
   git stash pop
   ```
   - Esto aplica el stash más reciente a tu directorio de trabajo y luego lo elimina de la lista de stashes.

5. **Aplicar un stash específico**:
   ```bash
   git stash apply stash@{2}
   ```
   - Si tienes varios stashes y quieres aplicar uno específico, puedes referenciarlo por su índice.

6. **Eliminar un stash específico**:
   ```bash
   git stash drop stash@{2}
   ```
   - Elimina un stash específico de la lista.

7. **Eliminar todos los stashes**:
   ```bash
   git stash clear
   ```
   - Esto elimina todos los stashes guardados. Úsalo con precaución, ya que los cambios se perderán permanentemente.

8. **Crear un stash con un mensaje**:
   ```bash
   git stash save "Mensaje descriptivo"
   ```
   - Esto guarda los cambios en el stash con un mensaje específico, que te ayudará a recordar lo que estabas trabajando.

### **Ejemplo de uso**

Imagina que estás trabajando en una nueva característica en la rama `feature`, y de repente necesitas cambiar a la rama `master` para solucionar un problema urgente. Sin `git stash`, tendrías que hacer un commit de tus cambios incompletos, lo cual no siempre es ideal.

1. **Guardar tus cambios actuales**:
   ```bash
   git stash
   ```

2. **Cambiar a la rama `master`**:
   ```bash
   git checkout master
   ```

3. **Después de solucionar el problema en `master`, regresar a tu trabajo**:
   ```bash
   git checkout feature
   git stash pop
   ```

Tus cambios guardados en `stash` se aplicarán de nuevo, y puedes continuar trabajando en tu característica.

### **¿Cuándo usar `git stash`?**

- **Interrupciones inesperadas**: Si necesitas cambiar de rama repentinamente sin haber terminado tu trabajo.
- **Probar algo temporalmente**: Si deseas hacer pruebas o experimentos sin afectar tu trabajo actual.
- **Limpiar el espacio de trabajo**: Si quieres limpiar tu área de trabajo sin perder tus progresos.

`git stash` es una herramienta muy útil para gestionar contextos de trabajo múltiples y mantener tu flujo de trabajo limpio y organizado en Git.