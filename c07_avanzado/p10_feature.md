# Feature Branch - Flujo de trabajo mediante pull request

Este flujo de trabajo con ramas (feature branches) y pull requests es muy útil para mantener un repositorio organizado y permitir un desarrollo más seguro y estructurado.

### Flujo de Trabajo con Feature Branches y Pull Requests

#### 1. **Crear una Nueva Rama**

Antes de empezar a trabajar en una nueva característica o corrección, es importante crear una rama separada de la rama principal (`main` o `master`). Esto ayuda a evitar modificaciones directas en la rama principal y permite un desarrollo paralelo.

```bash
# Crear una nueva rama y cambiar a ella
git checkout -b nombre-de-la-rama
```

#### 2. **Hacer Cambios y Commits**

Realiza los cambios necesarios en la nueva rama. Luego, guarda y registra estos cambios usando `git commit`.

```bash
# Agregar los archivos modificados al staging area
git add .

# Crear un commit con un mensaje descriptivo
git commit -m "Mensaje del commit"
```

#### 3. **Subir la Rama al Repositorio Remoto**

Una vez que los cambios están comprometidos localmente, sube la rama al repositorio remoto para respaldar el trabajo y permitir la colaboración.

```bash
# Subir la rama al repositorio remoto
git push origin nombre-de-la-rama
```

#### 4. **Crear un Pull Request**

Ve a la plataforma de control de versiones (como GitHub, GitLab, etc.) y crea un pull request (PR) para fusionar los cambios de la rama actual con la rama principal (`main`).

1. Navega a la sección de pull requests en tu repositorio.
2. Compara tu rama con la rama `main`.
3. Proporciona una descripción clara del PR y cualquier información relevante.
4. Crea el pull request.

#### 5. **Revisión y Fusión**

El pull request permite a los colaboradores revisar los cambios antes de fusionarlos con la rama principal. Después de la revisión y aprobación, puedes fusionar los cambios.

1. Revisa los comentarios y sugerencias en el PR.
2. Realiza ajustes si es necesario y actualiza el PR.
3. Fusiona el PR una vez aprobado.

#### 6. **Eliminar la Rama**

Después de que la rama ha sido fusionada y ya no es necesaria, puedes eliminarla tanto localmente como en el repositorio remoto.

```bash
# Eliminar la rama localmente
git branch -d nombre-de-la-rama

# Eliminar la rama en el repositorio remoto
git push origin --delete nombre-de-la-rama
```

#### 7. **Actualizar la Rama Principal**

Finalmente, asegúrate de que tu rama principal esté actualizada con los últimos cambios.

```bash
# Cambiar a la rama principal
git checkout main

# Obtener los últimos cambios del repositorio remoto
git pull origin main
```

### Consejos Adicionales

- **Nombrado de Ramas**: Usa nombres descriptivos para tus ramas que reflejen la característica o corrección en la que estás trabajando, como `feature/nueva-caracteristica` o `fix/correccion-bug`.
- **Commits Frecuentes**: Realiza commits frecuentes con mensajes claros y descriptivos para hacer más fácil el seguimiento de los cambios.
- **Resolución de Conflictos**: En caso de conflictos al fusionar ramas, resuélvelos cuidadosamente para mantener la integridad del código.