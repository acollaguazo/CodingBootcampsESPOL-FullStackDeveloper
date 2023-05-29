[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)
# Our Data Store

<p align="center">
<img src="https://mrviriato.files.wordpress.com/2018/10/mongoose.png" width="60%" alt="Banner"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Our Data Store](#dataStore)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="dataStore"> </a>

### 🟠 Our Data Store

Se estará utilizando Mongoose para crear el modelo de prevención en la base de datos para ello se tendrá la siguiente estructura:

```js
var mongoose = require('mongoose');
var preventionSchema = mongoose.Schema({
    name: String,
    description: String,
    location: { lat: Number, lng: Number },
    area: Number,
    perimeter: Number,

});
var Attraction = mongoose.model('Prevention', preventionSchema);
module.exports = Prevention;
```