# Diferentes formas de agregar archivos al escenario

### Comandos Usados y su Propósito

#### 1. `git init`
- **Propósito:** Inicializar un nuevo repositorio de Git.
- **Uso:**
  ```sh
  git init
  ```
  Esto crea una carpeta `.git` en el directorio actual (`02-BASES`), iniciando un nuevo repositorio.

#### 2. `git status`
- **Propósito:** Ver el estado actual del repositorio.
- **Uso:**
  ```sh
  git status
  ```
  Esto muestra los archivos modificados, añadidos, eliminados y no rastreados en el repositorio.

#### 3. `git add index.html main.html`
- **Propósito:** Añadir archivos específicos al área de preparación.
- **Uso:**
  ```sh
  git add index.html main.html
  ```
  Esto añade `index.html` y `main.html` al área de preparación, preparándolos para el próximo commit.

#### 4. `git reset index.html main.html`
- **Propósito:** Retirar archivos específicos del área de preparación.
- **Uso:**
  ```sh
  git reset index.html main.html
  ```
  Esto retira `index.html` y `main.html` del área de preparación, deshaciendo el `git add` previo para esos archivos.

#### 5. `git add *.html`
- **Propósito:** Añadir todos los archivos `.html` del directorio actual al área de preparación.
- **Uso:**
  ```sh
  git add *.html
  ```
  Esto añade todos los archivos con extensión `.html` del directorio actual al área de preparación.

#### 6. `git commit -m "archivos html añadidos"`
- **Propósito:** Crear un commit con los cambios en el área de preparación.
- **Uso:**
  ```sh
  git commit -m "archivos html añadidos"
  ```
  Esto crea un commit con el mensaje "archivos html añadidos", incluyendo todos los cambios en el área de preparación.

#### 7. `git add js/*.js`
- **Propósito:** Añadir archivos `.js` específicos en el subdirectorio `js` al área de preparación.
- **Uso:**
  ```sh
  git add js/*.js
  ```
  Esto añade todos los archivos con extensión `.js` en el subdirectorio `js` al área de preparación.

#### 8. `git commit -m "Archivos js"`
- **Propósito:** Crear un commit con los cambios en el área de preparación.
- **Uso:**
  ```sh
  git commit -m "Archivos js"
  ```
  Esto crea un commit con el mensaje "Archivos js", incluyendo todos los cambios en el área de preparación.

#### 9. `git add uploads/.gitkeep`
- **Propósito:** Añadir un archivo específico al área de preparación.
- **Uso:**
  ```sh
  git add uploads/.gitkeep
  ```
  Esto añade el archivo `.gitkeep` en el subdirectorio `uploads` al área de preparación.

#### 10. `git commit -m "Carpeta uploads"`
- **Propósito:** Crear un commit con los cambios en el área de preparación.
- **Uso:**
  ```sh
  git commit -m "Carpeta uploads"
  ```
  Esto crea un commit con el mensaje "Carpeta uploads", incluyendo todos los cambios en el área de preparación.

#### 11. `git add css/`
- **Propósito:** Añadir todos los archivos en el subdirectorio `css` al área de preparación.
- **Uso:**
  ```sh
  git add css/
  ```
  Esto añade todos los archivos en el subdirectorio `css` al área de preparación.

#### 12. `git commit -m "Estilos agregados"`
- **Propósito:** Crear un commit con los cambios en el área de preparación.
- **Uso:**
  ```sh
  git commit -m "Estilos agregados"
  ```
  Esto crea un commit con el mensaje "Estilos agregados", incluyendo todos los cambios en el área de preparación.

#### 13. `git add .`
- **Propósito:** Añadir todos los archivos modificados y no rastreados en el directorio actual y sus subdirectorios al área de preparación.
- **Uso:**
  ```sh
  git add .
  ```
  Esto añade todos los archivos modificados y no rastreados en el directorio actual y sus subdirectorios al área de preparación.

#### 14. `git commit -m "Fonts e Images agregadas"`
- **Propósito:** Crear un commit con los cambios en el área de preparación.
- **Uso:**
  ```sh
  git commit -m "Fonts e Images agregadas"
  ```
  Esto crea un commit con el mensaje "Fonts e Images agregadas", incluyendo todos los cambios en el área de preparación.

### Flujo Completo de Comandos

```sh
# Inicializar un nuevo repositorio de Git
git init

# Ver el estado actual del repositorio
git status

# Añadir archivos HTML específicos al área de preparación
git add index.html main.html

# Ver el estado del repositorio
git status

# Retirar archivos HTML específicos del área de preparación
git reset index.html main.html

# Ver el estado del repositorio
git status

# Añadir todos los archivos HTML al área de preparación
git add *.html

# Ver el estado del repositorio
git status

# Crear un commit con los archivos HTML añadidos
git commit -m "archivos html añadidos"

# Añadir archivos JS específicos al área de preparación
git add js/*.js

# Crear un commit con los archivos JS añadidos
git commit -m "Archivos js"

# Añadir un archivo específico en uploads al área de preparación
git add uploads/.gitkeep

# Crear un commit con la carpeta uploads añadida
git commit -m "Carpeta uploads"

# Añadir todos los archivos en el subdirectorio css al área de preparación
git add css/

# Crear un commit con los archivos CSS añadidos
git commit -m "Estilos agregados"

# Añadir todos los archivos modificados y no rastreados al área de preparación
git add .

# Crear un commit con todos los cambios añadidos
git commit -m "Fonts e Images agregadas"
```

### Conclusión

Estos comandos permiten un control detallado sobre qué archivos se incluyen en cada commit, asegurando que los cambios se registren de manera lógica y organizada. Este flujo de trabajo es útil para mantener un historial de commits claro y conciso, facilitando la colaboración y el seguimiento de cambios en el proyecto.