# Cambiar nombre de la rama Master a Main

Para cambiar el nombre de la rama predeterminada de `master` a `main` en Git, los comandos que mencionas deben seguir un flujo coherente.

### **Cambiar el nombre de la rama `master` a `main`**

1. **Ver las ramas actuales:**
   ```bash
   git branch
   ```

2. **Cambiar el nombre de la rama `master` a `main`:**
   ```bash
   git branch -m master main
   ```

3. **Verificar que el cambio se haya realizado:**
   ```bash
   git branch
   ```

### **Configuración global para nuevas inicializaciones**

4. **Configurar Git para que use `main` como la rama predeterminada en nuevos repositorios:**
   ```bash
   git config --global init.defaultBranch main
   ```

### **Inicialización de un nuevo repositorio**

5. **Inicializar un nuevo repositorio:**
   ```bash
   git init
   ```

6. **Agregar todos los archivos al área de preparación:**
   ```bash
   git add .
   ```

7. **Hacer el primer commit:**
   ```bash
   git commit -m "Primer commit"
   ```

8. **Verificar el estado del repositorio:**
   ```bash
   git status
   ```

### **Ver y editar la configuración global de Git**

9. **Editar la configuración global de Git:**
   ```bash
   git config --global -e
   ```
   Este comando abre el archivo de configuración global de Git en el editor predeterminado para realizar cambios, si es necesario.

### **Notas adicionales:**

- **`git checkout -- .`**: Este comando deshace los cambios no confirmados en el directorio de trabajo, pero no es necesario en el contexto de cambiar el nombre de la rama.
  
- **Verificación continua:** Utiliza `git status` y `git branch` para revisar el estado y confirmar que la rama `main` es ahora la rama predeterminada.

