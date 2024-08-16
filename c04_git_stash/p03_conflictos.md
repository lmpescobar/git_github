# Conflictos con el stash

### **Manejo de Conflictos con el Stash**

1. **Guardar cambios no confirmados en el stash**:
   ```bash
   git stash
   ```
   - Este comando guarda tus cambios no confirmados en un stash y limpia tu área de trabajo.

2. **Hacer un commit**:
   ```bash
   git commit -am "Readme Actualizado: Titulo"
   ```
   - Confirmas los cambios que has realizado, creando un nuevo commit con la actualización del título en el archivo `Readme`.

3. **Ver el historial de commits**:
   ```bash
   git log
   ```
   - Revisa que el commit se haya añadido correctamente al historial.

4. **Aplicar el stash más reciente**:
   ```bash
   git stash pop
   ```
   - Esto intenta aplicar los cambios del stash a tu directorio de trabajo. Si los cambios en el stash afectan las mismas partes del código que el commit reciente, Git generará un conflicto.

5. **Resolver el conflicto**:
   - Si se produce un conflicto, Git te indicará qué archivos tienen conflictos. Necesitarás abrir esos archivos y resolver manualmente los conflictos siguiendo las marcas de Git (`<<<<<<`, `======`, `>>>>>>`).

6. **Confirmar los cambios después de resolver el conflicto**:
   ```bash
   git commit -am "Merge con el stash"
   ```
   - Después de resolver los conflictos, confirmas los cambios. Esto completa la fusión del stash con el trabajo actual.

7. **Ver el historial de commits**:
   ```bash
   git log
   ```
   - Verifica que el commit con la resolución del conflicto se haya añadido correctamente al historial.

8. **Guardar nuevamente los cambios en el stash**:
   ```bash
   git stash
   ```
   - Si haces más cambios que no quieres confirmar inmediatamente, puedes guardarlos nuevamente en el stash.

9. **Hacer un nuevo commit**:
   ```bash
   git commit -am "Readme updated: Titulo objetivo"
   ```
   - Confirmas los cambios adicionales, asegurando que las nuevas actualizaciones del archivo `Readme` se registren en el historial.

10. **Aplicar el stash más reciente**:
    ```bash
    git stash pop
    ```
    - Intentas aplicar el stash nuevamente. Si los cambios en el stash entran en conflicto con los commits más recientes, deberás resolver los conflictos como antes.

11. **Resolver los conflictos y confirmar**:
    ```bash
    git commit -am "Conflictos en Stash resueltos"
    ```
    - Una vez que hayas resuelto los conflictos, confirmas los cambios, indicando que los conflictos del stash han sido solucionados.

12. **Listar los stashes restantes**:
    ```bash
    git stash list
    ```
    - Esto muestra los stashes restantes, si los hay. Si aplicaste y eliminaste correctamente los stashes con `git stash pop`, esta lista debería estar vacía.

### **Resumen**

Los conflictos con `git stash` ocurren cuando intentas aplicar cambios almacenados en un stash que modifican las mismas partes del código que otros commits recientes. Cuando esto sucede:

- **Resolver manualmente los conflictos**: Identifica y edita los archivos en conflicto.
- **Confirmar los cambios**: Después de resolver los conflictos, asegúrate de confirmar los cambios para mantener tu historial de commits limpio y coherente.
- **Gestionar stashes**: Mantén el control sobre tus stashes, aplicándolos o eliminándolos según sea necesario.

Estos comandos te permiten manejar de forma efectiva los conflictos que pueden surgir cuando utilizas `git stash` en combinación con otras ramas o commits.