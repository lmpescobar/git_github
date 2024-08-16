# Rebase - Actualizando una rama

### **Rebase - Actualizando una Rama**

El proceso de rebase es útil para actualizar una rama con los últimos cambios de otra rama, como `master`, sin crear un commit de fusión. Esto mantiene el historial de commits lineal y más fácil de seguir.

### **Pasos Detallados**

1. **Revisar el historial de commits**:
   ```bash
   git log
   ```
   - Muestra el historial de commits actual para verificar el estado de las ramas.

2. **Listar todas las ramas**:
   ```bash
   git branch
   ```
   - Muestra todas las ramas locales, para asegurarte de que estás trabajando en la rama correcta.

3. **Cambiar a la rama que quieres actualizar**:
   ```bash
   git checkout rama-misiones-completadas
   ```
   - Cambia a la rama `rama-misiones-completadas`, que es la que deseas actualizar con los cambios recientes de `master`.

4. **Verificar la rama activa**:
   ```bash
   git branch
   ```
   - Confirma que estás en la rama correcta (`rama-misiones-completadas`).

5. **Rebase de `rama-misiones-completadas` sobre `master`**:
   ```bash
   git rebase master
   ```
   - Este comando mueve los commits de `rama-misiones-completadas` para que se apliquen sobre la punta de `master`. Si `master` ha recibido actualizaciones desde que comenzaste a trabajar en `rama-misiones-completadas`, esos cambios ahora estarán integrados.

6. **Revisar el nuevo historial de commits**:
   ```bash
   git log
   ```
   - Verifica el historial de commits para asegurarte de que los commits de `rama-misiones-completadas` ahora están en la parte superior de los commits de `master`.

7. **Cambiar de vuelta a `master`**:
   ```bash
   git checkout master
   ```
   - Cambia a la rama `master` para fusionar los cambios de `rama-misiones-completadas`.

8. **Fusionar `rama-misiones-completadas` en `master`**:
   ```bash
   git merge rama-misiones-completadas
   ```
   - Fusiona `rama-misiones-completadas` en `master`. Dado que ya realizaste un rebase, esta fusión debería ser un fast-forward (una actualización rápida sin un commit de fusión).

9. **Listar las ramas para verificar el estado**:
   ```bash
   git branch
   ```
   - Confirma que las ramas están actualizadas y que `rama-misiones-completadas` ya ha sido fusionada en `master`.

10. **Eliminar la rama `rama-misiones-completadas`**:
    ```bash
    git branch -d rama-misiones-completadas
    ```
    - Ahora que los cambios han sido fusionados en `master`, puedes eliminar la rama `rama-misiones-completadas` ya que no es necesaria.

### **Resumen**

El rebase es una técnica poderosa para mantener el historial de commits limpio y lineal. Al actualizar una rama con `git rebase`, se integran los últimos cambios de la rama base sin crear un commit de fusión adicional. Esto es especialmente útil para mantener un proyecto organizado y evitar complejidades en el historial. 

Recuerda que siempre es buena práctica revisar los commits antes y después de un rebase para asegurarte de que todo se ha aplicado correctamente. Además, si trabajas en un equipo, evita hacer rebase en ramas compartidas, ya que reescribir la historia puede causar problemas para otros colaboradores.