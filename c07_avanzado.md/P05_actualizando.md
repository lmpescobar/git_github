# Actualizando nuestro Fork - Teoría

Actualizar nuestro fork es un proceso importante que nos permite mantener nuestro repositorio sincronizado con el repositorio central (a menudo llamado **upstream**). Este proceso es especialmente útil en situaciones donde trabajamos con repositorios compartidos, pero no queremos dar acceso total a otros colaboradores. En lugar de eso, permitimos que trabajen en una copia del repositorio mediante un fork. 

Vamos a desglosar el proceso con un ejemplo práctico:

## Escenario

Supongamos que tenemos un repositorio central en GitHub llamado **upstream**. Imaginemos que **Batman** y **Superman** hacen lo siguiente:

1. **Batman** hace un fork del repositorio **upstream** y comienza a trabajar en su copia del repositorio, que se encuentra en su cuenta de GitHub.
2. **Superman** también hace un fork del mismo repositorio y comienza a trabajar en su propia copia.

En este punto, tanto el repositorio de Batman como el de Superman son idénticos porque ninguno ha hecho cambios aún. 

## Trabajo Local y Sincronización

1. **Clonación del Repositorio:**
   - **Batman** clona su repositorio en su máquina local.
   - **Superman** también clona su repositorio en su máquina local.

2. **Modificaciones Locales:**
   - Ambos hacen cambios en sus repositorios locales.
   - Después de realizar estos cambios, hacen un `push` a sus respectivos repositorios en GitHub.

3. **Pull Requests:**
   - Para que sus cambios se integren en el repositorio **upstream**, ambos deben crear una **pull request**.

## Actualizando tu Fork

La pregunta del millón es: **¿cómo puede Batman actualizar su fork para incluir los cambios que Superman ha hecho?** Esto es importante para asegurarse de que Batman tenga acceso a los cambios de Superman, especialmente si esos cambios son necesarios para el trabajo de Batman.

### Proceso de Actualización

1. **Agregar el Remoto Upstream:**
   - Primero, necesitas agregar el repositorio original (**upstream**) como un remoto adicional en tu repositorio local. Esto permite que tu repositorio local se sincronice con el repositorio central.
   ```bash
   git remote add upstream <url-del-repositorio-original>
   ```

2. **Obtener los Cambios:**
   - Luego, debes obtener los cambios del repositorio **upstream**.
   ```bash
   git fetch upstream
   ```

3. **Integrar los Cambios en tu Rama Local:**
   - Puedes integrar los cambios descargados en tu rama local usando `merge` o `rebase`.
   - **Merge:** Funde los cambios con tu rama actual.
     ```bash
     git merge upstream/main
     ```
   - **Rebase:** Reescribe tu historial de commits para aplicar tus cambios encima de los cambios descargados.
     ```bash
     git rebase upstream/main
     ```

4. **Resolver Conflictos:**
   - Si hay conflictos entre tus cambios y los del repositorio **upstream**, tendrás que resolverlos. Edita los archivos conflictivos y marca los conflictos como resueltos.
   ```bash
   git add <archivo-resuelto>
   git commit
   ```

5. **Subir los Cambios a tu Fork:**
   - Finalmente, sube los cambios a tu repositorio en GitHub.
   ```bash
   git push origin main
   ```

## Resumen

Para mantener tu fork actualizado con el repositorio **upstream**:
1. Agrega el remoto upstream.
2. Haz un `fetch` para obtener los cambios.
3. Integra los cambios con `merge` o `rebase`.
4. Resuelve conflictos si es necesario.
5. Realiza un `push` a tu fork.

Estos pasos te permitirán trabajar con la versión más reciente del repositorio central y colaborar de manera efectiva con otros desarrolladores.