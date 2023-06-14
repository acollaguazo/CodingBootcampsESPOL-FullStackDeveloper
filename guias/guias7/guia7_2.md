[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Middleware comunes

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Middleware comunes](#middleware_comunes)
  - [Ejemplos de middleware comunes](#ejemplos)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="middleware_comunes"> </a>

### 🟠 Middleware comunes

Antes de Express 4.0, Express incluía Connect, que es el componente que contiene la mayoría del middleware más común. Con Express 4.0, Connect se eliminó de Express. Junto con este cambio, parte del middleware de Connect (body-parser es un ejemplo) se ha movido de Connect a su propio proyecto.
Gran parte del middleware incluido anteriormente con Express es bastante fundamental, por lo que es importante saber "dónde fue" y cómo obtenerlo. Casi siempre querrá Connect, por lo que se recomienda que siempre lo instale junto con Express.

```
npm install --save connect
```
Para tenerlo disponible en su aplicacióm use lo siguiente:

```js
var connect = require(connect);
```

<a name="ejemplos"> </a>

### 🟠 Ejemplos de middleware comunes

#### 🔹 BasicAuth

Proporciona autorización de acceso básica. Tenga en cuenta que la autenticación básica ofrece solo la seguridad más básica, y debe usar la autenticación básica solo a través de HTTPS (de lo contrario, los nombres de usuario y las contraseñas se transmiten sin cifrar).

```js
app.use(connect.basicAuth)();
```

#### 🔹 Body-parser

Middleware de conveniencia que simplemente vincula en json y urlencoded.
```
npm install --save body-parser
```
```js
app.use(require(bbodyparser)());
```

#### 🔹 Compress

Comprime los datos de respuesta con gzip. Esto es algo bueno, y sus usuarios se lo agradecerán, especialmente aquellos con conexiones lentas o móviles.

```js
app.use(connect.compress);
```

#### 🔹 Cookie-parser

Provee soporte de cookie.

```
npm install --save cookie-parser
```
```js
app.use(require(cookieparser)( your secret goes here);
```

#### 🔹 Cookie-session

Proporciona soporte de sesión de almacenamiento de cookies.

```
npm install --save cookie-session
```
```js
app.use(require(cookie-session)());
```

#### 🔹 Static-favicon

Favicon (el icono que aparece en la barra de título de tu navegador). Esto no es estrictamente necesario: simplemente puede poner un favicon.ico en la raíz de su directorio, pero este middleware puede mejorar el rendimiento

```
npm install --save static-favicon
```
```js
require(static-favicon)(path_to_favicon));
```

<p align="center">
<img src="https://dinahosting.com/blog/cont/uploads/2021/05/favicon.jpg" width="70%"/>
</p>


<a name="referencias"></a>

## Referencias

* Utilización del middleware. Retrieved February 21, 2023, from https://expressjs.com/es/guide/using-middleware.html