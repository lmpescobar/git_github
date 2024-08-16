# Rebase - edit

1. **Verifica el estado actual del repositorio**:
   ```bash
   git status
   ```
   Esto muestra los cambios en el área de preparación y en el directorio de trabajo.

2. **Descarta los cambios en `README.md`**:
   ```bash
   git checkout -- README.md
   ```
   Esto restaura el archivo `README.md` al último estado confirmado, descartando cambios no guardados.

3. **Añade todos los cambios al área de preparación**:
   ```bash
   git add .
   ```
   Esto agrega todos los archivos modificados y nuevos al área de preparación para el próximo commit.

4. **Crea un commit con un mensaje descriptivo**:
   ```bash
   git commit -m "commits"
   ```
   Esto confirma los cambios que han sido añadidos al área de preparación con el mensaje "commits".

5. **Muestra el historial de commits**:
   ```bash
   git log
   ```
   Esto muestra la lista de commits anteriores.

6. **Inicia un rebase interactivo de los últimos 3 commits**:
   ```bash
   git rebase -i HEAD~3
   ```
   Esto abre un editor para modificar los últimos 3 commits. Puedes elegir reordenar, combinar o editar commits.

7. **Verifica el estado después del rebase interactivo**:
   ```bash
   git status
   ```
   Muestra el estado del repositorio después de las operaciones de rebase.

8. **Reinicia el estado del índice al commit anterior**:
   ```bash
   git reset HEAD^
   ```
   Esto deshace el último commit, manteniendo los cambios en el área de trabajo.

9. **Añade el archivo `villanos.md` al área de preparación**:
   ```bash
   git add villanos.md
   ```
   Prepara el archivo `villanos.md` para un nuevo commit.

10. **Verifica el estado del repositorio**:
    ```bash
    git status
    ```
    Muestra los archivos en el área de preparación y en el directorio de trabajo.

11. **Crea un nuevo commit con un mensaje específico**:
    ```bash
    git commit -m "Agregamos a deadshot"
    ```
    Esto confirma los cambios en `villanos.md` con el mensaje "Agregamos a deadshot".

12. **Crea otro commit con un mensaje diferente**:
    ```bash
    git commit -am "Misiones actualizadas"
    ```
    Esto añade todos los archivos modificados y confirmados con el mensaje "Misiones actualizadas". 

13. **Muestra el historial de commits nuevamente**:
    ```bash
    git log
    ```
    Verifica los commits después de hacer los nuevos cambios.

14. **Verifica el estado del repositorio después de los nuevos commits**:
    ```bash
    git status
    ```
    Muestra el estado actual después de los nuevos commits.

15. **Continúa con el rebase después de resolver conflictos (si los hubo)**:
    ```bash
    git rebase --continue
    ```
    Finaliza el rebase interactivo, aplicando los cambios pendientes.

16. **Verifica el historial de commits nuevamente después del rebase**:
    ```bash
    git log
    ```
    Muestra el historial actualizado después de completar el rebase.

17. **Cambia a la rama `master`**:
    ```bash
    git checkout master
    ```
    Cambia a la rama principal del repositorio.

18. **Muestra el historial de commits en la rama `master`**:
    ```bash
    git log
    ```
    Verifica el historial de commits en la rama `master`.

Este flujo de trabajo muestra cómo usar Git para gestionar commits y realizar un rebase interactivo para ajustar el historial de cambios.