[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# File uploads
<p align="center">
<img src="https://www.w3jar.com/wp-content/uploads/node-js-file-upload-express.png" width="70%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [File uploads](#file_uploads)
  - [Tipos de file uploads](#tipos)
    - [Busboy](#busboy)
    - [Formidable](#formidable)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="file_uploads"> </a>

### 🟠 File uploads

Ya hemos mencionado que la carga de archivos trae consigo una serie de complicaciones. Afortunadamente, hay algunos proyectos geniales que ayudan a que el manejo de archivos sea muy sencillo.
Actualmente, las cargas de archivos se pueden manejar con el middleware multiparte incorporado de Connect; sin embargo, ese middleware ya se eliminó de Connect, y tan pronto como Express actualice su dependencia de Connect, también desaparecerá de Express, por lo que le recomiendo enfáticamente que no use ese middleware.

<a name="tipos"> </a>

### 🟠 Tipos de file uploads

Hay dos opciones populares y sólidas para el procesamiento de formularios de varias partes: Busboy y Formidable. 

<a name="busboy"> </a>

#### 🔹 Busboy
 Al llenarlo req.body, se necesita un cambio de código mínimo para usarlo.

```js
import bb from 'express-busboy';
const app = express();
bb.extend(app);
```

Por defecto, la carga de archivos está deshabilitada, el req.filesobjeto siempre estará vacío. Puedes activarlos con:

```js
bb.extend(app, {
    upload: true,
    path: '/path/to/save/files',
    allowedPath: /./
});
```

<a name="formidable"> </a>

#### 🔹 Formidable

Formidable es un módulo de Node.js para analizar datos de formularios, incluida multipart/form-datala carga de archivos.Entonces, express-formidablees algo así como un puente entre ellos, específicamente una implementación de middleware Express de Formidable.

```js
const express = require('express');
const formidableMiddleware = require('express-formidable');
 
var app = express();
 
app.use(formidableMiddleware());
 
app.post('/upload', (req, res) => {
  req.fields; // contains non-file fields
  req.files; // contains files
});
```


<a name="referencias"></a>

## Referencias

* Express-busboy. Retrieved February 21, 2023, from https://www.npmjs.com/package/express-busboy
* Express-formidable. Retrieved 21 February 2023, from https://www.npmjs.com/package/express-formidable