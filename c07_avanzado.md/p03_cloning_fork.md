# Cloning y Fork

El flujo de trabajo que describes implica clonar un repositorio, realizar cambios, y luego subir esos cambios de nuevo al repositorio en GitHub.

### **1. Clonar un Repositorio**
Clonar un repositorio crea una copia exacta del repositorio en tu máquina local.

```bash
git clone https://github.com/lmpescobar/git_github.git
```

- Este comando descarga el repositorio completo desde GitHub a tu máquina local. La URL especifica el origen del repositorio.

### **2. Revisar el Historial de Commits**
Después de clonar, puedes revisar el historial de commits para entender el trabajo previo en el repositorio.

```bash
git log
```

- Este comando muestra el historial de commits en el repositorio, incluyendo mensajes de commit, fechas y autores.

### **3. Realizar Cambios y Commit**
Realizas cambios en los archivos locales y luego los confirmas (commit) para agregarlos al historial del repositorio.

```bash
git commit -am "Readme actualizado"
```

- El `-a` indica que todos los archivos modificados deben ser incluidos en el commit, y `-m` te permite añadir un mensaje de commit directamente.

### **4. Subir Cambios al Repositorio en GitHub**
Una vez que has realizado los cambios y los has confirmado, puedes subirlos a tu repositorio en GitHub.

```bash
git push
```

- Este comando envía tus commits locales al repositorio remoto (en GitHub).

### **5. Verificar los Remotos Configurados**
Es importante asegurarse de que tu repositorio esté apuntando al origen correcto. Esto es especialmente relevante si estás trabajando con forks.

```bash
git remote -v
```

- Este comando lista las URLs de los repositorios remotos asociados con tu repositorio local. Verás algo como esto:
  
  ```
  origin  https://github.com/lmpescobar/git_github.git (fetch)
  origin  https://github.com/lmpescobar/git_github.git (push)
  ```

### **Fork vs. Clone**
- **Fork**: Se utiliza cuando no tienes permisos de escritura en el repositorio original y deseas proponer cambios. El fork crea una copia del repositorio en tu cuenta de GitHub.
- **Clone**: Clonar un repositorio lo copia a tu máquina local para que puedas trabajar en él. Clonas tanto repositorios propios como forks.

### **Consideraciones Adicionales**
- Si has hecho un fork de un repositorio, puedes sincronizarlo con el original añadiendo un remoto adicional (usualmente llamado `upstream`) y trayendo cambios desde allí.
  
  ```bash
  git remote add upstream https://github.com/original_owner/original_repo.git
  git fetch upstream
  git merge upstream/main
  ```

- Siempre verifica que estás enviando cambios al repositorio correcto, especialmente cuando trabajas con forks, para evitar confusión.

Este flujo es básico para cualquier desarrollador que trabaje con Git y GitHub, asegurando que puedas colaborar de manera efectiva en proyectos distribuidos.