# Cambios en los archivos


### **1. Inicializar un Repositorio y Hacer el Primer Commit**

- **Inicializar un nuevo repositorio:**
  ```bash
  git init
  ```
  Esto crea un nuevo repositorio Git en el directorio actual.

- **Agregar todos los archivos al área de preparación:**
  ```bash
  git add .
  ```
  Esto agrega todos los archivos y cambios al área de preparación.

- **Hacer el primer commit:**
  ```bash
  git commit -m "Instalaciones.md agregado"
  ```
  Aquí haces un commit con el mensaje especificando que se agregó el archivo `Instalaciones.md`.

### **2. Revisar el Historial y los Cambios**

- **Ver el historial de commits:**
  ```bash
  git log
  ```
  Esto muestra una lista de los commits realizados en el repositorio.

- **Revisar los cambios no preparados (unstaged):**
  ```bash
  git diff
  ```
  Este comando muestra las diferencias entre el estado actual de los archivos y el último commit, es decir, lo que aún no se ha agregado al área de preparación.

### **3. Agregar Cambios Adicionales y Revisarlos**

- **Agregar todos los cambios al área de preparación:**
  ```bash
  git add .
  ```
  Esto mueve los cambios al área de preparación, listos para ser confirmados.

- **Revisar nuevamente las diferencias en los archivos:**
  ```bash
  git diff
  ```
  En este punto, `git diff` mostrará las diferencias entre el último commit y los cambios que aún no se han preparado.

### **4. Revisar Cambios Preparados para Commit**

- **Ver el estado del repositorio:**
  ```bash
  git status
  ```
  Esto muestra cuáles archivos están en el área de preparación, listos para ser confirmados, y cuáles no.

- **Revisar los cambios que ya están en el área de preparación (staged):**
  ```bash
  git diff --staged
  ```
  Este comando muestra las diferencias entre el último commit y los cambios que están en el área de preparación (staged), los cuales se incluirán en el próximo commit.

### **5. Hacer un Commit con los Cambios**

- **Confirmar los cambios preparados:**
  ```bash
  git commit -m "Instalaciones actualizadas"
  ```
  Este commit registra los cambios preparados en el repositorio, con un mensaje que describe la actualización de `Instalaciones.md`.

### **6. Revisar los Cambios Después del Commit**

- **Revisar las diferencias (aunque no debería haber ninguna tras el commit):**
  ```bash
  git diff
  ```
  Después del commit, `git diff` no debería mostrar ninguna diferencia, ya que todos los cambios han sido confirmados.

### **7. Deshacer Cambios en el Directorio de Trabajo**

- **Revertir cambios no confirmados:**
  ```bash
  git checkout -- .
  ```
  Este comando deshace cualquier cambio que no haya sido confirmado, restaurando los archivos al estado del último commit.

### **Resumen de Comandos y Su Funcionalidad:**

1. **`git init`**: Inicializa un nuevo repositorio Git.
2. **`git add .`**: Agrega todos los archivos y cambios al área de preparación.
3. **`git commit -m "mensaje"`**: Realiza un commit con los cambios preparados.
4. **`git log`**: Muestra el historial de commits.
5. **`git diff`**: Muestra las diferencias entre los cambios no preparados y el último commit.
6. **`git diff --staged`**: Muestra las diferencias entre los cambios preparados y el último commit.
7. **`git checkout -- .`**: Revertir todos los cambios no confirmados en el directorio de trabajo.

Estos comandos son fundamentales para gestionar los cambios en tus archivos usando Git, permitiéndote controlar y revisar con precisión qué se está modificando en tu proyecto.