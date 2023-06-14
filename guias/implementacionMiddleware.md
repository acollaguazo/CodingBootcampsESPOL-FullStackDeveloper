[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Implementación

<p align="center">
<img src="https://libreriasjs.com/wp-content/uploads/2023/02/middlewares-1.png" width="60%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Middleware](#odm)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="orm"> </a>

### 🟠 Middleware

Como se mencionaba en la sección introductoria, los middleware son funciones que tienen acceso al objeto de solicitud (req), al objeto de respuesta (res) y a la siguiente función de middleware en el ciclo de solicitud/respuestas de la aplicación. Entre las tareas que realizan están:

* Ejecutar cualquier código.
* Realizar cambios en la solicitud y los objetos de respuesta.
* Finalizar el ciclo de solicitud/respuestas.
* Invocar el siguiente middleware en la pila.

A continuación, se muestra un ejemplo de una aplicación Express simple, “Hola Mundo”, para la que definirá dos funciones de middleware:

```js
var express = require('express');
var app = express();

app.get('/', function (req, res) {
  res.send('Hola Mundo!');
});

app.listen(3000);
```
Ahora un ejemplo simple de una función de middleware denominada “registrador”. Esta función simplemente imprime “REGISTRADO” cuando una solicitud de la aplicación pasa por ella. La función de middleware se asigna a una variable denominada registrador.

```js
var registrador = function (req, res, next) {
  console.log('LOGGED');
  next();
};
```
La llamada a esta función invoca la siguiente función de middleware en la aplicación. La función next() no forma parte de la API de Express o Node.js, pero es el tercer argumento que se pasa a la función de middleware. La función next() puede tener cualquier nombre, pero por convención siempre se denomina “next”. Para evitar confusiones, utilice siempre esta convención.

Para cargar la función de middleware, llame a app.use(), especificando la función de middleware. Por ejemplo, el siguiente código carga la función de middleware registrador antes de la ruta a la vía de acceso raíz (/).

```js
var express = require('express');
var app = express();

var registrador = function (req, res, next) {
  console.log('LOGGED');
  next();
};

app.use(registrador);

app.get('/', function (req, res) {
  res.send('Hola Mundo!');
});

app.listen(3000);
```

<a name="referencias"></a>

## Referencias

* Escritura de middleware para su uso en aplicaciones Express. Retrieved June 2, 2023, from [https://expressjs.com/es/guide/writing-middleware.html](https://expressjs.com/es/guide/writing-middleware.html)