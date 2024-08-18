# Cerrar issue mediante un commit

### Pasos para Cerrar un Issue mediante un Commit

1. **Identifica el Número del Issue:**
   - En el ejemplo, el número del issue es 5. Asegúrate de tener el número correcto del issue que quieres cerrar.

2. **Realiza los Cambios en tu Proyecto:**
   - Abre tu proyecto en tu editor de código, como Visual Studio Code.
   - Haz los cambios necesarios para resolver el issue. En el ejemplo, se elimina a Capitán Marvel.

3. **Guarda y Realiza un Commit con Referencia al Issue:**
   - Asegúrate de que todos tus cambios están guardados.
   - Abre tu terminal y navega a tu repositorio.
   - Escribe un mensaje de commit que incluya una referencia al issue. Utiliza una de las siguientes palabras clave para cerrar automáticamente el issue:
     - `Fixes #5`
     - `Fix #5`
     - `Closes #5`
   - Tu mensaje de commit puede ser algo como:
     ```bash
     git commit -m "Fixes #5: Borré a Capitán Marvel"
     ```
   - Alternativamente, puedes usar `--amend` para modificar el último commit si es necesario:
     ```bash
     git commit --amend -m "Fixes #5: Borré a Capitán Marvel"
     ```

4. **Sube los Cambios al Repositorio Remoto:**
   - Una vez que hayas hecho el commit, sube los cambios al repositorio remoto:
     ```bash
     git push
     ```

5. **Verifica el Cierre Automático del Issue:**
   - Regresa a GitHub y navega a la sección de "Issues".
   - Verás que el issue número 5 está cerrado automáticamente y asociado con el commit que hiciste.

6. **Revisa los Detalles del Commit:**
   - Puedes hacer clic en el número del issue para ver los detalles del commit que lo cerró. Esto te llevará a la vista del commit donde puedes verificar los cambios realizados.

### Beneficios de Este Método

- **Automatización:** Cerrar un issue automáticamente mediante un commit ahorra tiempo y evita errores manuales.
- **Rastreo:** Mantiene un historial claro de qué commits resolvieron qué issues, facilitando el seguimiento del progreso y la resolución de problemas.
- **Documentación:** El mensaje de commit proporciona un contexto adicional sobre qué se hizo para resolver el issue.

### Consejos Adicionales

- **Feature Branches:** En proyectos más grandes, es una buena práctica trabajar en un branch separado para cada feature o bug fix y luego hacer un pull request.
- **Revisión de Mensajes:** Asegúrate de que el mensaje de commit sea claro y útil para que otros colaboradores entiendan la solución.