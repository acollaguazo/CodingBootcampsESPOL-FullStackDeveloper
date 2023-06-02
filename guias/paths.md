---
remote_theme: pages-themes/architect@v0.2.0
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Paths and regular expressions

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Métodos de ruta](#ruta)
  - [Route paths](#rutasDeRutas)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="ruta"> </a>

### 🟠 Métodos de ruta

Un método de ruta se deriva de uno de los métodos HTTP y se adjunta a una instancia de la expressclase.

El siguiente código es un ejemplo de rutas definidas para los métodos GET y POST a la raíz de la aplicación.

```js
// GET method route
app.get('/', (req, res) => {
  res.send('GET request to the homepage')
})

// POST method route
app.post('/', (req, res) => {
  res.send('POST request to the homepage')
})
```
Express admite los métodos que corresponden a las solicitudes HTTP: get, post, delete, put y head. 
Uno de los métodos especiales es app.all() que es usado para cargar funciones de middleware en una ruta para todos los métodos de solicitud HTTP. A continuación, se muestra el código para que el controlador recepte las solicitudes a la ruta "/secret", es decir para cualquiera de las solicitudes HTTP. 

```js
app.all('/secret', (req, res, next) => {
  console.log('Accessing the secret section ...')
  next() // pass control to the next handler
})
```

<a name="rutasDeRutas"> </a>

### 🟠 Routhe paths

En combinación con un método de solicitud, definen los endpoints en los que se pueden relaizra las solicitudes. Pueden ser cadenas, patrones de cadenas o expresiones regulares.

Los caracteres ?, +, *y ()son subconjuntos de sus equivalentes de expresiones regulares. El guión ( -) y el punto ( .) se interpretan literalmente mediante rutas basadas en cadenas.

Si necesita usar el carácter de dólar `( $)` en una cadena de ruta, enciérrelo dentro de ([y ]). Por ejemplo, la cadena de ruta para las solicitudes en `/data/$book`, sería `/data/([\$])book`.

A continuación, se muestran algunos ejemplos de routhe pahs basadas en cadenas.

```js
// Routhe paths que coincidirá con las solicitudes a /about
app.get('/about', (req, res) => {
  res.send('about')
})

// Routhe paths que coincidirá con las solicitudes a la ruta raíz
app.get('/', (req, res) => {
  res.send('root')
})
```
Los siguientes ejemplos son basados en routhe paths basadas en patrones de cadena.

```js
// Routhe paths que coincidirá con acd y abcd.
app.get('/ab?cd', (req, res) => {
  res.send('ab?cd')
})

// Routhe paths que coincidirá con /abe y /abcde.
app.get('/ab(cd)?e', (req, res) => {
  res.send('ab(cd)?e')
})
```

<a name="referencias"></a>

## Referencias

* Routing. Retrieved May 12, 2023, from [https://expressjs.com/en/guide/routing.html](https://expressjs.com/en/guide/routing.html)