# Push a GitHub

### 1. **Preparativos Iniciales**

Asegúrate de haber creado un repositorio en GitHub y de tener un repositorio local configurado en tu máquina. Si no has clonado un repositorio, primero deberás inicializar uno y agregar archivos.

### 2. **Configura el Repositorio Remoto**

Si aún no has configurado un repositorio remoto en tu repositorio local, hazlo usando el siguiente comando:

```bash
git remote add origin <url-del-repositorio>
```

- Reemplaza `<url-del-repositorio>` con la URL de tu repositorio en GitHub. Puedes encontrar esta URL en la página de tu repositorio en GitHub, en el botón "Code".

### 3. **Hacer Commit de los Cambios**

Antes de poder hacer un `push`, asegúrate de que tus cambios están preparados y confirmados (committed). Si no has hecho esto, sigue estos pasos:

1. **Añadir Cambios al Área de Preparación (Staging Area):**

   ```bash
   git add <archivo>
   ```

   O para añadir todos los archivos modificados:

   ```bash
   git add .
   ```

2. **Hacer Commit de los Cambios:**

   ```bash
   git commit -m "Mensaje descriptivo del commit"
   ```

### 4. **Hacer Push de los Cambios**

Con los cambios confirmados y el repositorio remoto configurado, ahora puedes subir tus cambios al repositorio en GitHub. Usa el siguiente comando:

```bash
git push origin <rama>
```

- `origin` es el nombre del repositorio remoto por defecto.
- `<rama>` es la rama en la que deseas hacer el `push` (por ejemplo, `main` o `master`).

**Ejemplo:**

Para hacer `push` de la rama `main`, usa:

```bash
git push origin main
```

### 5. **Autenticación**

Dependiendo de tu configuración, es posible que se te pida que ingreses tu nombre de usuario y contraseña de GitHub, o que utilices un token de acceso personal en lugar de la contraseña. Si usas autenticación de dos factores, necesitarás usar un token de acceso en lugar de tu contraseña.

### 6. **Verifica el Push**

Después de realizar el `push`, puedes verificar que tus cambios se han subido correctamente:

- **En GitHub:** Navega a tu repositorio en GitHub y verifica que los cambios estén reflejados.
- **Desde la Línea de Comandos:** Usa el comando `git log` para ver los commits recientes y asegurarte de que tus cambios están registrados.

### **Resumen de Comandos**

1. Configura el repositorio remoto (si es necesario):

   ```bash
   git remote add origin <url-del-repositorio>
   ```

2. Añadir archivos al área de preparación:

   ```bash
   git add <archivo>
   ```

3. Hacer commit de los cambios:

   ```bash
   git commit -m "Mensaje descriptivo del commit"
   ```

4. Hacer push al repositorio remoto:

   ```bash
   git push origin <rama>
   ```

### 1. **Verificar el Historial de Commits**

```bash
git log
```
- **Descripción:** Muestra el historial de commits en tu repositorio local. Te permite ver los cambios que has confirmado hasta ahora.

### 2. **Añadir un Repositorio Remoto**

```bash
git remote add origin https://github.com/KlerithX2/liga-justicia.git
```
- **Descripción:** Configura el repositorio remoto llamado `origin` con la URL proporcionada. Esto permite que tu repositorio local se comunique con el repositorio en GitHub.

### 3. **Cambiar el Nombre de la Rama Principal**

```bash
git branch -M main
```
- **Descripción:** Cambia el nombre de la rama actual a `main`. Este comando se usa comúnmente si la rama principal del repositorio local tiene un nombre diferente (como `master`) y deseas renombrarla a `main` para coincidir con las convenciones actuales.

### 4. **Hacer Push Inicial a la Rama Principal**

```bash
git push -u origin main
```
- **Descripción:** Realiza el `push` de la rama `main` al repositorio remoto `origin`. El `-u` (o `--set-upstream`) establece la rama `main` en el repositorio remoto como la rama de seguimiento para tu rama local `main`. Esto significa que en futuros `push` y `pull`, Git sabrá que debes hacer estos cambios en la rama `main` del repositorio remoto `origin`.

### 5. **Hacer Push Subsecuente**

```bash
git push
```
- **Descripción:** Envía los commits locales al repositorio remoto. Dado que ya has configurado el repositorio remoto y la rama de seguimiento con el comando anterior, este comando simplemente envía los cambios a la rama `main` del repositorio `origin`.

### Flujo Completo de Configuración y Push

1. **Inicializa tu repositorio local y añade tus archivos.**
2. **Configura el repositorio remoto en GitHub.**
3. **Renombra la rama principal local (si es necesario).**
4. **Haz el `push` inicial para subir tus cambios a GitHub.**
5. **Realiza `push` futuros para subir cambios adicionales.**

### Ejemplo Completo

Aquí tienes un flujo de trabajo completo con estos comandos:

```bash
# Verifica los commits locales
git log

# Configura el repositorio remoto
git remote add origin https://github.com/KlerithX2/liga-justicia.git

# Renombra la rama principal (si es necesario)
git branch -M main

# Realiza el push inicial
git push -u origin main

# Realiza push futuros para enviar nuevos commits
git push
```