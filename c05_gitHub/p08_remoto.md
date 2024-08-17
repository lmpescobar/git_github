# Subir cambios locales al remoto

# Git Pull Rebase

### **Subir Cambios Locales al Remoto usando `Rebase`**

1. **Realizar un Commit Local:**

   ```bash
   git commit -am "Readme.md actualizado"
   ```

   - **Descripción:** Este comando agrega todos los archivos modificados al commit (`-a`) y crea un commit con el mensaje "Readme.md actualizado". El `-m` se usa para proporcionar el mensaje del commit.

2. **Verificar el Historial de Commits:**

   ```bash
   git log
   ```

   - **Descripción:** Muestra el historial de commits, permitiéndote revisar los cambios que has registrado.

3. **Enviar los Cambios al Repositorio Remoto:**

   ```bash
   git push
   ```

   - **Descripción:** Sube los cambios locales al repositorio remoto en la rama actual. Si otros colaboradores han realizado cambios en la misma rama, Git podría rechazar el push, requiriendo una sincronización primero.

4. **Realizar otro Commit Local:**

   ```bash
   git commit -am "Readme.md Local actualizado"
   ```

   - **Descripción:** Similar al paso 1, este commit incluye nuevas modificaciones con un mensaje diferente.

5. **Obtener Cambios del Repositorio Remoto:**

   ```bash
   git pull
   ```

   - **Descripción:** Sincroniza la rama local con los cambios más recientes del repositorio remoto. Si hay conflictos o diferencias significativas, Git intentará fusionar los cambios.

6. **Configurar `Rebase` como Estrategia de `Pull`:**

   ```bash
   git config --global pull.rebase true
   ```

   - **Descripción:** Este comando configura Git para que, en lugar de realizar una fusión automática (`merge`), utilice `rebase` cuando hagas `git pull`. El `rebase` reorganiza tus commits locales en la parte superior de los commits obtenidos desde el remoto, creando una historia más lineal y fácil de leer.

7. **Realizar un Pull con `Rebase`:**

   ```bash
   git pull
   ```

   - **Descripción:** Ahora que `pull.rebase` está configurado, este comando primero trae los cambios del remoto y luego intenta "rebasar" (reaplicar) tus commits locales sobre esos cambios. Si hay conflictos, Git te pedirá que los resuelvas antes de continuar.

8. **Verificar las Ramas Disponibles:**

   ```bash
   git branch
   ```

   - **Descripción:** Este comando lista todas las ramas locales y destaca la rama en la que estás trabajando.

9. **Agregar Cambios al Área de Staging:**

   ```bash
   git add .
   ```

   - **Descripción:** Este comando añade todos los cambios (nuevos archivos, modificaciones y eliminaciones) al área de staging, preparándolos para el próximo commit.

10. **Verificar el Estado Actual del Repositorio:**

    ```bash
    git status
    ```

    - **Descripción:** Muestra el estado de los archivos en tu directorio de trabajo y en el área de staging. Es útil para asegurarse de que todo está en orden antes de hacer un commit o un push.

11. **Realizar un Commit:**

    ```bash
    git commit -m "Readme unificado con oringin/main"
    ```

    - **Descripción:** Este commit incluye los cambios que unifican tu trabajo con la rama principal (`main`).

12. **Continuar el `Rebase` (si es necesario):**

    ```bash
    git rebase --continue
    ```

    - **Descripción:** Si el `rebase` fue interrumpido por conflictos, después de resolverlos, debes ejecutar este comando para continuar el proceso.

13. **Subir los Cambios al Remoto:**

    ```bash
    git push
    ```

    - **Descripción:** Sube todos los cambios y commits recientes al repositorio remoto.

14. **Almacenar Cambios Temporalmente (si es necesario):**

    ```bash
    git stash
    ```

    - **Descripción:** Este comando guarda temporalmente tus cambios no confirmados y limpia tu directorio de trabajo, permitiéndote hacer otras operaciones sin perder tu trabajo. Puedes recuperar estos cambios más tarde con `git stash pop`.

15. **Comando Final para Unificar y Subir Cambios:**

    ```bash
    git commit -am "Readme unificado con main"
    git push
    ```

    - **Descripción:** Este es un commit final que unifica todo antes de hacer un push al remoto.

### **Resumen**

Este flujo de trabajo es ideal para mantener un historial de commits limpio y ordenado, especialmente cuando trabajas en equipo. Utilizar `rebase` en lugar de `merge` evita los commits de fusión innecesarios y asegura que tu rama tenga una historia lineal.