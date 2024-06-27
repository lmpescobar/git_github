# Primeros comandos de git

### Comandos de Git

1. **Ver la versión de Git instalada**:
   ```sh
   git --version
   ```
   Este comando muestra la versión de Git que está instalada en tu sistema.

2. **Obtener ayuda general sobre Git**:
   ```sh
   git help
   ```
   Este comando muestra una lista de los comandos de Git más comunes y proporciona una breve descripción de cada uno.

3. **Obtener ayuda específica sobre el comando `commit`**:
   ```sh
   git help commit
   ```
   Este comando muestra la documentación detallada sobre el comando `commit`, incluyendo todas las opciones y argumentos que puedes utilizar con `commit`.

4. **Obtener ayuda sobre configuraciones globales de Git**:
   ```sh
   git help config
   ```
   Este comando muestra la documentación detallada sobre el comando `config`, el cual se usa para configurar Git. Aunque `git --help global` no es un comando válido, puedes utilizar `git help config` para obtener información sobre configuraciones globales.

5. **Configurar el nombre de usuario globalmente**:
   ```sh
   git config --global user.name "Luis Miguel"
   ```
   Este comando configura tu nombre de usuario para todos los repositorios de Git en tu máquina.

6. **Configurar el correo electrónico globalmente**:
   ```sh
   git config --global user.email "tuemail@gmail.com"
   ```
   Este comando configura tu correo electrónico para todos los repositorios de Git en tu máquina.

7. **Editar la configuración global de Git en tu editor de texto predeterminado**:
   ```sh
   git config --global -e
   ```
   Este comando abre el archivo de configuración global de Git en tu editor de texto predeterminado, permitiéndote editar directamente el archivo `.gitconfig`.

Estos comandos son útiles para configurar Git y obtener ayuda sobre su uso. La configuración global (`--global`) se aplica a todos los repositorios de Git en tu máquina, mientras que las configuraciones sin `--global` se aplican solo al repositorio en el que estás trabajando.