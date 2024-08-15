# Cambiar el nombre y eliminar archivos mediante git

### **1. Realizar un Commit Inicial**
- **Agregar y confirmar todos los archivos:**
  ```bash
  git add .
  git commit -m "Destruir mundo añadido"
  ```
  Esto agrega todos los archivos al área de preparación y realiza un commit con el mensaje "Destruir mundo añadido".

- **Ver el historial de commits:**
  ```bash
  git log
  ```
  Esto muestra el historial de commits, permitiéndote verificar que el commit fue exitoso.

### **2. Renombrar un Archivo**
- **Renombrar un archivo utilizando `git mv`:**
  ```bash
  git mv destruir-mundo.md salvar-mundo.md
  ```
  Este comando renombra el archivo `destruir-mundo.md` a `salvar-mundo.md`.

- **Ver el estado del repositorio:**
  ```bash
  git status
  ```
  Esto muestra que el archivo ha sido renombrado y que los cambios están listos para ser confirmados.

- **Confirmar el cambio de nombre:**
  ```bash
  git commit -m "Destruir mundo renombrado"
  ```
  Este commit guarda el cambio de nombre en el historial del repositorio.

- **Verificar el historial de commits:**
  ```bash
  git log
  ```
  Esto te permite ver el historial de commits, incluyendo el cambio de nombre.

### **3. Eliminar un Archivo**
- **Eliminar el archivo `salvar-mundo.md`:**
  ```bash
  git rm salvar-mundo.md
  ```
  Este comando elimina el archivo `salvar-mundo.md` del repositorio.

- **Ver el estado del repositorio:**
  ```bash
  git status
  ```
  Esto muestra que el archivo ha sido eliminado y los cambios están listos para ser confirmados.

- **Revertir cambios con `reset --hard`:**
  ```bash
  git reset --hard
  ```
  Este comando revierte todos los cambios no confirmados en el repositorio, incluyendo la eliminación del archivo. Después de esto, el archivo `salvar-mundo.md` debería reaparecer en tu directorio de trabajo.

- **Eliminar el archivo nuevamente:**
  ```bash
  git rm salvar-mundo.md
  ```
  Como se deshicieron los cambios anteriores, vuelves a eliminar el archivo.

- **Ver el estado del repositorio:**
  ```bash
  git status
  ```
  Verifica que el archivo ha sido eliminado correctamente y que los cambios están listos para ser confirmados.

- **Confirmar la eliminación:**
  ```bash
  git commit -m "Salvar-mundo: eliminado"
  ```
  Este commit guarda la eliminación del archivo en el historial del repositorio.

- **Verificar el historial de commits:**
  ```bash
  git log
  ```
  Muestra el historial de commits, incluyendo la eliminación del archivo.

### **Resumen de Comandos y Funcionalidad:**

1. **`git mv <archivo_actual> <nuevo_nombre>`**: Renombra un archivo en el repositorio.
2. **`git rm <archivo>`**: Elimina un archivo del repositorio.
3. **`git reset --hard`**: Revierte todos los cambios no confirmados, restaurando el estado del repositorio al último commit.
4. **`git log`**: Muestra el historial de commits.

Estos comandos te permiten gestionar y revertir cambios en el repositorio de manera eficiente, asegurando que el historial refleje las modificaciones realizadas.