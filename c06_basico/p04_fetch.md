# Git Fetch

`git fetch` es un comando que se utiliza para actualizar tu repositorio local con los cambios del repositorio remoto sin fusionarlos automáticamente con tu rama local. Es una forma segura de ver qué cambios se han realizado en el repositorio remoto sin afectar tu trabajo actual.

Cómo usar `git fetch` y cómo se integra con otros comandos como `git pull`:

### **1. Ejecutar `git fetch`**

El comando `git fetch` descarga los cambios desde el repositorio remoto pero no los fusiona con tu rama actual. Esto te permite revisar los cambios antes de integrarlos.

```bash
git fetch
```

### **2. Verificar el log de commits**

Después de hacer un `git fetch`, puedes revisar el log de commits para ver qué cambios se han descargado del repositorio remoto. Estos cambios están en las ramas remotas y no en tu rama local todavía.

```bash
git log
```

Esto muestra el historial de commits de tu rama actual.

### **3. Hacer un Pull (opcional)**

Si decides que deseas integrar los cambios descargados en tu rama local, puedes usar `git pull`. `git pull` realiza un `fetch` y luego hace una fusión (`merge`) de los cambios en tu rama actual.

```bash
git pull
```

### **4. Verificar el log de commits después de `git pull`**

Después de hacer un `git pull`, puedes verificar el log de commits nuevamente para ver cómo se han integrado los cambios del repositorio remoto en tu rama local.

```bash
git log
```

### **Resumen de Comandos**

1. **Descargar los cambios del repositorio remoto:**
    ```bash
    git fetch
    ```

2. **Verificar el historial de commits:**
    ```bash
    git log
    ```

3. **Fusionar los cambios del repositorio remoto en tu rama actual (opcional):**
    ```bash
    git pull
    ```

4. **Verificar el historial de commits después de la fusión:**
    ```bash
    git log
    ```

### **Flujo de Trabajo Típico**

1. **Usa `git fetch`** para obtener los cambios del remoto sin modificar tu rama actual. Esto es útil para ver qué ha cambiado en el repositorio remoto y revisar los commits en las ramas remotas.

2. **Revisa el log de commits** para decidir si quieres integrar esos cambios.

3. **Usa `git pull`** si decides fusionar esos cambios en tu rama actual.

4. **Revisa el log de commits nuevamente** para confirmar que la fusión se realizó como esperabas.

Este enfoque te da control sobre cuándo y cómo integrar los cambios del repositorio remoto, evitando sorpresas y conflictos inesperados.