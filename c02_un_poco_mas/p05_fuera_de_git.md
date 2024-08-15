# Cambiar el nombre y eliminar archivos fuera de git

### **1. Verificar el Estado y Confirmar Cambios**
- **Verificar el estado del repositorio:**
  ```bash
  git status
  ```
  Esto muestra los archivos modificados, eliminados o renombrados en tu directorio de trabajo que Git está rastreando.

- **Agregar todos los cambios al área de preparación:**
  ```bash
  git add .
  ```
  Este comando añade todos los cambios (incluyendo renombrados y eliminados) al área de preparación.

- **Verificar nuevamente el estado:**
  ```bash
  git status
  ```
  Esto asegura que todos los cambios han sido correctamente añadidos al área de preparación y están listos para ser confirmados.

- **Hacer un commit con los cambios:**
  ```bash
  git commit -m "Historia de superman renombrada"
  ```
  Este commit guarda los cambios en el historial de commits, reflejando el cambio de nombre de un archivo.

- **Revisar el historial de commits:**
  ```bash
  git log
  ```
  Esto te permite verificar que el commit fue registrado correctamente en el historial.

### **2. Restaurar el Estado del Repositorio con `reset --hard`**
- **Restaurar el repositorio a un commit específico:**
  ```bash
  git reset --hard 33c7c70
  ```
  Este comando mueve `HEAD` al commit especificado (`33c7c70`) y restablece el directorio de trabajo a ese estado exacto, eliminando todos los cambios que se realizaron después de ese commit.

- **Verificar el historial después del `reset`:**
  ```bash
  git log
  ```
  Esto muestra el historial de commits después del `reset`. Los commits que estaban después de `33c7c70` ya no aparecen en el historial.

### **3. Usar `reflog` para Restaurar un Estado Anterior**
- **Ver los movimientos de `HEAD` con `reflog`:**
  ```bash
  git reflog
  ```
  `reflog` muestra todos los movimientos de `HEAD`, permitiéndote ver incluso los commits que fueron descartados por un `reset --hard`.

- **Restaurar el repositorio a un estado anterior utilizando un hash de `reflog`:**
  ```bash
  git reset --hard b0bdf9a
  ```
  Este comando utiliza el hash de un commit identificado en `reflog` para restaurar el repositorio a ese punto específico, incluso si ese commit no aparece en el `log` normal.

- **Verificar el historial después del `reset` con `reflog`:**
  ```bash
  git log
  ```
  Ahora, el historial de commits debería reflejar el estado en el que estaba el repositorio en el momento del commit restaurado.

### **4. Manejar Cambios y Confirmar un Commit Final**
- **Verificar el estado del repositorio:**
  ```bash
  git status
  ```
  Esto muestra si hay archivos modificados o eliminados después de restaurar el repositorio con `reflog`.

- **Agregar todos los cambios al área de preparación:**
  ```bash
  git add .
  ```
  Esto prepara todos los cambios para ser confirmados, incluyendo cualquier archivo eliminado o modificado.

- **Verificar el estado nuevamente:**
  ```bash
  git status
  ```
  Asegúrate de que todos los cambios están listos para el commit.

- **Hacer un commit final:**
  ```bash
  git commit -m "Historia de batman eliminada"
  ```
  Este commit guarda la eliminación de `historia de batman` en el historial de commits.

- **Revisar el historial de commits final:**
  ```bash
  git log
  ```
  Ahora, el historial de commits debería reflejar todos los cambios realizados, incluyendo la eliminación de `historia de batman`.

### **Resumen de Comandos y Funcionalidad:**

1. **`git status`**: Muestra el estado del repositorio.
2. **`git add .`**: Agrega todos los cambios al área de preparación.
3. **`git commit -m "mensaje"`**: Confirma los cambios en el historial de commits.
4. **`git reset --hard <hash>`**: Restaura el repositorio a un estado específico, eliminando cambios posteriores.
5. **`git reflog`**: Muestra el historial completo de movimientos de `HEAD`, permitiendo restaurar commits descartados.
6. **`git log`**: Verifica el historial de commits.

Este flujo de trabajo te permite gestionar los cambios en tu repositorio, incluyendo restauraciones y eliminaciones, asegurando que el historial de Git refleje exactamente los estados deseados.