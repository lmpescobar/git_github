# Diferentes formas de agregar archivos al escenario

Formas de agregar archivos al área de preparación en Git, y cómo realizar commits con ellos, utilizando los comandos:

### **1. Inicialización del Repositorio y Estado Inicial**
- **Inicializar un nuevo repositorio:**
  ```bash
  git init
  ```
- **Verificar el estado del repositorio:**
  ```bash
  git status
  ```
  Esto mostrará los archivos no rastreados (untracked files) que no han sido agregados al repositorio.

### **2. Agregar Archivos Específicos al Área de Preparación**
- **Agregar archivos específicos:**
  ```bash
  git add index.html main.html
  ```
  Este comando agrega los archivos `index.html` y `main.html` al área de preparación.

- **Verificar el estado nuevamente:**
  ```bash
  git status
  ```
  Ahora, `index.html` y `main.html` deberían aparecer como archivos en el área de preparación.

### **3. Quitar Archivos del Área de Preparación**
- **Quitar los archivos `index.html` y `main.html` del área de preparación:**
  ```bash
  git reset index.html main.html
  ```
  Este comando saca los archivos del área de preparación, devolviéndolos a su estado no preparado.

- **Verificar el estado nuevamente:**
  ```bash
  git status
  ```

### **4. Agregar Archivos Usando un Patrón (Wildcard)**
- **Agregar todos los archivos `.html`:**
  ```bash
  git add *.html
  ```
  Este comando agrega todos los archivos con la extensión `.html` en el directorio actual al área de preparación.

- **Verificar el estado:**
  ```bash
  git status
  ```

- **Crear un commit para los archivos `.html`:**
  ```bash
  git commit -m "archivos html añadidos"
  ```

### **5. Agregar Archivos en un Subdirectorio**
- **Agregar todos los archivos `.js` en el directorio actual:**
  ```bash
  git add *.js
  ```
  
- **Agregar archivos `.js` dentro de una carpeta específica (por ejemplo, `js/`):**
  ```bash
  git add js/*.js
  ```

- **Crear un commit para los archivos `.js`:**
  ```bash
  git commit -m "Archivos de JS agregados"
  ```

### **6. Agregar Archivos Específicos de Carpeta con Archivos Ocultos**
- **Agregar un archivo específico dentro de la carpeta `uploads/` (por ejemplo, `.gitkeep`):**
  ```bash
  git add uploads/.gitkeep
  ```
  `.gitkeep` es un archivo usado para rastrear directorios vacíos en Git.

- **Crear un commit para el archivo `.gitkeep`:**
  ```bash
  git commit -m "Carpeta uploads añadida"
  ```

### **7. Agregar Todo el Contenido de una Carpeta**
- **Agregar todos los archivos en el directorio `css/`:**
  ```bash
  git add css/
  ```

- **Crear un commit para los estilos:**
  ```bash
  git commit -m "Estilos agregados"
  ```

### **8. Agregar Todos los Archivos Cambiados**
- **Agregar todos los archivos modificados, nuevos y eliminados al área de preparación:**
  ```bash
  git add .
  ```

- **Crear un commit para todos los archivos:**
  ```bash
  git commit -m "Fonts e Imagenes"
  ```

### **Resumen de los Comandos Utilizados**
- **Agregar archivos específicos:** `git add index.html main.html`
- **Agregar usando patrones:** `git add *.html`, `git add js/*.js`
- **Agregar archivos dentro de un subdirectorio:** `git add css/`, `git add uploads/.gitkeep`
- **Agregar todo el contenido del directorio actual:** `git add .`
- **Confirmar los cambios:** `git commit -m "Mensaje del commit"`

Este conjunto de comandos demuestra cómo gestionar y realizar commits de manera eficiente usando diversas opciones para agregar archivos al área de preparación en Git.