[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)
# CORS

<p align="center">
<img src="https://images.ctfassets.net/nx13ojx82pll/60miWU6vSisC1N2IgQRPkt/61066f84608375c590b6dcb68fb47dc0/nodejs-cors-guide-what-it-is-and-how-to-enable-it-picture-1.png?w=1744&h=982&q=80&fm=png" width="60%" alt="Banner"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Cors](#cors)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="cors"> </a>

### 🟠 Cors

Si está publicando una API, es probable que desee que la API esté disponible para otros. Esto dará como resultado una solicitud HTTP entre sitios. Las solicitudes HTTP entre sitios han sido objeto de muchos ataques y, por lo tanto, han sido restringidas por la política del mismo origen, que restringe desde dónde se pueden cargar los scripts. Específicamente, el protocolo, el dominio y el puerto deben coincidir. Esto hace que sea imposible que su API sea utilizada por otro sitio, que es donde entra CORS. CORS le permite levantar esta restricción caso por caso, incluso permitiéndole enumerar qué dominios específicamente pueden acceder a la guion.
CORS se implementa a través del encabezado Access-Control-Allow-Origin. La forma más fácil de implementarlo en una aplicación Express es usar el paquete cors (npm install--save cors). Para habilitar CORS para su aplicación:

```js
app.use(require('cors')());
```
La palabra CORS significa "intercambio de recursos de origen cruzado" . El uso compartido de recursos de origen cruzado es un mecanismo basado en un encabezado HTTP implementado por el navegador que permite que un servidor o una API (interfaz de programación de aplicaciones) indique cualquier origen (diferente en términos de protocolo, nombre de host o puerto) que no sea su origen desde el cual el origen desconocido obtiene permiso para acceder y cargar recursos. 

<a name="referencias"></a>

## Referencias

* Use of CORS in Node.js. Retrieved May 12, 2023, from [https://www.geeksforgeeks.org/use-of-cors-in-node-js/](https://www.geeksforgeeks.org/use-of-cors-in-node-js/)