[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Rate Limiter

<p align="center">
<img src="https://miro.medium.com/v2/resize:fit:1400/1*l8pn27-7xGBhjKOzQHZLnw.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Rate Limiter](#comments)
  - [¿Qué es la limitación de velocidad?](#comment)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Rate Limiter

La limitación de velocidad es una característica muy poderosa para proteger las API de back-end de ataques maliciosos y para manejar flujos de solicitudes no deseados de los usuarios. En términos generales, nos permite controlar la velocidad a la que nuestro servidor procesa las solicitudes de los usuarios.

<a name="comment"> </a>

### 🟠 ¿Qué es la limitación de velocidad?

La limitación de velocidad es una técnica utilizada para controlar la cantidad de tráfico entrante o saliente dentro de una red. En este contexto, red se refiere a la línea de comunicación entre un cliente (p. ej., un navegador web) y nuestro servidor (p. ej., una API).

Por lo tanto, es una técnica que nos permite manejar las solicitudes de los usuarios en función de alguna restricción específica tal que:

   * Hay un mejor flujo de datos.
   * Hay un riesgo reducido de ataque, es decir, seguridad mejorada
   * El servidor nunca se sobrecarga.
   * Los usuarios solo pueden hacer todo lo que les permite el desarrollador.

Por ejemplo, podríamos querer limitar la cantidad de solicitudes que un usuario no suscrito puede realizar a una API pública a 1000 solicitudes por mes. Una vez que el usuario supera ese número, podemos ignorar la solicitud y arrojar un error que indica que el usuario ha excedido su límite.


Tenga en cuenta que para que se implemente la limitación de velocidad, debe haber una restricción (límite) claramente definida, que puede basarse en cualquiera de los siguientes:

* **Usuarios:**

La restricción es específica de un usuario y se implementa mediante un identificador de usuario único.

* **Ubicación:**

La restricción se basa en la geografía y se implementa en función de la ubicación desde la que se realizó la solicitud.

* **Direcciones IP:** la restricción se basa en la dirección IP del dispositivo que inicia una solicitud.

<p align="center">
<img src="https://media.licdn.com/dms/image/C5612AQGVjVSzWNq9LA/article-cover_image-shrink_600_2000/0/1623140381082?e=2147483647&v=beta&t=7NIxGIIv1ZDDvC5GvLcvqXJRzH7DLlvWpRF_n694pes" width="50%"/>
</p>

<a name="referencias"></a>

## Referencias

* Understanding and implementing rate limiting in Node.js. Retrieved May 12, 2023, from [https://blog.logrocket.com/rate-limiting-node-js/](https://blog.logrocket.com/rate-limiting-node-js/)