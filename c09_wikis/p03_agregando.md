# Agregando referencias entre páginas en la wiki

Para agregar referencias entre páginas en una wiki de GitHub, puedes usar enlaces internos que facilitan la navegación y mantienen la integridad del contenido, incluso si cambian las URLs.

### Pasos para Agregar Referencias Internas:

1. **Identificar el Nombre de la Página**: Cada página en la wiki tiene un nombre que se utiliza para crear el enlace. Por ejemplo, si la página se llama `Contact`, usaremos este nombre para crear el enlace.

2. **Editar el Contenido**: Abre la página en la que deseas agregar el enlace y edita el contenido.

3. **Crear un Enlace Interno**:
   - Selecciona el texto al que deseas añadir el enlace (por ejemplo, "Escríbame aquí").
   - Usa la sintaxis de Markdown para crear el enlace:
     ```markdown
     [Escríbame aquí](Contact)
     ```
   - **Vista Previa**: Puedes usar la función de vista previa para asegurarte de que el enlace funciona correctamente.

4. **Guardar los Cambios**: Una vez que estés satisfecho con los cambios, guarda la página.

### Ejemplo Práctico:

Supongamos que tienes una página principal (`Home`) y quieres agregar un enlace a la página de contacto (`Contact`). Puedes hacerlo de la siguiente manera:

```markdown
# Bienvenido a mi proyecto

Para mayor información, [escríbame aquí](Contact).
```

### Organizar el Menú de Navegación:

Si quieres personalizar la barra lateral (sidebar) para organizar las páginas de la wiki de una manera específica, puedes hacerlo creando un archivo `custom sidebar`. Este archivo te permite ordenar las páginas como desees y agruparlas bajo diferentes secciones.

1. **Crear un Archivo `custom sidebar`**:
   - Ve a la página de la wiki y selecciona la opción para crear un archivo personalizado para la barra lateral.
   - Puedes ordenar las páginas alfabéticamente o en el orden que prefieras.
   
   Ejemplo de un archivo `custom sidebar`:

   ```markdown
   # Menú Principal
   - [Home](Home)
   - [Información](Contact)
   - [Instalaciones](Installation)
   ```

2. **Visualizar el Menú Personalizado**: Después de guardar los cambios, la barra lateral reflejará la nueva estructura que hayas definido.

### Consejos Adicionales:

- **Evita Cambiar Nombres de Páginas**: Una vez que hayas compartido URLs o enlaces internos, trata de no cambiar los nombres de las páginas, ya que esto romperá los enlaces existentes.
- **Usa el Buscador**: La wiki tiene un buscador incorporado que facilita la navegación entre las diferentes páginas, especialmente cuando el número de páginas crece.
- **Documentación Extensiva**: Puedes elevar la wiki a un nivel más profesional, usándola como la documentación oficial de tu proyecto.

Con estos pasos, puedes crear una wiki bien estructurada y fácil de navegar, mejorando la experiencia del usuario y facilitando el acceso a la información relevante.