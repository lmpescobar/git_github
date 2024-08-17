# Git pull - Ejercicio

Este ejercicio se enfoca en la integración de cambios locales y remotos utilizando `git pull` y `git rebase`.

### **Ejercicio: Sincronizando Cambios Locales y Remotos**

1. **Realizar un Commit Local:**

   ```bash
   git commit -am "Ciudades y Héroes actualizados"
   ```

   - **Descripción:** Este comando añade todos los archivos modificados (`-a`) y crea un commit con el mensaje "Ciudades y Héroes actualizados". Se utiliza `-m` para añadir un mensaje al commit.

2. **Enviar los Cambios al Repositorio Remoto:**

   ```bash
   git push
   ```

   - **Descripción:** Sube los cambios locales al repositorio remoto. Este es el primer paso para sincronizar tus cambios con los del servidor.

3. **Obtener los Cambios más Recientes del Remoto:**

   ```bash
   git pull
   ```

   - **Descripción:** Este comando sincroniza la rama local con los últimos cambios del repositorio remoto. Si hay algún cambio en el remoto que aún no está en tu rama local, Git intentará fusionar esos cambios.

4. **Realizar un Nuevo Commit Local:**

   ```bash
   git commit -am "Unificado ciudades y héroes"
   ```

   - **Descripción:** Después de haber hecho un `pull`, puedes realizar otro commit con los cambios que hayas integrado o modificado. Este commit unifica el trabajo previo con los nuevos cambios.

5. **Verificar el Estado del Repositorio:**

   ```bash
   git status
   ```

   - **Descripción:** Muestra el estado actual del directorio de trabajo y del área de staging, indicando si hay archivos pendientes de commit o si todo está listo para ser subido.

6. **Continuar el `Rebase` (si es necesario):**

   ```bash
   git rebase --continue
   ```

   - **Descripción:** Si durante el `pull` o el `rebase` anterior hubo conflictos y los resolviste, este comando permite continuar con el proceso de `rebase`.

7. **Verificar el Estado del Repositorio Nuevamente:**

   ```bash
   git status
   ```

   - **Descripción:** Después de resolver cualquier conflicto y continuar con el `rebase`, es buena práctica verificar nuevamente el estado para asegurarse de que todo está correcto.

8. **Subir los Cambios al Remoto:**

   ```bash
   git push
   ```

   - **Descripción:** Finalmente, sube todos los cambios (incluyendo los que fueron unificados y rebasados) al repositorio remoto.

### **Resumen**

Este ejercicio demuestra cómo manejar cambios locales y remotos usando `git pull` y `git rebase`, asegurando una integración sin conflictos. El `rebase` es especialmente útil para mantener un historial de commits limpio, evitando los commits de fusión que se generan con un `merge` tradicional.