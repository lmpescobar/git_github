# Warning - Pulling without reconcile strategy

Al realizar un `git pull`, es posible que recibas advertencias si Git no puede determinar automáticamente cómo debe fusionar los cambios remotos con los locales. Una forma de evitar estas advertencias es especificar una estrategia de reconciliación para el `pull`.

### **Advertencia al hacer `git pull` sin estrategia de reconciliación**

La advertencia típica que puedes ver es algo como:

```
Warning: Pulling without specifying how to reconcile divergent branches is discouraged.
```

Esta advertencia ocurre cuando Git no sabe cómo debe manejar los cambios divergentes entre la rama local y la remota. Para evitar estas advertencias, puedes configurar una estrategia de `pull`.

### **Configurar `git pull` para usar `fast-forward only`**

El modo `fast-forward only` asegura que el `git pull` solo avance la rama si no hay cambios locales que entren en conflicto. Si Git detecta divergencias que requieren una fusión, abortará el `pull` y te pedirá que manejes la situación manualmente.

1. **Configura la estrategia `fast-forward only` globalmente:**

   ```bash
   git config --global pull.ff only
   ```

   - Esta configuración asegura que todos los futuros `git pull` en cualquier repositorio utilicen esta estrategia de reconciliación.

2. **Editar la Configuración Global (`--global`) con tu Editor:**

   ```bash
   git config --global -e
   ```

   - Este comando abre el archivo de configuración global en tu editor de texto predeterminado. Aquí puedes revisar o editar configuraciones como la estrategia de `pull`, el nombre de usuario, el correo electrónico, etc.

### **Revisión de Cambios y Repositorios Remotos**

Después de configurar la estrategia de `pull`, puedes continuar trabajando normalmente:

1. **Haz `pull` para obtener los últimos cambios:**

   ```bash
   git pull
   ```

   - Ahora, Git usará la estrategia `fast-forward only` automáticamente.

2. **Verifica el historial de commits:**

   ```bash
   git log
   ```

   - Este comando muestra el historial de commits. Puedes usarlo para revisar los cambios que se han fusionado en tu rama.

3. **Verifica las URLs de los remotos configurados:**

   ```bash
   git remote -v
   ```

   - Esto te muestra las URLs de los remotos, útil para asegurarte de que estás trabajando con el repositorio correcto.

### **Resumen**

Configurando `git pull` con `fast-forward only`, te aseguras de que Git no intente fusionar automáticamente cambios que podrían causar conflictos. En cambio, si hay cambios que requieren una fusión, Git te avisará y podrás manejarlos manualmente. Esta es una forma segura de mantener la integridad de tu historia de commits.