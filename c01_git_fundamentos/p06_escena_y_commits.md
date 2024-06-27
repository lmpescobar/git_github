# Demostración de la creación, puesta en escena y commits

### Estado Inicial

1. **Primera Imagen:**
   - Estructura de directorios: `01-BASES/` contiene `css`, `fonts`, `images`, `js`, `scss`, `index.html`, y `main.html`.

2. **Segunda Imagen:**
   - Se ha añadido un nuevo archivo `README.md` (estado: `U`, untracked).

3. **Tercera Imagen:**
   - Se ha editado el archivo `README.md` y se ha añadido al área de preparación usando `git add .`.

4. **Cuarta Imagen:**
   - El archivo `README.md` ha sido modificado (estado: `M`).

5. **Quinta Imagen:**
   - Se ejecuta `git checkout -- .`, revirtiendo cambios no confirmados en `README.md`.

### Comandos y Acciones

#### Añadir y Confirmar Archivos

1. **Añadir archivos al área de preparación:**
   ```sh
   git add .
   ```
   - **Efecto:** Todos los archivos modificados y no rastreados se añaden al área de preparación.

2. **Retirar `README.md` del área de preparación:**
   ```sh
   git reset README.md
   ```
   - **Efecto:** `README.md` se retira del área de preparación, volviendo a su estado no rastreado o modificado.

3. **Añadir todos los archivos nuevamente al área de preparación:**
   ```sh
   git add .
   ```
   - **Efecto:** Todos los archivos, incluyendo `README.md`, se añaden nuevamente al área de preparación.

4. **Crear un commit con los cambios añadidos:**
   ```sh
   git commit -m "Readme agregado"
   ```
   - **Efecto:** Se crea un commit con el mensaje "Readme agregado", incluyendo todos los cambios en el área de preparación.

#### Revertir Cambios No Confirmados

5. **Revertir cambios no confirmados en todos los archivos:**
   ```sh
   git checkout -- .
   ```
   - **Efecto:** Todos los cambios no confirmados en el directorio actual y sus subdirectorios se revierten al último estado confirmado.

#### Confirmar Cambios y Ver Historial

6. **Crear un commit que incluye todos los cambios rastreados (modificados y añadidos):**
   ```sh
   git commit -am "Readme actualizado"
   ```
   - **Efecto:** Crea un commit con el mensaje "Readme actualizado" e incluye todos los cambios en archivos rastreados que están en el área de preparación y que han sido modificados.

7. **Ver el historial de commits:**
   ```sh
   git log
   ```
   - **Efecto:** Muestra el historial de commits en el repositorio, permitiéndote ver todos los commits realizados, incluyendo hashes, autores, fechas y mensajes de commit.

### Resumen del Flujo Completo

```sh
# Añadir todos los archivos modificados y no rastreados al área de preparación
git add .

# Retirar README.md del área de preparación
git reset README.md

# Añadir todos los archivos nuevamente al área de preparación
git add .

# Crear un commit con todos los cambios en el área de preparación
git commit -m "Readme agregado"

# Revertir todos los cambios no confirmados en el directorio actual
git checkout -- .

# Crear un commit con todos los cambios rastreados y modificados
git commit -am "Readme actualizado"

# Ver el historial de commits
git log
```

### Conclusión

Estos comandos y acciones te permiten gestionar eficazmente los archivos en tu repositorio, añadiendo, confirmando, y revirtiendo cambios según sea necesario.
