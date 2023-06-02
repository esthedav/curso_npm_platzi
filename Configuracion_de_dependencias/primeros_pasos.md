## Crea un directorio

Desde una terminal o línea de comandos, crea un directorio con el nombre de tu proyecto. Después, como buena práctica, inicia un repositorio local de Git dentro de la carpeta creada.

## Terminal

Una vez creado el espacio correspondiente al proyecto de JavaScript. Deberás tener un archivo de configuración llamado package.json.
Cómo estructurar un archivo de configuración package.json

El archivo package.json es un archivo de configuración que contiene la información más importante de tu proyecto como: datos específicos, dependencias, dependencias de desarrollo y archivos de ejecución.

Este archivo, como su extensión lo indica, está estructurado en formato `JSON` (JavaScript Object Notation) que sirve para una mejor lectura e interpretación para los usuarios y las máquinas.
Datos específicos del archivo package.json

Los datos específicos ayudan a identificar el proyecto y actúan como una base para que los usuarios y los contribuidores obtengan información sobre el proyecto.

El archivo package.json estaría estructurado inicialmente por las siguientes propiedades:

```json
    "name": Indica el nombre del proyecto.
    "version": Indica la versión del proyecto.
    "description": Indica una breve descripción del proyecto.
    "main": Indica el archivo principal del proyecto.
    "scripts": Indica los comandos a ejecutar del proyecto (no te preocupes por el comando test por ahora).
    "keywords": Indica las palabras clave del proyecto.
    "author": Indica el nombre y dirección de correo electrónico del propietario del proyecto.
    "license": Indica la licencia del proyecto.
```

**Aunque puedes crear el archivo de configuración manualmente**, NPM te ayuda a crearlo rápidamente mediante el comando npm init. Este comando te permite ingresar los datos específicos del proyecto y genera el archivo package.json en tu directorio.

### Comando `-y`

El comando npm init --yes o npm init -y te ayudará a crear un archivo package.json de manera rápida con una configuración por defecto, sin la necesidad de ingresar los datos.

Para establecer esta configuración por defecto, necesitarás utilizar el comando npm config set init-<atributo>.

De esta manera ya estás listo para gestionar dependencias de tu proyecto con NPM.