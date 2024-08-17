# Push de los Tags de nuestro repositorio

Para subir los tags de tu repositorio local a GitHub, necesitas seguir algunos pasos específicos. Los tags son referencias a puntos específicos en la historia del repositorio, y se utilizan a menudo para marcar versiones importantes del código, como lanzamientos o hitos.

### 1. **Crear un Tag**

Antes de poder hacer `push` de los tags, primero debes crearlos en tu repositorio local. Puedes crear tags ligeros o anotados.

**Crear un Tag Ligero:**

```bash
git tag <nombre-del-tag>
```

- **Ejemplo:** `git tag v1.0.0`

**Crear un Tag Anotado:**

```bash
git tag -a <nombre-del-tag> -m "Mensaje del tag"
```

- **Ejemplo:** `git tag -a v1.0.0 -m "Versión 1.0.0"`

- Los tags anotados se almacenan como objetos completos en Git y contienen información adicional como el autor y la fecha.

### 2. **Verificar los Tags Locales**

Para ver los tags que has creado en tu repositorio local, usa:

```bash
git tag
```

### 3. **Hacer Push de un Tag Específico**

Para subir un tag específico al repositorio remoto en GitHub, usa:

```bash
git push origin <nombre-del-tag>
```

- **Ejemplo:** `git push origin v1.0.0`

### 4. **Hacer Push de Todos los Tags**

Si deseas subir todos los tags de tu repositorio local al repositorio remoto, usa:

```bash
git push --tags
```

Este comando sube todos los tags que has creado localmente al repositorio remoto.

### Ejemplo Completo de Manejo de Tags

1. **Crear un Tag Anotado:**

   ```bash
   git tag -a v1.0.0 -m "Versión 1.0.0"
   ```

2. **Verificar los Tags Locales:**

   ```bash
   git tag
   ```

3. **Hacer Push del Tag Específico:**

   ```bash
   git push origin v1.0.0
   ```

4. **Hacer Push de Todos los Tags:**

   ```bash
   git push --tags
   ```

### 5. **Verificar los Tags en GitHub**

Después de hacer `push`, puedes verificar que los tags se han subido correctamente navegando a la sección de "Releases" en tu repositorio de GitHub o revisando la lista de tags en la página del repositorio.

Estos pasos te permiten gestionar y compartir tus tags con otros colaboradores o para referencia futura en el repositorio remoto en GitHub. Si tienes alguna pregunta adicional sobre los tags o cualquier otro aspecto de Git, no dudes en preguntar.