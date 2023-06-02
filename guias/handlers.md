---
remote_theme: pages-themes/architect@v0.2.0
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Handlers

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Controladores de ruta](#controladores)
  - [Métodos de respuesta](#metodos)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="param"> </a>

### 🟠 Controladores de ruta

Puede proporcionar múltiples funciones de devolución de llamada que se comportan como un middleware para manejar una solicitud. La única excepción es que estas devoluciones de llamada pueden invocarse next('route')para omitir las devoluciones de llamada de ruta restantes. Puede usar este mecanismo para imponer condiciones previas en una ruta y luego pasar el control a rutas posteriores si no hay razón para continuar con la ruta actual.

Los controladores de rutas pueden tener la forma de una función, una matriz de funciones o una combinación de ambas, como se muestra en los siguientes ejemplos.

Una sola función de devolución de llamada puede manejar una ruta. Por ejemplo:

```js
app.get('/example/a', (req, res) => {
  res.send('Hello from A!')
})
```
Más de una función de devolución de llamada puede manejar una ruta. Por ejemplo:

```js
app.get('/example/b', (req, res, next) => {
  console.log('the response will be sent by the next function ...')
  next()
}, (req, res) => {
  res.send('Hello from B!')
})
```
<a name="metodos"> </a>

### 🟠 Métodos de respuesta

Los métodos en el objeto de respuesta ( res) en la siguiente tabla pueden enviar una respuesta al cliente y terminar el ciclo de solicitud-respuesta. Si ninguno de estos métodos se llama desde un controlador de ruta, la solicitud del cliente quedará pendiente.

| Método | Descripción |
|----------|----------|
| res.download()    | Pide que se descargue un archivo.  |
| res.end()    | Terminar el proceso de respuesta.   |
| res.json()   | Envía una respuesta JSON.   |
| res.redirect()   | Redirigir una solicitud.   |
| res.render()   | Renderice una plantilla de vista.   |
| res.send()  | Enviar una respuesta de varios tipos.   |


<a name="referencias"></a>

## Referencias

* Routing. Retrieved May 12, 2023, from [https://expressjs.com/en/guide/routing.html](https://expressjs.com/en/guide/routing.html)