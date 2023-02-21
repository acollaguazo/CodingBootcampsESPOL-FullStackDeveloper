[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Middleware
<p align="center">
<img src="https://miro.medium.com/max/945/1*RgPEcCE3mHSGR-fS5lXTCQ.png" width="70%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Middleware](#comments)
  - [Sintaxis de Middleware](#sintaxis)
  - [Ejemplos de Middlewares](#ejemplos)
- [Parte práctica](#practica)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="middleware"> </a>

### 🟠 Middleware

el middleware es una forma de encapsular la funcionalidad: específicamente, la funcionalidad que opera en una solicitud HTTP a su aplicación.  

<a name="sintaxis"> </a>

### 🟠 Sintaxis de Middleware 

 En la práctica, un middleware es simplemente una función que toma tres argumentos: un objeto de solicitud, un objeto de respuesta y una función "next". Tiene la siguiente sintaxis básica:

```js
app.get(path, (req, res, next) => {}, (req, res) => {})
```
La parte central (req,res,next)=>{} es la función de middleware. Aquí generalmente realizamos las acciones requeridas antes de que el usuario pueda ver la página web o llamar a los datos y muchas otras funciones.

<p align="center">
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20211007172251/middleware.png" width="70%"/>
</p>

<a name="ejemplos"> </a>

### 🟠 Ejemplos de Middleware 

A continuación se mostrarán algunos ejemplos simples de middleware.

El siguiente ejemplo registra un mensaje en la consola antes de pasar la solicitud al siguiente middleware en la canalización llamando a next().
```js
app.use(function(req, res, next){
    console.log('processing request for "' + req.url + '"....');
    next();
});
```
El siguiente middleware realmente maneja la solicitud. Tenga en cuenta que si se omite el res.send aquí, nunca se devolverá ninguna respuesta al cliente. Eventualmente, el cliente expiraría.
```js
app.use(function(req, res, next){
    console.log('terminating request');
    res.send('thanks for playing!');
});
```
El último middleware nunca se ejecutará porque todas las solicitudes finalizan en el middleware anterior.
```js
app.use(function(req, res, next){
console.log('whoops, i\'ll never get called!');
});
```
<a name="practica"> </a>

## 💻 Parte práctica


<a name="referencias"></a>

## Referencias

* Middleware in Express. Retrieved February 21, 2023, from https://www.geeksforgeeks.org/middleware-in-express-js/  