1. Preparando un repositorio para viajes en el tiempo
2. Viajes en el tiempo, resets y reflog

### **1. Inicializar un Repositorio y Hacer Varios Commits**

- **Inicializar un nuevo repositorio:**
  ```bash
  git init
  ```
  Esto crea un nuevo repositorio Git en el directorio actual.

- **Agregar y confirmar archivos progresivamente:**
  ```bash
  git add README.md
  git commit -m "Readme agregado"
  
  git add misiones.md
  git commit -m "Agregamos misones.md"
  
  git add heroes.md
  git commit -m "Agregamos heroes.md"
  
  git add ciudades.md
  git commit -m "Agregamos ciudades"
  
  git add historia/
  git commit -m "Agregamos la carpeta historia"
  ```
  Estos comandos agregan y confirman varios archivos y directorios, creando un historial de commits que refleja el progreso de tu proyecto.

### **2. Modificar el Último Commit**

- **Modificar el último commit:**
  ```bash
  git commit --amend
  ```
  Esto permite cambiar el mensaje del commit más reciente o agregar/retirar archivos de él. Es útil si cometiste un error en el commit anterior.

- **Ver el historial de commits:**
  ```bash
  git log
  ```
  Aquí puedes revisar cómo luce el historial después de los cambios.

- **Hacer un nuevo commit con cambios en `heroes.md`:**
  ```bash
  git commit -am "Heroes.md: Agregamos a linterna verde"
  ```
  Este comando hace un commit con un cambio en `heroes.md`, confirmando tanto los cambios existentes como el nuevo mensaje.

### **3. Viajar en el Tiempo con `reset` y `reflog`**

#### **3.1. Retroceder al Estado de un Commit Anterior**

- **Ver el historial de commits:**
  ```bash
  git log
  ```
  Antes de retroceder, verifica los commits con `git log` para identificar el hash del commit al que deseas volver.

- **Hacer un `reset --soft` a un commit anterior:**
  ```bash
  git reset --soft 13240c3
  ```
  Este comando mueve `HEAD` a un commit anterior (identificado por el hash `13240c3`), pero mantiene los cambios en el área de preparación (staged). Esto te permite hacer un nuevo commit con esos cambios.

- **Ver el estado del repositorio:**
  ```bash
  git status
  ```
  Esto muestra los archivos que aún están en el área de preparación, listos para un nuevo commit.

- **Hacer un nuevo commit:**
  ```bash
  git commit -am "Heroes.md: Robin y Linterna verde"
  ```
  Aquí se confirma nuevamente los cambios con un mensaje actualizado.

#### **3.2. Cambiar el Tipo de `reset` para Modificar el Estado del Repositorio**

- **Usar `reset --mixed` para retroceder y deshacer cambios en el área de preparación:**
  ```bash
  git reset --mixed db37df0
  ```
  Este comando retrocede `HEAD` al commit especificado y deshace los cambios en el área de preparación (volviéndolos a `unstaged`), pero mantiene los cambios en el directorio de trabajo.

- **Verificar el historial de commits:**
  ```bash
  git log
  ```
  Muestra el historial después del `reset`.

- **Usar `reset --hard` para un retroceso completo:**
  ```bash
  git reset --hard db37df0
  ```
  Esto no solo mueve `HEAD` al commit anterior, sino que también borra cualquier cambio en el área de preparación y el directorio de trabajo, dejándolos exactamente como estaban en ese commit.

- **Continuar usando `reset --hard` para revertir a otros commits:**
  ```bash
  git reset --hard 8c87e15
  git reset --hard HEAD^
  ```
  Estos comandos mueven el estado del repositorio a un commit anterior específico o al commit anterior al actual (`HEAD^`).

#### **3.3. Restaurar un Estado Anterior con `reflog`**

- **Usar `reflog` para ver todos los movimientos de `HEAD`:**
  ```bash
  git reflog
  ```
  Esto muestra un historial de todas las acciones que han movido `HEAD`, incluyendo los `reset`, `checkout`, y `amend`.

- **Restaurar un estado anterior utilizando `reset --hard` con un hash de `reflog`:**
  ```bash
  git reset --hard 1ee019b
  ```
  Utilizando el hash de un estado anterior mostrado por `reflog`, puedes restaurar el repositorio a ese estado exacto.

### **Resumen de Comandos y Funcionalidad:**

1. **`git commit --amend`**: Modifica el último commit (mensaje y/o archivos).
2. **`git reset --soft <hash>`**: Mueve `HEAD` a un commit anterior y deja los cambios en el área de preparación.
3. **`git reset --mixed <hash>`**: Retrocede `HEAD` y mueve los cambios a no preparados (unstaged).
4. **`git reset --hard <hash>`**: Retrocede `HEAD` y elimina los cambios tanto del área de preparación como del directorio de trabajo.
5. **`git reflog`**: Muestra todos los movimientos de `HEAD` para restaurar estados anteriores.
6. **`git reset --hard <reflog hash>`**: Restaura el estado del repositorio a un punto previo identificado en `reflog`.

Estos comandos te permiten manipular el historial de Git con precisión, restaurar estados anteriores, y corregir errores sin perder datos importantes.