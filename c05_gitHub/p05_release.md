# Creando - release tags

Para crear y gestionar "release tags" (etiquetas de versión) en GitHub, se utilizan tags en Git que se suelen asociar con versiones específicas del software.

### 1. **Crear un Tag Anotado para una Release**

Los tags anotados son ideales para las releases porque incluyen información adicional, como el nombre del autor, la fecha y un mensaje.

**Paso 1: Crear un Tag Anotado**

1. **Desde la Línea de Comandos:**

   ```bash
   git tag -a <nombre-del-tag> -m "Mensaje del tag"
   ```

   - **Ejemplo:** Si estás lanzando la versión 1.0.0, el comando sería:

     ```bash
     git tag -a v1.0.0 -m "Release version 1.0.0"
     ```

2. **Sube el Tag al Repositorio Remoto:**

   ```bash
   git push origin <nombre-del-tag>
   ```

   - **Ejemplo:** Para subir el tag `v1.0.0`:

     ```bash
     git push origin v1.0.0
     ```

### 2. **Crear una Release en GitHub**

Una vez que has creado y subido el tag a GitHub, puedes crear una release a partir de ese tag para proporcionar detalles adicionales sobre la versión.

**Paso 1: Ir a la Página del Repositorio en GitHub**

1. Navega a tu repositorio en GitHub.

2. **Haz clic en la pestaña "Releases":**

3. **Haz clic en "Draft a new release":**

**Paso 2: Completar el Formulario de Release**

1. **Selecciona el Tag:**

   - En el campo **"Tag version"**, selecciona el tag que has creado previamente. GitHub te mostrará los tags disponibles en el repositorio.

2. **Rellena los Detalles de la Release:**

   - **Release Title:** Proporciona un título para la release (por ejemplo, "Versión 1.0.0").
   - **Description:** Escribe una descripción de los cambios incluidos en esta release. Puedes utilizar Markdown para formatear el texto.
   - **Attach binaries:** Si tienes archivos binarios o artefactos de construcción que quieres adjuntar, puedes subirlos aquí.

3. **Publicar la Release:**

   - Una vez que hayas completado todos los campos, haz clic en **"Publish release"** para hacer pública la release.

### Ejemplo Completo

Aquí tienes un flujo completo para crear y publicar una release en GitHub:

1. **Desde la Línea de Comandos:**

   ```bash
   # Crea un tag anotado
   git tag -a v1.0.0 -m "Release version 1.0.0"
   
   # Sube el tag al repositorio remoto
   git push origin v1.0.0
   ```

2. **En GitHub:**

   1. Navega a la pestaña **"Releases"** de tu repositorio.
   2. Haz clic en **"Draft a new release"**.
   3. Selecciona el tag `v1.0.0`.
   4. Completa el título y la descripción de la release.
   5. Haz clic en **"Publish release"**.

### Beneficios de Usar Releases

- **Documentación:** Proporciona un historial claro de las versiones y cambios importantes.
- **Descargas:** Permite a los usuarios descargar versiones específicas del software.
- **Visibilidad:** Hace que sea más fácil para los colaboradores y usuarios ver los cambios significativos y las mejoras en el proyecto.