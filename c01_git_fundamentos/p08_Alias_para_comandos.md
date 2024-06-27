# Creando Alias para nuestros comandos

### Comandos y Alias en Git: Paso a Paso

#### Estado del Repositorio

1. **Primera Imagen:**
   - Estructura de directorios: `02-BASES/` contiene `css`, `fonts`, `images`, `js`, `scss`, `uploads`, `index.html`, y `main.html`.

2. **Segunda Imagen:**
   - El archivo `index.html` ha sido modificado (estado: `M`).

### Comandos y Alias

#### Comandos Iniciales

1. **Ver el estado del repositorio**:
   ```sh
   git status
   ```

2. **Ver el estado del repositorio en formato corto**:
   ```sh
   git status --short
   ```

#### Crear Alias para `git status --short`

3. **Crear un alias para `git status --short`**:
   ```sh
   git config --global alias.s "status --short"
   ```
   Ahora puedes usar `git s` en lugar de `git status --short`.

4. **Usar el nuevo alias**:
   ```sh
   git s
   ```

#### Editar Configuración Global

5. **Editar la configuración global de Git**:
   ```sh
   git config --global -e
   ```
   Esto abre el archivo de configuración global de Git en tu editor de texto predeterminado, permitiéndote ver y editar tus alias y otras configuraciones.

#### Ver el Historial de Commits

6. **Ver el historial de commits**:
   ```sh
   git log
   ```

7. **Ver el historial de commits en una línea por commit**:
   ```sh
   git log --oneline
   ```

8. **Ver el historial de commits con decoración, en todas las ramas, y en formato gráfico**:
   ```sh
   git log --oneline --decorate --all --graph
   ```

#### Crear Alias para `git log`

9. **Crear un alias para un log gráfico y decorado**:
   ```sh
   git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
   ```
   Ahora puedes usar `git lg` para obtener un log gráfico y decorado.

10. **Usar el nuevo alias**:
    ```sh
    git lg
    ```

### Flujo Completo de Comandos

```sh
# Ver el estado del repositorio
git status

# Ver el estado del repositorio en formato corto
git status --short

# Crear un alias para git status --short
git config --global alias.s "status --short"

# Usar el nuevo alias para ver el estado en formato corto
git s

# Editar la configuración global de Git
git config --global -e

# Ver el historial de commits
git log

# Ver el historial de commits en una línea por commit
git log --oneline

# Ver el historial de commits en formato gráfico y decorado
git log --oneline --decorate --all --graph

# Crear un alias para el log gráfico y decorado
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

# Usar el nuevo alias para ver el log gráfico y decorado
git lg
```

### Explicación de Alias

- **Alias `s` para `status --short`**:
  ```sh
  git config --global alias.s "status --short"
  ```
  - **Propósito:** Simplificar la verificación del estado del repositorio en formato corto.
  - **Uso:** `git s`.

- **Alias `lg` para un log gráfico y decorado**:
  ```sh
  git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
  ```
  - **Propósito:** Ver el historial de commits en un formato gráfico y decorado, mostrando todas las ramas.
  - **Uso:** `git lg`.

Estos alias mejoran la eficiencia al trabajar con Git, permitiéndote ejecutar comandos largos y frecuentemente utilizados de manera más rápida y sencilla.