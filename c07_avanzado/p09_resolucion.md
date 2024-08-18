# Resolución de la tarea

A continuación, se describen los pasos para completar la tarea y asegurarte de que todo esté configurado correctamente en tu repositorio.

#### 1. **Inicializar el Repositorio Local y Hacer el Primer Commit**

1. **Abre tu terminal en Visual Studio Code** o cualquier otra terminal de tu elección.
2. Navega a tu directorio del proyecto, por ejemplo:
   ```bash
   cd /ruta/a/tu/directorio/11_Avenger
   ```
3. Inicializa el repositorio local:
   ```bash
   git init
   ```
4. Crea un archivo `.gitignore` y añade las reglas necesarias.
5. Agrega todos los archivos al repositorio:
   ```bash
   git add .
   ```
6. Realiza el primer commit:
   ```bash
   git commit -m "Primer commit - Proyecto inicializado"
   ```

#### 2. **Renombrar la Rama Principal y Subir al Repositorio Remoto**

1. Renombra la rama principal de `master` a `main`:
   ```bash
   git branch -m master main
   ```
2. Conéctate al repositorio remoto en GitHub:
   ```bash
   git remote add origin https://github.com/tu_usuario/nuevo_repositorio.git
   ```
3. Sube la rama `main` al repositorio remoto:
   ```bash
   git push -u origin main
   ```

#### 3. **Crear y Subir un Tag**

1. **Crear un Tag Anotado:**
   ```bash
   git tag -a v0.01 -m "Versión alfa"
   ```
   - `-a` crea un tag anotado.
   - `-m` añade un mensaje al tag.

2. **Subir el Tag al Repositorio Remoto:**
   ```bash
   git push origin v0.01
   ```

3. **Verificar el Tag en GitHub:**
   - Accede a tu repositorio en GitHub.
   - Ve a la sección de "Tags" para confirmar que el tag `v0.01` está presente.

#### 4. **Opcional: Marcar el Tag como un Release**

1. En tu repositorio en GitHub, ve a la sección de "Releases".
2. Haz clic en "Draft a new release".
3. Selecciona el tag `v0.01` y añade una descripción, como "Versión alfa 0.01".
4. Publica el release.

#### Resumen

- **Inicializa el repositorio local y haz un primer commit.**
- **Renombra la rama principal a `main` y súbela a GitHub.**
- **Crea un tag anotado y súbelo al repositorio remoto.**
- **Opcionalmente, marca el tag como un release en GitHub.**