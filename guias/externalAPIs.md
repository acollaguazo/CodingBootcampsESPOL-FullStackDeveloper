[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# External APIs

<p align="center">
<img src="https://drek4537l1klr.cloudfront.net/sholmes2/Figures/07fig01_alt.jpg" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Invocación de una API](#comments)
    - [Utilizando HTTPS](#usar)
    - [Utilizando Fetch](#usarD)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Invocación de una API

La invocación de una API es una de las tareas más comunes para el manejo de backends con Node.js. Existen una serie de bibliotecas para aquello: `node-fetch`, `isomorphic-fetch`, `axios`, etc, sin embargo, en realidad hay un par de formas nativas que son bastante simples de usar y no requieren ninguna dependencia externa.


<a name="usar"> </a>

### 🟠 Utilizando HTTPS

Se puede integrar con Node https para realizar una solicitud de API simple con CERO dependencias externas.
Aquí se puede ver que usa la vía nativa require("node:http").

```js
const https = require("node:https");

const request = (options) => {
  return new Promise((resolve, reject) => {
    const req = https.request(options, (res) => {
      let data = "";

      res.on("data", (d) => {
        data += d;
      });

      res.on("end", () => {
        data = JSON.parse(data.toString().trim());

        if (res.statusCode === 200) {
          resolve(data);
        } else {
          reject(new Error(`Error code: ${res.statusCode}.`));
        }
      });

      res.on("error", (error) => {
        reject(new Error(error));
      });
    });

    req.end();
  });
};

const auth = `Basic ${Buffer.from(`${user}:${password}`).toString("base64")}`;

request({
 hostname: "foobar.com",
  port: 443,
  path: "/api/users/1",
  method: "GET",
  headers: {
    Accept: "application/json",
    Authorization: auth,
  },
})
.then((data) => {
  console.log(data);
})
.catch((error) => {
  // Do something with the error
});
```

<a name="usarD"> </a>

### 🟠 Utilizando Fetch

Fetch API está disponible en la mayoría de los navegadores. Sin embargo, a partir de la **versión 18.0.0** se tiene acceso a la fetchAPI en Node.

```js
fetch("https://foobar.com/api/users/1", {
  headers: new Headers({
     'Authorization': `Basic ${Buffer.from(`${user}:${password}`).toString("base64")}`, 
     'Content-Type': 'application/json'
   }), 
})
.then((resp) => {
  if (response.status >= 200 && response.status <= 299) {
      return response.json();
    } else {
      throw Error(response.statusText);
    }
})
.catch(() => {
  return resp.text();
})
```

<a name="referencias"></a>

## Referencias

* Calling an API with authorization using native nodejs with zero external dependencies. Retrieved June 10, 2023, from [https://www.jonathancreamer.com/calling-an-api-with-authorization-using-native-nodejs-with-zero-external-dependencies/](https://www.jonathancreamer.com/calling-an-api-with-authorization-using-native-nodejs-with-zero-external-dependencies/)