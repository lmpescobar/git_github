# Actualizar mensaje del commit y revertir commits

### **1. Actualizar el Mensaje de un Commit Reciente**

- **Hacer un commit inicial:**
  ```bash
  git commit -am "Instalaciones actualiz"
  ```
  Este comando hace un commit con los cambios actuales y los prepara con `-a`, pero con un mensaje incorrecto ("Instalaciones actualiz").

- **Revisar el historial de commits:**
  ```bash
  git log
  ```
  Esto te permite ver el historial de commits y verificar el mensaje incorrecto.

- **Actualizar el mensaje del commit más reciente:**
  ```bash
  git commit --amend -m "Instalaciones actualizadas"
  ```
  Este comando modifica el último commit, actualizando su mensaje a "Instalaciones actualizadas". `--amend` permite realizar cambios en el commit más reciente, tanto en el mensaje como en los archivos incluidos.

- **Verificar el cambio en el historial:**
  ```bash
  git log
  ```
  Ahora, el `log` mostrará el commit con el mensaje actualizado.

- **Modificar el mensaje nuevamente:**
  ```bash
  git commit --amend -m "Notas añadidas a las instalaciones"
  ```
  Este comando realiza otro ajuste al mensaje del mismo commit, cambiando el mensaje a "Notas añadidas a las instalaciones".

- **Revisar el historial nuevamente:**
  ```bash
  git log
  ```
  El historial ahora reflejará el mensaje del commit actualizado.

### **2. Revertir Commits Utilizando `git reset`**

- **Revertir al commit anterior (manteniendo los cambios):**
  ```bash
  git reset --soft HEAD^
  ```
  Este comando mueve el puntero de `HEAD` al commit anterior, dejando los cambios del commit revertido en el área de preparación. Es decir, deshace el commit pero mantiene los cambios listos para ser confirmados nuevamente.

- **Revisar el estado del repositorio:**
  ```bash
  git status
  ```
  Esto te mostrará que los cambios del commit revertido están en el área de preparación, listos para ser confirmados.

- **Verificar el historial de commits:**
  ```bash
  git log
  ```
  Ahora verás que el commit revertido ya no aparece en el historial.

- **Volver a confirmar los cambios:**
  ```bash
  git add .
  git commit -m "Notas añadidas de nuevo a las instalaciones"
  ```
  Este comando hace un nuevo commit con los mismos cambios que habías revertido, pero ahora con un nuevo mensaje.

- **Revisar el historial de commits nuevamente:**
  ```bash
  git log
  ```
  Ahora verás el nuevo commit con el mensaje "Notas añadidas de nuevo a las instalaciones".

### **Resumen de Comandos y Funcionalidad:**

1. **`git commit --amend -m "nuevo mensaje"`**: Modifica el mensaje (y los archivos si es necesario) del commit más reciente.
2. **`git reset --soft HEAD^`**: Revierte al commit anterior, manteniendo los cambios del commit revertido en el área de preparación.
3. **`git log`**: Revisa el historial de commits.
4. **`git add .` y `git commit -m "mensaje"`**: Confirma nuevamente los cambios revertidos con un nuevo mensaje.

### **Consideraciones Importantes:**
- **`git commit --amend`** es útil para corregir errores en el commit más reciente, pero ten en cuenta que altera el historial, lo que puede causar problemas si ya has compartido ese commit con otros.
- **`git reset --soft HEAD^`** te permite deshacer un commit sin perder los cambios realizados, dándote la oportunidad de modificarlos o simplemente confirmar nuevamente con un mensaje diferente.

Estos comandos te proporcionan flexibilidad para ajustar tus commits y mantener un historial de Git limpio y coherente.