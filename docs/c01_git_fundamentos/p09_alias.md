# Creando Alias para nuestros comandos

Crear alias en Git es una forma eficiente de ahorrar tiempo y simplificar comandos largos que usas con frecuencia.

### **1. Ver el Estado del Repositorio**

- **Comando original:**
  ```bash
  git status
  ```

- **Comando con alias para una vista abreviada:**
  ```bash
  git status --short
  ```

- **Crear alias:**
  ```bash
  git config --global alias.s "status --short"
  ```
  Ahora puedes usar `git s` en lugar de `git status --short` para ver el estado abreviado del repositorio.

### **2. Ver el Historial de Commits**

- **Comando original (resumido):**
  ```bash
  git log --oneline
  ```

- **Comando original con más detalles:**
  ```bash
  git log --oneline --decorate --all --graph
  ```

- **Crear un alias avanzado para el log:**
  ```bash
  git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
  ```
  Este alias (`git lg`) muestra el historial de commits en un formato gráfico, incluyendo la decoración de ramas, un resumen de cada commit, y la información del autor.

### **3. Usar los Alias**

- **Ver el estado abreviado del repositorio:**
  ```bash
  git s
  ```
  Esto ejecuta `git status --short`.

- **Ver el historial de commits con el alias `lg`:**
  ```bash
  git lg
  ```
  Esto muestra un log gráfico y decorado con información detallada.

### **Ventajas de Usar Alias en Git:**

- **Ahorro de tiempo:** Te permite escribir comandos más cortos.
- **Personalización:** Puedes adaptar los comandos a tus necesidades.
- **Facilidad de uso:** Alias personalizados facilitan la ejecución de comandos complejos sin necesidad de recordar todos los parámetros.

### **Alias Adicionales Sugeridos:**

- **Alias para agregar y hacer commit de todos los archivos:**
  ```bash
  git config --global alias.ac '!git add . && git commit -m'
  ```
  Ahora puedes usar `git ac "mensaje del commit"` para agregar y hacer commit en un solo paso.

- **Alias para ver las ramas:**
  ```bash
  git config --global alias.br "branch"
  ```
  Usa `git br` para ejecutar `git branch`.

Estos alias te ayudarán a trabajar de manera más eficiente en Git, simplificando tareas comunes y agilizando tu flujo de trabajo.