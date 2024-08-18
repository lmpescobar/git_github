# GitHub Issues

En esta sección, vamos a explorar cómo utilizar la herramienta de **Issues** en GitHub para gestionar y organizar el trabajo en tu repositorio. Asegúrate de estar en el repositorio correcto, es decir, el tuyo y no el mío.

## **Acceso a Issues**

1. **Acceder a Issues:**
   - Dirígete a tu repositorio en GitHub.
   - Haz clic en la pestaña **Settings**.
   - En la barra lateral de opciones, busca **Issues**. Si la opción está desactivada, puedes activarla aquí para empezar a crear y gestionar Issues.

2. **Visibilidad y Filtros:**
   - De forma predeterminada, se mostrarán todos los Issues abiertos. Puedes utilizar los filtros para ver Issues cerrados, buscar por etiquetas, o ver Issues asociados a milestones específicos.
   - Para buscar Issues específicos, puedes ingresar el índice del Issue, por ejemplo, `#1`, `#2`, etc. Esto te ayudará a encontrar rápidamente Issues por su número.

3. **Creación de Issues:**
   - Para crear un nuevo Issue, haz clic en **New Issue**.
   - Llena el título y la descripción. Puedes utilizar Markdown para formatear tu texto y añadir imágenes o archivos adjuntos.
   - Puedes también asignar el Issue a colaboradores específicos, añadir etiquetas, y asociarlo con un milestone.

   Ejemplo:
   - **Título:** Falta un personaje en la lista de Avengers
   - **Descripción:** Por favor agregar a Nick Fury a la lista de los Avengers. Esto es importante para completar el equipo.

4. **Asignación y Etiquetas:**
   - **Asignación:** Puedes asignar el Issue a uno o varios colaboradores que trabajarán en él. Esto les enviará una notificación.
   - **Etiquetas (Labels):** Usa etiquetas para categorizar los Issues, como `bug`, `enhancement`, etc.
   - **Milestones:** Puedes asociar Issues a milestones para seguir el progreso hacia objetivos específicos.

5. **Relación con Pull Requests:**
   - Puedes vincular Issues con Pull Requests. Si un Issue se resuelve con un Pull Request, puedes hacer referencia al Issue en el mensaje del Pull Request. Por ejemplo, `fixes #1` en el mensaje de commit cerrará automáticamente el Issue número 1 cuando se haga el merge del Pull Request.

6. **Cierre de Issues:**
   - Cuando un Issue se resuelve, puedes marcarlo como cerrado. Esto se hace fácilmente haciendo clic en **Close Issue**.
   - Recuerda que puedes usar palabras clave en los mensajes de commit para cerrar Issues automáticamente cuando se integren cambios relevantes.

## **Resumen**

La gestión de Issues es esencial para mantener un proyecto organizado y asegurar que todos los problemas y solicitudes sean documentados y atendidos. Utiliza las herramientas de filtrado, asignación y etiquetado para mantener un control efectivo sobre el progreso de tu proyecto.