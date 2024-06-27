# Cambiar nombre de la rama Master a Main

### Comandos Usados y su Propósito

Aquí tienes una exposición detallada de los comandos de Git que has mencionado, explicando su propósito y el efecto que tienen en el repositorio:

#### 1. `git branch`
- **Propósito:** Listar las ramas locales en el repositorio.
- **Uso:**
  ```sh
  git branch
  ```
  Esto muestra todas las ramas locales existentes en el repositorio y destaca la rama actual con un asterisco (*).

#### 2. `git status`
- **Propósito:** Ver el estado actual del repositorio.
- **Uso:**
  ```sh
  git status
  ```
  Esto muestra los archivos modificados, añadidos, eliminados y no rastreados, así como la rama actual en la que te encuentras.

#### 3. `git branch -m master main`
- **Propósito:** Renombrar una rama.
- **Uso:**
  ```sh
  git branch -m master main
  ```
  Esto renombra la rama `master` a `main` en tu repositorio local.

#### 4. `git config --global init.defaultBranch main`
- **Propósito:** Establecer la rama predeterminada para nuevos repositorios.
- **Uso:**
  ```sh
  git config --global init.defaultBranch main
  ```
  Esto configura Git para que utilice `main` como la rama predeterminada al inicializar nuevos repositorios.

#### 5. `git init`
- **Propósito:** Inicializar un nuevo repositorio de Git.
- **Uso:**
  ```sh
  git init
  ```
  Esto crea un nuevo repositorio de Git en el directorio actual, con `main` como la rama inicial, gracias a la configuración anterior.

#### 6. `git add .`
- **Propósito:** Añadir todos los archivos modificados al área de preparación (staging area).
- **Uso:**
  ```sh
  git add .
  ```
  Esto añade todos los archivos modificados en el directorio actual y sus subdirectorios al área de preparación.

#### 7. `git commit -m "Primer commit"`
- **Propósito:** Crear un commit con los cambios en el área de preparación.
- **Uso:**
  ```sh
  git commit -m "Primer commit"
  ```
  Esto guarda una versión del proyecto con el mensaje "Primer commit", incluyendo todos los cambios en el área de preparación.

#### 8. `git config --global -e`
- **Propósito:** Editar la configuración global de Git en tu editor de texto predeterminado.
- **Uso:**
  ```sh
  git config --global -e
  ```
  Esto abre el archivo de configuración global de Git (`.gitconfig`) en tu editor de texto predeterminado, permitiéndote hacer cambios directamente.

### Flujo Completo

A continuación, se presenta el flujo completo de comandos en el orden en que se utilizaron, junto con su explicación:

```sh
# Listar las ramas locales
git branch

# Ver el estado actual del repositorio
git status

# Listar las ramas locales nuevamente
git branch

# Renombrar la rama 'master' a 'main'
git branch -m master main

# Listar las ramas locales para verificar el cambio
git branch

# Configurar la rama predeterminada para nuevos repositorios
git config --global init.defaultBranch main

# Inicializar un nuevo repositorio de Git
git init

# Añadir todos los archivos modificados al área de preparación
git add .

# Crear un commit con los cambios en el área de preparación
git commit -m "Primer commit"

# Ver el estado actual del repositorio
git status

# Listar las ramas locales para verificar que estamos en 'main'
git branch

# Editar la configuración global de Git
git config --global -e
```

### Resultado Esperado

1. **Renombrar la Rama `master` a `main`**:
   - La rama principal ahora se llama `main`.

2. **Configuración de Rama Predeterminada**:
   - Nuevos repositorios se inicializarán con `main` como la rama predeterminada.

3. **Inicialización y Commit**:
   - Se ha inicializado un nuevo repositorio con `main` como la rama inicial.
   - Todos los archivos del directorio se han añadido y confirmado en el primer commit.

### Consideraciones Adicionales

- **Colaboradores**: Informa a tus colaboradores sobre el cambio de nombre de la rama para que puedan actualizar sus copias locales.
- **Integraciones**: Asegúrate de actualizar cualquier integración (CI/CD, scripts, etc.) que haga referencia a `master`.

Este conjunto de comandos y sus explicaciones proporciona una comprensión clara de cómo renombrar la rama principal, configurar la rama predeterminada para nuevos repositorios, y realizar operaciones básicas de Git.