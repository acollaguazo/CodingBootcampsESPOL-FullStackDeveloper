[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Template engine
<p align="center">
<img src="https://blog.logrocket.com/wp-content/uploads/2021/12/template-engine-visual.png"  alt="Banner Template engine" width="80%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Motores de plantilla](#motores_plantilla)
  - [Ventaja de motores de plantilla](#ventaja_plantilla)
  - [Criterios al elegir un motor de plantilla](#criterio_plantilla)
    - [Rendimiento](#rendimiento)
    - [¿Cliente, servidor o ambos?](#csa)
    - [Abstracción](#abstracción)
  - [Ejemplos de motores de plantilla](#ejemplos_plantilla)
- [Parte práctica](#practica)
  - [Motor de plantilla PUG](#pug)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="motores_plantilla"> </a>

### 🟠 Motores de plantilla

Un motor de plantillas le permite utilizar archivos de plantillas estáticas en su aplicación. En tiempo de ejecución, el motor de plantillas reemplaza las variables en un archivo de plantilla con valores reales y transforma la plantilla en un archivo HTML enviado al cliente. Este enfoque facilita el diseño de una página HTML.

<a name="ventaja_plantilla"> </a>

### 🟠 Ventaja de motores de plantilla

Entre las ventajas de usar motores de plantillas están:
+ Mejora la productividad del desarrollador.
+ Mejora la legibilidad y la mantenibilidad.
+ Plantilla única para varias páginas. 

<a name="criterio_plantilla"> </a>

### 🟠 Criterios al elegir un motor de plantilla

En el mundo de Node, existen varios motores de plantillas, por tal razóm surge la interrogante ¿Cuál debo elegir?. Es una pregunta complicada pero depende de tus necesidades. Sin embargo, hay algunos criterios a considerar:

<a name="rendimiento"> </a>

#### 🔹 Rendimiento

Debes escoger un motor de plantillas que sea lo más rápido posible. No se desea ralentizar tu sitio web.

<a name="csa"> </a>

#### 🔹 ¿Cliente, servidor o ambos?

La mayoría de los motores de plantillas, pero no todos, están disponibles tanto en el lado del servidor como en el del cliente. Si necesita usar plantillas en ambos ámbitos se recomienda que elija algo que sea igualmente capaz en cualquiera de las dos capacidades.

<a name="abstracción"> </a>

#### 🔹 Abstracción

¿Quieres algo familiar (como HTML normal con corchetes, por ejemplo), o odias HTML en secreto y te encantaría algo que te salve de todos esos corchetes angulares? Las plantillas (especialmente las plantillas del lado del servidor) le brindan algunas opciones.

<a name="ejemplos_plantilla"> </a>

### 🟠 Ejemplos de motores de plantilla

Express permite trabajar con muchos motores de plantilla entre los que se encuentra:
+ Pug Js
+ Moustache
+ EJS
+ Jade

<a name="practica"> </a>

## 💻 Parte práctica

<a name="pug"> </a>

### 🟠 Motor de plantilla PUG
[Pug JS](https://pugjs.org/api/getting-started.html) permite utilizar archivos estáticos como plantillas, enviar valores para reemplazar variables dentro de las mismas y transformar estos archivos en páginas HTML que se envían al cliente.

<p align="center">
<img src="https://www.nodejsera.com/library/assets/img/pug-logo.png"  alt="BPUG" width="50%"/>
</p>

A continuación se realizará una práctica utilizando pug como motor de plantilla. 

1️⃣ En tu editor de texto favorito, crea un directorio donde se generará la plantilla de pug.

2️⃣ En la raíz del proyecto, crear un directorio con el nombre de "views".

3️⃣ Ahora se le indicará a express que el directorio "views" contendrá las plantillas. Además de que el motor de plantillas que se utilizará sera Pug Js. El archivo index.js tendrá la siguiente estructura:

```
const express = require('express');
const port = 3000;
const app = express();

app.use('/static', express.static(__dirname + '/public'));

app.use(express.urlencoded({ extended: false }));
app.use(express.json());

// Se indica el directorio donde se almacenarán las plantillas 
app.set('views', './views');

// Se indica el motor del plantillas a utilizar
app.set('view engine', 'pug');

app.get('/hello', (req, res) => {
  res.send('Hola mundo');
});

app.get('/urlparam', (req, res) => {
  res.send(req.query);
});

app.post('/urljson', (req, res) => {
  res.send(req.body);
});

app.listen(port, () => console.log(`Servidor iniciado en el puerto ${port}`));
```
4️⃣ Ahora instalaremos Pug JS, para esto abriremos la terminal, nos posicionaremos en la ruta de nuestra aplicación y lo instalaremos con ayuda de npm con el siguiente comando:

```
npm install pug
```

5️⃣ Ya instalado correctamente el motor de plantilla, crearemos la primera plantilla para mostrarla al cliente. Para ello crearemos el archivo hello.pug (.pug es la extensión de las plantillas). En archivo hello.pug tendrá el siguiente codigo:

```
html
    head
        title="Mi primera plantilla Pug JS"
    body
        h1=mensaje
```
En el codigo se stá declarando una variable con nombre “mensaje”, esta será reemplazada con el valor que se enviará al momento de transforma de formato .pug a HTML.

6️⃣ Ahora se usará la funcion render que recibe dos parámetros, el primero el nombre de la plantilla a mostrar y el segundo un objeto con los valores a reemplazar. Con el fin de modificar la ruta “/hello”, actualmente está mostrando al usuario el mensaje “Hola mundo”, lo reemplazaremos con la plantilla que creamos.
El código final de index.js queda de la siguiente manera: 

```
const express = require('express');
const port = 3000;
const app = express();

app.use('/static', express.static(__dirname + '/public'));

app.use(express.urlencoded({ extended: false }));
app.use(express.json());

// Se indica el directorio donde se almacenarán las plantillas 
app.set('views', './views');

// Se indica el motor del plantillas a utilizar
app.set('view engine', 'pug');

app.get('/hello', (req, res) => {
  res.render('hello.pug', { mensaje: 'Usando Pug JS en Express' }); // Se muestra la plantilla hello.pug
});

app.get('/urlparam', (req, res) => {
  res.send(req.query);
});

app.post('/urljson', (req, res) => {
  res.send(req.body);
});
```
7️⃣ Finalmente ejeucta el archivo index.js y el resultado será un mensaje que dice "Usando Pug JS en Express" que se mostrará al cliente a través de una página HTML.

<a name="referencias"></a>

## Referencias

* Using template engines with Express. Retrieved February 15, 2023, from https://expressjs.com/en/guide/using-template-engines.html
* Template engines. Retrieved 15 February 2023, from https://expressjs.com/en/resources/template-engines.html