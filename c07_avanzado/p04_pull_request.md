# Pull Request

# Cómo Contribuir a un Repositorio en GitHub: Fork, Modificaciones y Pull Request

Este documento explica paso a paso cómo contribuir a un proyecto en GitHub mediante la creación de un *fork*, la realización de modificaciones en tu repositorio local, y la creación de un *pull request* para solicitar que tus cambios sean integrados en el repositorio original.

## 1. Hacer un Fork del Repositorio

Un *fork* es una copia del repositorio original que se encuentra en tu cuenta de GitHub. Esto te permite hacer modificaciones sin afectar el proyecto original.

1. Ve al repositorio del proyecto al que deseas contribuir.
2. Haz clic en el botón **Fork** en la esquina superior derecha de la página.
3. Ahora tendrás una copia del repositorio en tu cuenta de GitHub.

## 2. Clonar el Repositorio Forkeado

Una vez que hayas hecho el *fork*, debes clonar tu repositorio forkeado a tu máquina local para poder trabajar en él.

```bash
git clone https://github.com/tu-usuario/nombre-del-repositorio.git
cd nombre-del-repositorio
```

## 3. Crear una Nueva Rama para tus Modificaciones

Es una buena práctica crear una nueva rama para cada conjunto de cambios que quieras proponer. Esto mantiene tu rama principal (`master` o `main`) limpia.

```bash
git checkout -b nombre-de-tu-rama
```

## 4. Realizar Cambios en el Código

Ahora que estás en tu nueva rama, puedes hacer los cambios que desees. Por ejemplo, supongamos que quieres eliminar un archivo o agregar uno nuevo.

- **Eliminar un archivo:** Si deseas eliminar un archivo, navega a la ubicación del archivo y elimínalo.
- **Agregar un archivo:** Si deseas agregar un nuevo archivo, crea el archivo en la ubicación deseada.

## 5. Hacer un Commit de los Cambios

Después de realizar los cambios, debes hacer un *commit* para guardar esos cambios en tu rama local.

```bash
git add .
git commit -m "Descripción de los cambios realizados"
```

## 6. Subir los Cambios a GitHub

Sube los cambios desde tu máquina local al repositorio en GitHub.

```bash
git push origin nombre-de-tu-rama
```

## 7. Crear un Pull Request

Un *pull request* (PR) es una solicitud para que los mantenedores del proyecto original revisen e integren tus cambios en su repositorio. Para crear un PR:

1. Ve a tu repositorio forkeado en GitHub.
2. Haz clic en el botón **Contribute** y selecciona **Open Pull Request**.
3. Revisa que las ramas base y de comparación estén correctas: la base debe ser la rama principal del repositorio original, y la rama de comparación debe ser la rama en la que trabajaste.
4. Escribe un título y una descripción clara para tu PR. Explica qué cambios has hecho y por qué deberían integrarse.
5. Haz clic en **Create Pull Request**.

## 8. Esperar la Revisión y Responder a los Comentarios

Una vez que crees el PR, los mantenedores del proyecto revisarán tus cambios. Es posible que te hagan preguntas o te pidan ajustes. Si es así, realiza los cambios solicitados en tu rama local y empuja los nuevos commits a GitHub; el PR se actualizará automáticamente.

## 9. Fusionar el Pull Request

Si tus cambios son aprobados, el PR será fusionado en el repositorio original, y tus contribuciones serán parte del proyecto. Si eres el dueño del repositorio o tienes permisos de escritura, puedes fusionar el PR tú mismo. De lo contrario, esto lo hará uno de los mantenedores del proyecto.