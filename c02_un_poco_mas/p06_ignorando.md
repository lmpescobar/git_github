# Ignorando archivos que no deseamos

### **Contenido del archivo `.gitignore`:**
El archivo `.gitignore` en la imagen tiene el siguiente contenido:

```
dist/
node_modules/
*.log
```

### **Qué significa esto:**
1. **`dist/`**: Ignora todo el directorio `dist` y su contenido.
2. **`node_modules/`**: Ignora todo el directorio `node_modules` y su contenido.
3. **`*.log`**: Ignora todos los archivos con la extensión `.log`.

### **Pasos a seguir para ignorar archivos:**
1. **Ver el estado actual del repositorio:**
   ```bash
   git status
   ```
   Este comando te muestra los archivos que están siendo rastreados por Git, así como aquellos que están listos para ser añadidos al área de preparación.

2. **Agregar el archivo `.gitignore` al área de preparación:**
   ```bash
   git add .gitignore
   ```
   Esto agrega el archivo `.gitignore` al área de preparación para que pueda ser confirmado.

3. **Confirmar el archivo `.gitignore`:**
   ```bash
   git commit -m ".gitignore agregado"
   ```
   Con esto, el archivo `.gitignore` queda guardado en el historial de commits, y a partir de ahora, los archivos y directorios especificados en él serán ignorados por Git.

### **Posibles causas por las que `git status` aún muestra los archivos:**
- **Archivos ya rastreados**: Si Git ya está rastreando estos archivos (por ejemplo, si `dist/`, `node_modules/`, o `*.log` ya fueron añadidos y confirmados antes de crear el archivo `.gitignore`), necesitarás dejar de rastrearlos explícitamente.
  
  Para ello, puedes usar:
  ```bash
  git rm -r --cached dist/ node_modules/ *.log
  ```
  Esto eliminará los archivos y carpetas del índice de Git (dejando los archivos en tu sistema de archivos) y los deshará del control de versiones.

- **Asegúrate de que el `.gitignore` esté en el directorio correcto**: Si colocas el archivo `.gitignore` en el lugar equivocado, es posible que Git no lo esté aplicando a los archivos correctos. Debe estar en el directorio raíz del proyecto o en el directorio relevante para las reglas que definas.

Después de ejecutar el `git rm -r --cached` y confirmar los cambios, `git status` debería reflejar que los archivos en `dist/`, `node_modules/`, y cualquier archivo `.log` ya no están siendo rastreados, y no deberían aparecer en futuros estados.