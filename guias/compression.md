[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Compression

<p align="center">
<img src="https://miro.medium.com/v2/resize:fit:1050/1*mSID8QuKF-c3qOsDO_nbnw.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Compression](#comments)
  - [Uso de compression con Gzip](#usar)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Compression

La compresión ayuda a disminuir la cantidad de datos descargables en nuestra aplicación NodeJS y conduce a una mejora en el rendimiento de la aplicación. Este proceso de compresión puede reducir drásticamente el tamaño de la carga útil por encima del 70 %.

<a name="usar"> </a>

### 🟠 Uso de compression con Gzip

Gzip es la compresión más utilizada, especialmente para las interacciones entre el servidor y el cliente.

En el archivo **index.js** se agregará el middleware de compresión para nuestra aplicación de NodeJS. Esto habilitará GZIP, lo que hace que sus respuestas HTTP sean más pequeñas.

* Iniciamos creando una aplicación NodeJS.

```
mkdir Project 
cd Project
npm init -y
```

* Instale el módulo de compresión y ExpressJS usando el siguiente comando:

```
npm install compression --save
npm install express --save
```

* Ahora se debe crear en la raíz del proyecto el archivo **index.js**.


```js
// Initialize compression module
const compression = require('compression');
const express = require('express');
const app = express();
  
// Compress all HTTP responses
app.use(compression());
  
// It will repeatedly the word 'I love GeeksforGeeks'
const data = ('I love GeeksforGeeks').repeat(800) ;
  
app.get('/', (req, res) => {
  // Send as 'text/html' format file
  res.send(data);
});
  
// Server setup
app.listen(8080, function () {
  console.log('Server listening on port 8080!');
});
```

* Ejecuta el archivo index.js.

```
node index.js
```

*  En el navegador acceda a la URL [http://localhost:8080/](http://localhost:8080/).

Si la compresión está activada la compresión está activada.

<a name="referencias"></a>

## Referencias

* How to do compression with Gzip in Node.js ?. Retrieved May 12, 2023, from [https://www.geeksforgeeks.org/how-to-do-compression-with-gzip-in-node-js/](https://www.geeksforgeeks.org/how-to-do-compression-with-gzip-in-node-js/)