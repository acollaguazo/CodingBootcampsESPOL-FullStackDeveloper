[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)
# Obtener Node

<p align="center">
<img src="https://pplware.sapo.pt/wp-content/uploads/2016/05/nodejs_04.jpg" width="80%" alt="Banner Node.js"/>
</p>

## Contenido

- [Fundamentos te贸ricos](#fundamentos_teoricos)
  - [Node.js](#node)
- [Parte pr谩ctica](#practica)
  - [Instalaci贸n Node](#instalacion_node)
  - [Configuraci贸n de servidor web](confi_web)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 馃搼 Fundamentos te贸ricos

<a name="node"> </a>

### 馃煚 Node

Node.js es un marco de programaci贸n del lado del servidor que utiliza JavaScript como lenguaje de programaci贸n. Node.js es adecuado para los desarrolladores que desean crear aplicaciones de servidor escalables y simult谩neas mediante el uso de funciones como funciones de devoluci贸n de llamada y el ciclo de eventos de tiempo de ejecuci贸n de Node.JS.


<a name="practica"> </a>

## 馃捇 Parte pr谩ctica
<a name="instalacion_node"> </a>

### 馃煚 Instalaci贸n Node

1锔忊儯 Visita el sitio oficial de [Node.](https://nodejs.org/)

2锔忊儯 Para instalar da clic en uno de los botones verdes para iniciar con la descarga del instalador.

<p align="center">
  <img src="../imagenes/instalacionNode.jpg" alt="cliente-servidor" width="50%">
</p>

3锔忊儯 Sigue las instrucciones de instalaci贸n. 

4锔忊儯 La verificaci贸n de que instal贸 correctamente Node es ejecutando el comando `node` en la terminal, debe aparecerle la versi贸n de Node que instal贸. 

<p align="center">
  <img src="../imagenes/node.jpg" alt="cliente-servidor" width="50%">
</p>


<a name="confi_web"> </a>

### 馃煚 Configuraci贸n de servidor web

Una vez instalado Node.js en su computadora, creamos un programa que muestre "Hello World" en un navegador web.

1锔忊儯 En el editor de texto de su preferncia, cree un archivo Node.js en este caso le pondremos "miPrimerPrograma.js" y copie el siguiente c贸digo.

```js
var http = require('http');

http.createServer(function(req,res){
res.writeHead(200, { 'Content-Type': 'text/plain' });
res.end('Hello world!');
}).listen(8080);
console.log('Server started on localhost:3000; press Ctrl-C to terminate....');
```

2锔忊儯 Guarde el archivo en su computador. 

3锔忊儯 Dentro de la l铆nea de comandos en su computadora, dir铆jase a la carpeta donde se encuentra el archivo "miPrimerPrograma.js". Para abrir la interfaz de l铆nea de comandos en usuarios de Windows, presione el bot贸n de inicio y busque "S铆mbolo del sistema", o simplemente escriba "cmd" en el campo de b煤squeda.

4锔忊儯 Para iniciar el archivo de Node.js, en el cmd escriba `node "miPrimerPrograma.js"` y presione enter. Ahora, su computadora funciona como un servidor. 

5锔忊儯 En su navegador de preferencia escriba la siguiente direcci贸n: http://localhost:8080. Se muestre un 'Hello World!' en el navegador. 

<p align="center">
<img src="../imagenes/helloWorld.jpg" width="80%" alt="Banner Node.js"/>
</p>

<a name="referencias"></a>

## Referencias

* Node.js Get Started. Retrieved February 12, 2023, from https://www.w3schools.com/nodejs/nodejs_get_started.asp
