---
remote_theme: pages-themes/architect@v0.2.0
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Routing

<p align="center">
<img src="https://miro.medium.com/v2/resize:fit:653/1*qAwW7MMqk80HNgANpQHGNw.png"  alt="Banner" width="60%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [¿Qué es enrutamiento?](#route)
  - [Express router](#express-router)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="route"> </a>

### 🟠 ¿Qué es enrutamiento?

Es fundamental iniciar entendiendo que es el enrutamiento y a su vez su propósito. Una ruta es una sección de código Express que asocia una operación HTTP (get, post, put, delete) con una ruta de URL y también una función para manejar dicho patrón.

A continuación se describirá las principales acciones para incursionar en el mundo del enrutamiento. Entre los aspectos importantes están:

* **Rutas**

Las rutas son usadas reenviar las solicitudes admitidas (y cualquier información codificada en las URL de solicitud) a las funciones de controlador correspondientes.

* **Controlador**

El controlador funciona para obtener los datos solicitados de los modelos, crea una página HTML que muestra los datos y se los devuelve al usuario para que los vea en el navegador.

* **Vistas**

También conocidas como plantillas son utilizadas por los controladores para representar los datos.

<p align="center">
<img src="https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/routes/mvc_express.png"  alt="Banner" width="60%"/>
</p>

En última instancia, podríamos tener páginas para mostrar listas e información detallada de libros, géneros, autores e instancias de libros, junto con páginas para crear, actualizar y eliminar registros.

<a name="express-router"> </a>

### 🟠 Express router

Existen distintas formas de crear rutas. En este caso hablaremos del middleware [express.Router](https://expressjs.com/en/guide/routing.html#express-router). 
Express Router se usa para crear manejadores de rutas montables y modulares. Además, permite agrupar los controladores de ruta para una parte particular de un sitio y acceder a ellos usando un prefijo de ruta común. Recordemos que los Estos métodos de enrutamiento especifican una función de devolución de llamada (a veces denominada "funciones de controlador") que se activa cuando la aplicación recibe una solicitud para la ruta (punto final) y el método HTTP especificados. En otras palabras, la aplicación "escucha" las solicitudes que coinciden con las rutas y los métodos especificados, y cuando detecta una coincidencia, llama a la función de devolución de llamada especificada.
A continuación, se mostrará un ejemplo de ruta muy básica. 

```js
const express = require('express')
const app = express()

// respond with "hello world" when a GET request is made to the homepage
app.get('/', (req, res) => {
  res.send('hello world')
})
```
En las siguientes secciones describiremos las acciones que convella el enrutamiento:

* Rutas y expressiones regulares
* Manejadores
* Parámetros

<a name="referencias"></a>

## Referencias

* Express Tutorial Parte 4: Rutas y controladores. Retrieved May 12, 2023, from [https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/routes](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/routes)