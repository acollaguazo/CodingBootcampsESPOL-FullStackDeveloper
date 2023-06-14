[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Middleware
<p align="center">
<img src="https://opengraph.githubassets.com/4f39c1ad8d8ae83d857709a478dc2dd3635688eac13cde10c501784ba871138e/expressjs/morgan" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Third-Party Middlewares](#middleware)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="middleware"> </a>

### 🟠 Third-Party Middlewares

En las aplicaciones se puede usar middleware de terceros para agregar funciones creadas por la comunidad a nuestras aplicaciones Express. Están disponibles como módulos npm que instalamos ejecutando el npm install en la ventana de terminal.

El siguiente ejemplo ilustra la instalación y carga de un middleware de terceros llamado Morganque es un middleware de registro de solicitudes HTTP para Node.js.

```
npm install morgan
```
Después de instalar el módulo que contiene el middleware de terceros, se debe cargar la función de middleware en nuestra aplicación Express como se muestra a continuación:

```js
const express = require('express')
const morgan = require('morgan')

const app = express()

app.use(morgan('tiny'))
```

Aquí estamos cargando la función de middleware morganllamando require()y luego adjuntando la función a nuestras rutas con el use()método de la appinstancia.

<a name="referencias"></a>

## Referencias

* Complete Guide to Express Middleware. Retrieved June 1, 2023, from [https://reflectoring.io/express-middleware/](https://reflectoring.io/express-middleware/)