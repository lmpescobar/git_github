# Introducción al git rebase

### **Introducción a Git Rebase**

`Git rebase` es una poderosa herramienta en Git que se utiliza para mover o combinar una secuencia de commits a una nueva base. Se puede considerar como una manera de "revolver" o "reordenar" la historia del commit, lo que permite mantener un historial de commits más limpio y lineal. 

#### **¿Qué es `git rebase`?**
- **Rebase** es el proceso de trasladar o aplicar commits desde una rama sobre otra.
- A diferencia de `git merge`, que une dos ramas y crea un commit de fusión, `git rebase` mueve los commits de una rama en la parte superior de otra, lo que resulta en un historial lineal.
- Esto es especialmente útil para limpiar el historial antes de fusionar ramas, evitando los commits de fusión y manteniendo una historia más sencilla.

#### **Cuándo usar `git rebase`**

- **Integrar cambios recientes de `master`**: Si estás trabajando en una rama de características (feature branch) y `master` ha avanzado, puedes hacer un `rebase` para que tu trabajo esté encima de la versión más reciente de `master`.
- **Limpiar el historial de commits**: Si tu historial tiene muchos commits pequeños y desordenados, `rebase` interactivo (`git rebase -i`) permite combinar o reordenar esos commits para crear un historial más limpio y legible.
- **Evitar commits de fusión innecesarios**: A diferencia de `merge`, `rebase` no crea un commit de fusión, lo que ayuda a mantener el historial de commits más lineal y claro.

#### **Ejemplo básico de `git rebase`**

Imagina que tienes dos ramas: `master` y `feature`. La rama `feature` tiene algunos commits que no están en `master`. Si quieres mover los commits de `feature` encima de los commits más recientes de `master`, harías lo siguiente:

```bash
git checkout feature
git rebase master
```

Esto hace que los commits en `feature` se apliquen encima de los commits más recientes en `master`. Ahora, el historial de `feature` parece como si hubiera comenzado desde la cabeza de `master`.

#### **Rebase interactivo**

Un `rebase` interactivo te permite modificar commits antes de aplicarlos:

```bash
git rebase -i HEAD~3
```

Este comando abre un editor donde puedes elegir qué hacer con los últimos 3 commits:
- **Pick**: Deja el commit como está.
- **Squash**: Combina este commit con el anterior.
- **Reword**: Cambia el mensaje del commit.
- **Drop**: Elimina el commit.

#### **Consideraciones y Precauciones**
- **Conflictos**: Al igual que con `merge`, los conflictos pueden surgir durante un `rebase`, y deben ser resueltos antes de continuar.
- **Ramas compartidas**: Nunca hagas un `rebase` en una rama que has compartido con otros, ya que esto reescribe la historia y puede causar problemas para quienes están trabajando en la misma rama.

### **Resumen**

`Git rebase` es una técnica esencial para mantener un historial de commits limpio y manejable. Es útil para integrar cambios de ramas base, limpiar commits desordenados y evitar los commits de fusión. Sin embargo, debe usarse con precaución, especialmente en ramas compartidas, debido a su capacidad de reescribir el historial de commits.