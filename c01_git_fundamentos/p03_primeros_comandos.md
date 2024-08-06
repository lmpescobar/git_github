### Primeros Comandos de Git

A continuación se describen algunos de los comandos iniciales más importantes de Git, que te ayudarán a configurar y empezar a usar este poderoso sistema de control de versiones.

#### 1. **Verificar la Versión de Git**
```bash
git --version
```
Este comando muestra la versión de Git instalada en tu sistema. Es útil para asegurarte de que tienes Git correctamente instalado y para verificar si necesitas actualizarlo.

#### 2. **Obtener Ayuda en Git**
```bash
git help
```
Este comando muestra una lista de los comandos disponibles en Git y proporciona acceso a la documentación de Git. Es una herramienta útil para familiarizarse con los comandos y opciones disponibles.

#### 3. **Obtener Ayuda Específica sobre un Comando**
```bash
git --help config
```
Este comando muestra la documentación y las opciones disponibles para el comando específico (`config` en este caso). Puedes utilizar este formato con cualquier comando de Git para obtener información detallada sobre su uso.

#### 4. **Configurar el Nombre de Usuario Global**
```bash
git config --global user.name "Luis Escobar"
```
Este comando establece el nombre de usuario global para Git. El nombre de usuario es parte de la configuración que Git utilizará para identificar al autor de los commits. El parámetro `--global` indica que esta configuración se aplicará a todos los repositorios en tu máquina.

#### 5. **Configurar el Correo Electrónico Global**
```bash
git config --global user.email "lmpes@tutanota.com"
```
Este comando establece el correo electrónico global para Git. Similar al nombre de usuario, el correo electrónico se utiliza para identificar al autor de los commits. La configuración global aplica a todos los repositorios en tu máquina.

#### 6. **Editar la Configuración Global**
```bash
git config --global -e
```
Este comando abre tu editor de texto predeterminado para que puedas editar el archivo de configuración global de Git (`.gitconfig`). Aquí puedes ajustar configuraciones adicionales o modificar las existentes.

### Ejemplo de Archivo de Configuración `.gitconfig`
Cuando ejecutas `git config --global -e`, puedes ver un archivo similar a este:

```ini
[user]
    name = Luis Escobar
    email = lmpes@tutanota.com
[core]
    editor = vim
```

En este archivo, puedes agregar o modificar configuraciones según tus necesidades.

### Conclusión

Estos comandos básicos de Git son esenciales para comenzar a usar Git de manera efectiva. Configurar tu nombre de usuario y correo electrónico garantiza que tus commits estén correctamente identificados, mientras que los comandos de ayuda y configuración proporcionan la base para explorar más a fondo las capacidades de Git. Una vez que te sientas cómodo con estos comandos iniciales, podrás avanzar a comandos más complejos y flujos de trabajo avanzados.