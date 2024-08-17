# Bonus - No hacer esto

git config --global -e

name = Andrew Clark
email = hi@andrewclark.io

git pull

git fetch

git commit -am "Readme actualizado"

git log

git push

git config --global -e

name = Fernando Herrera
email = Klerith@yahoo.com

git config --global -e

La sección "Bonus - No hacer esto" trata sobre cómo cambiar las configuraciones globales de Git para suplantar la identidad de otra persona al hacer commits, lo cual es una práctica poco ética y potencialmente dañina.

### **1. Suplantación de Identidad en Git**

```bash
git config --global -e

name = Andrew Clark
email = hi@andrewclark.io
```

- **Contexto**: Aquí se está configurando el nombre y el correo electrónico globalmente en Git para que los commits aparezcan como si hubieran sido realizados por otra persona, en este caso, "Andrew Clark" con el correo "hi@andrewclark.io".

- **Problema**: Suplantar la identidad de otra persona en los commits puede llevar a problemas graves, como violaciones de políticas de seguridad, pérdida de confianza entre colaboradores, y posibles acciones legales si se hace sin permiso.

### **2. Realizar Commits Bajo una Identidad Falsa**

```bash
git commit -am "Readme actualizado"
```

- **Contexto**: Este commit aparecerá en el historial del repositorio como si lo hubiera realizado "Andrew Clark". Cualquier acción posterior que esté ligada a este commit (como revisiones de código, reportes de bugs, o auditorías) se atribuirá incorrectamente a esa persona.

- **Problema**: Esto genera un rastro de auditoría falso y puede engañar a otros colaboradores o al propietario del repositorio. En entornos profesionales, esto puede tener consecuencias severas.

### **3. Cambiar la Identidad Globalmente Otra Vez**

```bash
git config --global -e

name = Fernando Herrera
email = Klerith@yahoo.com
```

- **Contexto**: Cambiar la identidad global de nuevo para que los commits futuros parezcan hechos por "Fernando Herrera" también es problemático. Esta práctica podría repetirse con diferentes identidades, lo que demuestra una intención deliberada de suplantación.

### **4. Consecuencias de la Suplantación de Identidad en Git**

- **Ética**: Suplantar la identidad de alguien es una falta grave de ética. En proyectos de código abierto o colaborativos, esto puede arruinar relaciones profesionales y dañar tu reputación.
- **Legalidad**: Dependiendo de la jurisdicción, la suplantación de identidad puede ser ilegal y estar sujeta a sanciones.
- **Confianza**: Los sistemas de control de versiones, como Git, se basan en la confianza. Si los commits no son confiables, se compromete la integridad del proyecto.

### **Recomendación**

- **No suplantar identidades**: Es importante ser transparente y usar tu verdadera identidad en los commits. Si estás colaborando en un proyecto, la transparencia ayuda a construir confianza y asegura que el trabajo de todos sea reconocido apropiadamente.
- **Usa tus propias credenciales**: Siempre configura Git con tu propio nombre y correo electrónico. Si necesitas cambiar de identidad entre proyectos (por ejemplo, entre trabajo y proyectos personales), usa configuraciones locales en lugar de globales.

Mantener la integridad y la ética en el uso de herramientas como Git es crucial para un desarrollo de software profesional y colaborativo.