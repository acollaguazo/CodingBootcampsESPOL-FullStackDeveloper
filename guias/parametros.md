---
remote_theme: pages-themes/architect@v0.2.0
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Parámetros

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Parámetros de ruta](#param)
  - [Route paths](#rutasDeRutas)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="param"> </a>

### 🟠 Parámetros de ruta

Los parámetros de ruta son segmentos de URL con nombre que se utilizan para capturar los valores especificados en su posición en la URL. Los valores capturados se rellenan en el objeto **req.params**, con el nombre del parámetro de ruta especificado en la ruta como sus respectivas claves.

```js
Route path: /users/:userId/books/:bookId
Request URL: http://localhost:3000/users/34/books/8989
req.params: { "userId": "34", "bookId": "8989" }
```

Para definir rutas con parámetros de ruta, simplemente especifique los parámetros de ruta en la ruta de la ruta como se muestra a continuación.

```js
app.get('/users/:userId/books/:bookId', (req, res) => {
  res.send(req.params)
})
```

Para tener más control sobre la cadena exacta que puede coincidir con un parámetro de ruta, puede agregar una expresión regular entre paréntesis ( ()):

```js
Route path: /user/:userId(\d+)
Request URL: http://localhost:3000/user/42
req.params: {"userId": "42"}
```
**Aspecto a considerar:** 
* El nombre de los parámetros de ruta debe estar compuesto por “caracteres de palabra” ([A-Za-z0-9_]).
* Dado que la expresión regular suele formar parte de una cadena literal, asegúrese de incluir \una barra invertida adicional en los caracteres de escape, por ejemplo \\d+.
* En Express 4.x, el *carácter de las expresiones regulares no se interpreta de la forma habitual . Como solución alternativa, use {0,}en lugar de *. Es probable que esto se solucione en Express 5.

<a name="referencias"></a>

## Referencias

* Routing. Retrieved May 12, 2023, from [https://expressjs.com/en/guide/routing.html](https://expressjs.com/en/guide/routing.html)