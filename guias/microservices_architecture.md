[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Microservices Architecture

<p align="center">
<img src="https://www.blog.devitpl.com/wp-content/uploads/Application-UI-Server.jpg
" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Microservicios](#comments)
  - [Comunicación entre microservicios](#comment)
  - [Crear una aplicación de microservicio simple con Node.js](#comment)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Microservicios

En el desarollo de nuestra aplicación podemos hacer uso de microservicios, que permite construir componentes de software por separado. Una falla en un componente no afectará la funcionalidad de todo el producto de software.

Los microservicios se hicieron necesarios debido a las deficiencias del patrón monolítico de desarrollo de software. En un microservicio, cada característica de la aplicación de software está separada de las demás, en la mayoría de los casos con sus respectivos servidores y bases de datos. Las aplicaciones creadas con este tipo de arquitectura están débilmente acopladas, también denominadas aplicaciones distribuidas.

<a name="comment"> </a>

### 🟠 Comunicación entre microservicios

La elección de un patrón arquitectónico de microservicio presenta algunos desafíos; uno de ellos es la comunicación de servicio a servicio. Los servicios son una parte débilmente acoplada de una aplicación que, en conjunto, contribuyen al rendimiento general de la aplicación.

Para lograr un rendimiento efectivo, debe haber un medio de comunicación entre los microservicios . En una aplicación de microservicio, la comunicación es posible a través de un protocolo de comunicación entre servicios como HTTP(s), gRPC o agentes de mensajes.

<a name="comment"> </a>

### 🟠 Comunicación HTTP

La comunicación HTTP es un tipo de patrón de comunicación síncrona en el que un servicio depende de otro para realizar.

<p align="center">
<img src="https://blog.logrocket.com/wp-content/uploads/2022/10/http-communication-request-response-diagram.png" width="50%"/>
</p>

<a name="commen"> </a>

### 🟠 Crear una aplicación de microservicio simple con Node.js

```
npm init -y
```

```
npm install express nodemon body-parser
```

* Crea el archivo `server.js` con el siguiente código:

```js
const express = require("express");
const bodyParser = require("body-parser")

const aboutRouter = require("./routes/about");
const weatherRouter = require("./routes/weather");

const PORT = 3000;
const HOST_NAME = "localhost";

const app = express();
app.use(express.static("client"));
app.use(bodyParser.urlencoded({extended: true}));

app.use("/weather", weatherRouter);
app.use("/about", aboutRouter);


app.listen(PORT, HOST_NAME, ()=&gt;{
    console.log(`Server running at ${HOST_NAME}:${PORT}`)
})
```

* En carpeta routes cree dos archivos `about.js` `weather.js`, con el siguiente código:

```js
const express = require("express");
const properties = require("../package.json");

const aboutRoute = express.Router();

aboutRoute.get("/", (req, res)=&gt;{
    const aboutInfo ={
        name: properties.name,
        description: properties.description,
        author: properties.author
    }
    res.json(aboutInfo)
})

module.exports = aboutRoute
```

<a name="referencias"></a>

## Referencias

* Building microservices with Node.js. Retrieved May 12, 2023, from [https://blog.logrocket.com/building-microservices-node-js/](https://blog.logrocket.com/building-microservices-node-js/)