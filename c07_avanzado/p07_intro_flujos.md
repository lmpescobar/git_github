# Introducción a los Flujos de Trabajo en Git

En el desarrollo colaborativo de software, es esencial manejar eficazmente los flujos de trabajo en Git para asegurar una integración fluida y minimizar conflictos. En esta sección, exploraremos dos enfoques comunes para trabajar en un proyecto compartido utilizando Git: el **flujo de trabajo basado en forks** y el **flujo de trabajo basado en ramas**.

---

#### 1. **Flujo de Trabajo Basado en Forks**

En este enfoque, cada miembro del equipo realiza un fork del repositorio central, clona el repositorio a su máquina local, realiza cambios y, finalmente, envía los cambios a su propio repositorio en GitHub. A continuación, se envían pull requests al repositorio central para integrar los cambios.

**Ventajas:**
- Aislación de los cambios: Cada colaborador trabaja en su propio repositorio sin afectar el repositorio central directamente.
- Control y revisión: Los cambios se pueden revisar antes de ser integrados al repositorio principal.

**Desventajas:**
- **Desincronización**: Puede haber un desfase entre el repositorio central y los forks si no se sincronizan regularmente.
- **Complejidad en la colaboración**: La integración de cambios puede volverse compleja con muchos colaboradores.

---

#### 2. **Flujo de Trabajo Basado en Ramas**

En este enfoque, el repositorio central es utilizado por todo el equipo, y cada miembro crea ramas para trabajar en nuevas características o correcciones. Los cambios se integran al `master` (o `main`) después de ser revisados.

**Pasos a seguir:**

1. **Creación de una Rama:**
   - Cada desarrollador crea una rama para trabajar en una nueva característica o corrección.
   ```bash
   git checkout -b nombre-de-la-rama
   ```

2. **Trabajo en la Rama:**
   - Realiza cambios y confirma los commits en tu rama local.
   ```bash
   git add .
   git commit -m "Mensaje del commit"
   ```

3. **Actualizar el Repositorio Remoto:**
   - Subir los cambios a tu repositorio en GitHub.
   ```bash
   git push origin nombre-de-la-rama
   ```

4. **Revisión y Merge:**
   - Realiza un **pull request** en GitHub para solicitar la integración de los cambios en la rama principal (`master` o `main`). El equipo revisará y discutirá los cambios antes de integrarlos.
   - Alternativamente, puedes hacer un merge de la rama en tu repositorio local.
   ```bash
   git checkout master
   git pull origin master
   git merge nombre-de-la-rama
   git push origin master
   ```

**Ventajas:**
- **Control de Integración**: Permite una revisión y discusión de los cambios antes de su integración al `master`.
- **Menos Conflictos**: Los conflictos se resuelven de forma aislada en las ramas y no afectan el `master` directamente.

**Desventajas:**
- **Complejidad en la Gestión**: Manejar múltiples ramas puede ser complicado, especialmente en equipos grandes.

---

#### **Práctica en Git**

Para ilustrar estos conceptos, realizaremos una serie de pasos prácticos:

1. **Crear una Rama de Característica:**
   ```bash
   git checkout -b feature/nueva-caracteristica
   ```

2. **Realizar Cambios y Confirmar:**
   ```bash
   git add archivo-modificado
   git commit -m "Añadida nueva característica"
   ```

3. **Subir la Rama al Repositorio Remoto:**
   ```bash
   git push origin feature/nueva-caracteristica
   ```

4. **Crear un Pull Request:**
   - En GitHub, navega a la pestaña de Pull Requests y crea uno nuevo desde tu rama hacia `master`.

5. **Revisar y Merge:**
   - Una vez aprobado el pull request, realiza el merge desde la interfaz de GitHub.