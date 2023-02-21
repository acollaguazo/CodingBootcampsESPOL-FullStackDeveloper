[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Gestor de paquetes NPM
<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Npm-logo.svg/800px-Npm-logo.svg.png"  alt="Banner NPM" width="75%"/>
</p>
## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Propósito de NPM](#proposito_npm)
    - [Dependencias](#dependencia)
  - [Aspectos de NPM](#aspecto_npm)
  - [Propósito de package.json](#proposito_pjson)
- [Parte práctica](#practica)
  - [Instalación de NPM](#instalacion)
    - [Instalación local](#local)
    - [Instalación global](#global)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

Cuando se trata de lenguajes que usan módulos y paquetes, como JavaScript, generalmente se necesita una herramienta llamada administrador de paquetes.
<a name="proposito_npm"> </a>

### 🟠 Propósito de NPM

Un administrador de paquetes es un conjunto de herramientas que se utilizan para manejar módulos y paquetes que contienen dependencias. Un administrador de paquetes automatiza el proceso de búsqueda, instalación, actualización, configuración, mantenimiento y eliminación de paquetes para un programa de computadora.
A veces también se le conoce como sistema de gestión de paquetes. Los administradores de paquetes generalmente están conectados y mantienen una base de datos de dependencias e información de versiones para los paquetes en un repositorio.

<a name="dependencia"> </a>

#### 🔹 Dependencias

Las dependencias son código, generalmente en forma de bibliotecas y paquetes, que se llaman y reutilizan en un programa. Entonces, por ejemplo, supongamos que está desarrollando un nuevo módulo y llama a una función contenida en otro módulo escrito por usted, que llama a otro módulo escrito por otra persona, que llama a otro módulo escrito por ese tercero. El módulo que está escribiendo es "dependiente" de todos esos otros módulos.

<p align="center">
  <img src="https://cdn-icons-png.flaticon.com/512/2689/2689634.png" alt="Dependencia" width="50%">
</p>

<a name="aspecto_npm"> </a>

### 🟠 Aspectos de NPM

Node Package Manager, generalmente abreviado como NPM, es el administrador de paquetes predeterminado para el motor de tiempo de ejecución de Node.js. NPM tiene dos funciones: 
  + NPM proporciona una interfaz de línea de comandos que permite a los usuarios publicar y descargar paquetes.
  + NPM se comporta como un depósito en línea de paquetes JavaScript binarios.

<a name="proposito_pjson"> </a>

### 🟠 Propósito de package.json

Todos los paquetes de NPM requieren un archivo llamado "package.json" que debe estar ubicado en el directorio raíz del proyecto. NPM usa los metadatos en el archivo package.json para determinar todas las dependencias en un paquete.
  + Este archivo contiene los metadatos de identificación del proyecto en forma de pares clave-valor que, como mínimo, identifican el nombre del proyecto y el número de versión del proyecto.

  ```json
  {
     "name" : "thisProject",
     "version" : "0.0.0",
  }
  ```
<a name="practica"> </a>

## 💻 Parte práctica

<a name="instalacion"> </a>

### 🟠 Instalación de NPM

Hay dos formas en que NPM puede instalar paquetes: local o globalmente.
<a name="local"> </a>

#### 🔹 Instalación local

+ Querrá usar la instalación local si está instalando un paquete que desea usar dentro de su aplicación.
+ La instalación local es el comportamiento predeterminado de npm.
+ Ejecute el comando de instalación local desde el directorio en el que desea instalar el paquete.
Para instalar el paquete node_modules localmente, use la interfaz de línea de comandos de NPM.

```
npm install <package_name>
```

Este comando crea un directorio llamado node_modules con el paquete y sus dependencias en su directorio de trabajo actual.

<a name="global"> </a>

#### 🔹 Instalación global

+ Una instalación global significa que todas las aplicaciones en la máquina en la que está instalado el paquete pueden usar ese código.
+ Las instalaciones globales deben usarse con prudencia porque todos los proyectos en esa computadora harán uso de ese paquete y sus dependencias.
+ Si tiene diferentes versiones de un proyecto en su máquina, todas usarán el paquete instalado globalmente, lo que podría romper la compatibilidad con otras dependencias.
Para instalar node_modules para que cualquier aplicación en la máquina pueda acceder al paquete, lo que significa que se instalan globalmente, use el comando:

```
npm install -g <package_name>
```

Es el mismo comando que el comando de instalación local pero agrega la opción -g.


<a name="referencias"></a>

## Referencias

* What is npm?. Retrieved February 13, 2023, from https://www.w3schools.com/whatis/whatis_npm.asp
* npm Docs. Retrieved 13 February 2023, from https://docs.npmjs.com/