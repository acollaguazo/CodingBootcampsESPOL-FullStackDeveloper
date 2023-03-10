[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

Configuraci贸n de servidor web con Node.js
=========================================

<p align="center">
<img src="https://pplware.sapo.pt/wp-content/uploads/2016/05/nodejs_04.jpg" width="80%" alt="Banner Node.js"/>
</p>

## Contenido

- [Fundamentos te贸ricos](#fundamentos_teoricos)
  - [Express](#express)
- [Parte pr谩ctica](#practica)
  - [Esqueleto de un proyecto web](#esqueleto)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 馃搼 Fundamentos te贸ricos
===========================

* * *

<a name="express"> </a>

### 馃煚 Express

Express es una infraestructura de aplicaciones web Node.js m铆nima y flexible que proporciona un conjunto s贸lido de caracter铆sticas para las aplicaciones web y m贸viles.

<p align="center">
<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--KkScstnJ--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zojuy79lo3fn3qdt7g6p.png"  alt="Banner NPM" width="70%"/>
</p>


<a name="practica"> </a>

## 馃捇 Parte pr谩ctica
=====================

* * *
<a name="esqueleto"> </a>

Esqueleto de un proyecto web en Node
============================

Para la construcci贸n del sitio web se utilizar谩 el [generador de aplicaciones de express](https://expressjs.com/en/starter/generator.html). En la linea de comandos ejecute las siguientes instrucciones:  

* Instale el **express-generator**, con: `npm i -g express-generator`

* Cree un sitio de prueba llamado **sitio**, con: `express --view=ejs admin`

* La aplicaci贸n generada tendr谩 la siguiente estructura de directorios. 

  <pre><code>
    .
    鈹溾攢鈹? app.js           <b style="background-color: #00aae4;"># Configuraci贸n para la aplicaci贸n que se ejecutar谩 en el servidor</b>
    鈹溾攢鈹? package.json     <b style="background-color: #00aae4;"># M贸dulos de la aplicaci贸n</b>
    鈹溾攢鈹? package-lock.json
    鈹溾攢鈹? bin
    鈹?   鈹斺攢鈹? www          <b style="background-color: #00aae4;"># Punto de arranque de la aplicaci贸n - Lee el archivo app.js</b>
    鈹溾攢鈹? public           <b style="background-color: #00aae4;"># Directorio de archivos est谩ticos</b>
    鈹?   鈹溾攢鈹? images
    鈹?   鈹溾攢鈹? javascripts
    鈹?   鈹斺攢鈹? stylesheets
    鈹?       鈹斺攢鈹? style.css
    鈹溾攢鈹? routes           <b style="background-color: #00aae4;"># Rutas de la aplicaci贸n.</b>
    鈹?   鈹溾攢鈹? index.js
    鈹?   鈹斺攢鈹? users.js
    鈹斺攢鈹? views            <b style="background-color: #00aae4;"># Vistas de la aplicaci贸n por renderizar.</b>
        鈹溾攢鈹? error.ejs
        鈹斺攢鈹? index.ejs
  </code></pre>

* El archivo `app.js` contiene la configuraci贸n para la aplicaci贸n web que se ejecutar谩 en el servidor, con las siguientes partes
  + M贸dulos para la aplicaci贸n web

  <pre><code>
    var createError = require('http-errors');    <b style="background-color: #00aae4;"># Manejo de errores por defecto</b>
    var express = require('express');            <b style="background-color: #00aae4;"># Arquitectura de la aplicaci贸n en backend</b>
    var path = require('path');                  <b style="background-color: #00aae4;"># Manejo de rutas</b>
    var cookieParser = require('cookie-parser'); <b style="background-color: #00aae4;"># Manejo de cookies</b>
    var logger = require('morgan');              <b style="background-color: #00aae4;"># Registro (log) de acciones del servidor</b>
  </code></pre>

  + Referencia a los archivos con las rutas internas 

  <pre><code>
    var indexRouter = require('./routes/index'); <b style="background-color: #00aae4;"># Carga del manejador de subrutas para la ruta index</b>
    var usersRouter = require('./routes/users'); <b style="background-color: #00aae4;"># Carga del manejador de subrutas para la ruta users </b>
  </code></pre> 

  + Instanciaci贸n de la aplicaci贸n

  <pre><code>
    var app = express();
  </code></pre>

  + Vistas (EJS que ser谩n renderizadas en HTML)

  <pre><code>
    // view engine setup
    app.set('views', path.join(__dirname, 'views')); <b style="background-color: #00aae4;"># Ruta a los archivos f铆sicos que contienen las vistas </b>
    app.set('view engine', 'ejs');                     <b style="background-color: #00aae4;"># Motor de renderizaci贸n - EJS</b>
  </code></pre>

  + Configuraci贸n de la aplicaci贸n

  <pre><code>
    app.use(logger('dev'));                             <b style="background-color: #00aae4;"># Instanciaci贸n del registrador (logger) de acciones para el MODO DE DESARROLLO</b>
    app.use(express.json());                            <b style="background-color: #00aae4;"># Este m茅todo se usa para analizar las solicitudes entrantes con cargas JSON y se basa en el analizador de cuerpo de mensajes HTTP.</b>
    app.use(express.urlencoded({ extended: false }));   <b style="background-color: #00aae4;"># Analiza las requests entrantes con cargas codificadas y se basa en body-parser. </b>
    app.use(cookieParser());                            <b style="background-color: #00aae4;"># Manejo de cookies entre el cliente y el servidor </b>
    app.use(express.static(path.join(__dirname, 'public')));     <b style="background-color: #00aae4;"># Registro de la ruta para archivos est谩ticos (im谩genes, hojas de estilo, etc)</b>
  </code></pre>


  + Relaci贸n entre las rutas externas y las rutas internas 

  <pre><code>
    app.use('/', indexRouter);              
    app.use('/users', usersRouter);        
  </code></pre>


  + Middleware para errores

  <pre><code>
    // catch 404 and forward to error handler
    app.use(function(req, res, next) {
      next(createError(404));               <b style="background-color: #9b47d3;"># En caso de cualquier error, lanzar un error404 </b>
    });
  
    // error handler
    app.use(function(err, req, res, next) {
      // set locals, only providing error in development
      res.locals.message = err.message;
      res.locals.error = req.app.get('env') === 'development' ? err : {}; <b style="background-color: #9b47d3;"># Los errores se mostrar谩n en el MODO DE DESARROLLO </b>

      // render the error page
      res.status(err.status || 500);
      res.render('error');
    });
  </code></pre>


* Los siguientes comandos nos ayudar谩n a comprobar el funcionamiento del servidor. Cada comando es ejecutado individualmente. 

    <pre><code>
      cd sitio   
      npm install   
      SET DEBUG=sitio:\* & npm start
    </code></pre>

* Luego, acceda a  `http://localhost:3000/` en su navegador para visualizar su aplicaci贸n. 
<a name="referencias"></a>

Referencias
===================

* * *

* Express. Retrieved February 24, 2023, from https://expressjs.com/es/ 
* Introducci贸n a Express/Node - Aprende sobre desarrollo web MDN. Recuperado el 24 de febrero de 2023, de https://developer.mozilla.org/es/docs/Learn/Server-side/Express_Nodejs/Introduction
Tutorial Express Parte 2: Creando un sitio web esqueleto - Aprende desarrollo web MDN. Recuperado el 24 de febrero de 2023, de https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/skeleton_website 
