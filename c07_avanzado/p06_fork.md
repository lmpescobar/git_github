# Actualizando Nuestro Fork - Práctica

**Objetivo del Ejercicio:**

El objetivo de este ejercicio es actualizar un fork en GitHub para incorporar los cambios realizados en el repositorio original (upstream) en nuestro fork personal. Esto es útil cuando trabajamos con un repositorio bifurcado y queremos asegurarnos de que nuestro fork esté al día con las actualizaciones del repositorio original.

**Pasos para Actualizar un Fork:**

1. **Identificar el Repositorio Original (Upstream):**
   - El repositorio del cual hicimos el fork es conocido como "upstream".
   - Debemos tener el URL de este repositorio para poder integrarlo a nuestro repositorio local.

2. **Agregar el Repositorio Upstream como Remoto:**
   - En la terminal de Git, primero verificamos los remotos actuales con:
     ```bash
     git remote -v
     ```
   - Luego, agregamos el repositorio upstream:
     ```bash
     git remote add upstream <URL-del-repositorio-upstream>
     ```

3. **Obtener los Cambios del Repositorio Upstream:**
   - Para traer los cambios del upstream a nuestra copia local, utilizamos:
     ```bash
     git fetch upstream
     ```

4. **Fusionar los Cambios del Upstream con Nuestra Rama Local:**
   - Verificamos los cambios traídos:
     ```bash
     git log upstream/master
     ```
   - Fusionamos los cambios del upstream en nuestra rama actual:
     ```bash
     git merge upstream/master
     ```
   - Si se presentan conflictos, resuélvelos y luego confirma los cambios:
     ```bash
     git commit -m "Resuelto conflicto de fusión"
     ```

5. **Subir los Cambios a Nuestro Fork en GitHub:**
   - Finalmente, subimos los cambios fusionados a nuestro repositorio en GitHub:
     ```bash
     git push origin master
     ```

**Ejemplo Práctico:**

1. **Preparación:**
   - Supongamos que tenemos el repositorio `LegionDelMal` como nuestro repositorio original y `batman-fork` como nuestro fork.
   - En `batman-fork`, añadimos el remoto `upstream` y lo configuramos:
     ```bash
     git remote add upstream https://github.com/legiondelmal/original-repo.git
     ```

2. **Actualización:**
   - Verificamos que el remoto `upstream` se haya añadido:
     ```bash
     git remote -v
     ```
   - Hacemos un fetch para traer los cambios del upstream:
     ```bash
     git fetch upstream
     ```
   - Fusionamos los cambios en nuestra rama actual:
     ```bash
     git merge upstream/master
     ```
   - Resolvemos cualquier conflicto si es necesario y confirmamos los cambios:
     ```bash
     git commit -m "Actualización desde el repositorio upstream"
     ```
   - Subimos los cambios a nuestro fork:
     ```bash
     git push origin master
     ```

**Consideraciones Finales:**

- **Revisión de Conflictos:** Siempre revisa los conflictos cuidadosamente y asegúrate de resolverlos de manera que no afecten el funcionamiento de tu código.
- **Frecuencia de Actualización:** Es recomendable actualizar tu fork regularmente para mantener tu repositorio al día con los cambios del upstream.

**Sugerencia de Práctica:**

- Si solo tienes un usuario de GitHub, puedes crear un segundo repositorio para probar la actualización de forks. Alternativamente, puedes colaborar con un amigo que también esté haciendo el curso para realizar estas pruebas de manera colaborativa.