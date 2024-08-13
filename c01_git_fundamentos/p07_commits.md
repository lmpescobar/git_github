# Demostración de la creación, puesta en escena y commits

### **Flujo de trabajo de Git**

1. **Agregar todos los archivos al área de preparación (staging):**
   ```bash
   git add .
   ```
   Este comando agrega todos los archivos y cambios en el repositorio al área de preparación, preparando los cambios para ser confirmados (commit).

2. **Sacar un archivo específico del área de preparación:**
   ```bash
   git reset README.md
   ```
   Este comando elimina `README.md` del área de preparación, por lo que no será incluido en el próximo commit, aunque los cambios realizados en el archivo siguen existiendo en el directorio de trabajo.

3. **Agregar todos los archivos nuevamente al área de preparación:**
   ```bash
   git add .
   ```
   Este paso es repetido para asegurarte de que todos los archivos excepto `README.md` estén en la zona de staging.

4. **Crear un commit:**
   ```bash
   git commit -m "Readme agregado"
   ```
   Este comando crea un commit con un mensaje que indica que se ha agregado `README.md`, aunque este archivo no fue incluido en el commit debido al `git reset` anterior.

5. **Deshacer cambios en el directorio de trabajo:**
   ```bash
   git checkout -- .
   ```
   Este comando deshace cualquier cambio no confirmado en el directorio de trabajo, restaurando los archivos a su estado en el último commit.

6. **Agregar y confirmar todos los cambios de una vez:**
   ```bash
   git commit -am "Readme atualizado"
   ```
   Aquí, el flag `-a` le indica a Git que debe agregar automáticamente todos los archivos rastreados (excepto los nuevos archivos no rastreados) al área de preparación y hacer un commit con el mensaje especificado.

7. **Revisar el historial de commits:**
   ```bash
   git log
   ```
   Este comando muestra el historial de commits en el repositorio, proporcionando detalles sobre cada commit, como el autor, la fecha y el mensaje del commit.

### **Resumen del flujo:**

- **`git add .`**: Prepara todos los archivos para el commit.
- **`git reset README.md`**: Saca `README.md` de la preparación.
- **`git commit -m "Readme agregado"`**: Confirma los cambios, pero sin incluir `README.md`.
- **`git checkout -- .`**: Deshace cualquier cambio no confirmado en el directorio de trabajo.
- **`git commit -am "Readme atualizado"`**: Agrega todos los archivos rastreados y los confirma en un solo paso.
- **`git log`**: Revisa el historial de commits.

Este flujo muestra cómo gestionar de manera efectiva la puesta en escena y los commits en Git, permitiéndote un control granular sobre los archivos y sus versiones.