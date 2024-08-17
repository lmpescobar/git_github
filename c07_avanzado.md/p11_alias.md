# Bonus: Actualizar un Alias

En esta clase, estamos aprendiendo cómo actualizar un alias en Git para hacer más eficiente nuestro flujo de trabajo. Aquí está el proceso detallado:

### Actualización de Alias en Git

1. **Crear un Alias para `git status` con Información Adicional**

   Si deseas que tu alias `git s` también muestre la rama en la que estás trabajando, puedes actualizar el alias de la siguiente manera:

   1. Abre la terminal y edita tu configuración global de Git para añadir o actualizar el alias.
   
   ```bash
   git config --global --edit
   ```

   2. Esto abrirá el archivo de configuración de Git en tu editor predeterminado. Busca la sección `[alias]`. Si ya tienes un alias para `status`, lo verás aquí. Si no, puedes añadirlo.

   3. Añade o actualiza la línea para `s` para que muestre tanto el estado corto como la rama:

   ```ini
   [alias]
       s = status -s -b
   ```

   Aquí, `status -s` proporciona la vista corta del estado y `-b` muestra la rama actual. Puedes usar el alias `s` en lugar de escribir `git status` y `git branch` por separado.

   4. Guarda y cierra el archivo del editor.

2. **Verificar el Alias**

   Ahora, puedes usar tu nuevo alias `git s` para ver el estado y la rama actual en una sola línea. Ejemplo:

   ```bash
   git s
   ```

   Esto debería mostrarte algo similar a:

   ```
   M  archivo.txt
   ## main...origin/main
   ```

   Aquí, `M` indica que el archivo `archivo.txt` ha sido modificado, y `## main...origin/main` muestra que estás en la rama `main`, y que está sincronizada con `origin/main`.

### Recomendaciones

- **Alias Cortos:** Utilizar alias como `s` para `status` puede ahorrar tiempo y mantener tus comandos de Git limpios.
- **Revisar Configuración:** Revisa periódicamente tus alias para asegurarte de que aún se ajustan a tus necesidades y flujo de trabajo.