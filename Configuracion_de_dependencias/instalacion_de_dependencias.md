# Instalación de dependencias

- Las **dependencias** son paquetes que vamos a utilizar en nuestro proyecto. 
- Un **paquete** es el conjunto de módulos para resolver un problema. 
 
Saber manejar las dependencias en un proyecto permite `desarrollar la aplicación más rápido sin partir desde cero`.

**Existen tres tipos de dependencias:** 
- Locales
- Desarrollo
- Globales.

## **Qué son las dependencias locales**

Las dependencias locales son aquellas que `son obligatorias para el proyecto`, es decir, son las necesarias para que la aplicación funcione en producción. 

### Cómo instalar dependencias locales

Para instalar una dependencia local, utiliza uno de los siguientes comandos, donde es el nombre del paquete.

```bash
npm install <paquete> 
```

Las dependencias locales se encuentran en el package.json en la propiedad "dependencies", seguido de la versión que fue instalada.

```json
json { ... "dependencies": { "paquete": "1.0.0" } }
```

## **Qué son las dependencias de desarrollo**

Las dependencias de desarrollo son aquellas que `NO son obligatorias para el proyecto`, es decir, sin estas la aplicación servirá. Estas dependencias ofrecen una ayuda para construir código de forma óptima, por ejemplo, formatear el código, agregar estilos, levantar un servidor para observar los cambios.

### Cómo instalar dependencias de desarrollo

Para instalar una dependencia de desarrollo, utiliza el siguiente comando, donde es el nombre del paquete.

```bash
npm install -D <paquete>
```

Las dependencias de desarrollo se encuentran en el package.json en la propiedad "dev-dependencies", seguido de la versión que fue instalada.

```json
json { ... "dev-dependencies": { "paquete": "1.0.0" } }
```

## **Qué son las dependencias globales**

Las dependencias globales son aquellas que `están disponibles para todos los proyectos en tu computador`, pero **no aparecen el archivo de configuración package.json.**

### Cómo instalar dependencias globales

Para instalar una dependencia global, utiliza el siguiente comando, donde es el nombre del paquete.

```bash
npm install -g <paquete>
```

Ten en cuenta que para instalar dependencias globales requiera permisos elevados, esto se soluciona con la palabra reservada sudo en terminales basadas en Unix, o en Windows ejecutando la terminal como administrador.

Las dependencias globales no se encuentran en el package.json, por esta razón recomiendo no abusar de esta herramienta, ya que el archivo de configuración es muy importante para que otros desarrolladores tengan toda la información pertinente al proyecto, incluyendo las dependencias a utilizar.

## **Cómo visualizar los paquetes instalados**

Para ver qué dependencias locales están instaladas, ejecuta el siguiente comando:

```bash
npm list
```

Para ver qué dependencias globales están instaladas, ejecuta uno de los siguientes comandos:

```bash
npm list -g --depth 0
```

Puedes utilizar el flag --depth para indicar la profundidad de dependencias, esto mostrará los paquetes que contiene cada paquete.

```bash
npm list --depth 2
```