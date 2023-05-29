[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)
# Webhooks, JWT, API GW

<p align="center">
<img src="https://phpenthusiast.com/theme/assets/images/blog/what_is_rest_api.png" width="70%" alt="Banner Node.js"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Webhooks](#webhooks)
    - [Ejemplos de webhooks](#ejemplosWebHooks)
  - [JWT](#jwt)
  - [API GW](#API-GW)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="webhooks"> </a>

### 🟠 Webhooks

Los webhooks son "devoluciones de llamada HTTP definidas por el usuario". Por lo general, se desencadenan por algún evento, como enviar código a un repositorio o publicar un comentario en un blog. Cuando ocurre ese evento, el sitio de origen realiza una solicitud HTTP al URI configurado para el webhook. Los usuarios pueden configurarlos para causar eventos en un sitio para invocar el comportamiento en otro. La acción tomada puede ser cualquier cosa. Los usos comunes son activar compilaciones con sistemas de integración continua o notificar sistemas de seguimiento de errores. Dado que utilizan HTTP, pueden integrarse en servicios web sin agregar nueva infraestructura.

<p align="center">
<img src="https://websitepandas.com/wp-content/uploads/2020/12/1.png" width="50%" alt="Banner"/>
</p>

Para instalar el paquete de webhooks y aplicarlo a su proyecto de node utilice el siguiente comando:

```
npm install node-webhooks --save
```
Cuando se activa un webHook, enviará una solicitud HTTPS POST a las URL adjuntas, que contiene una actualización serializada en JSON (la especificada cuando llama al método de activación ).

<a name="ejemplosWebHooks"> </a>

#### 🔹 Ejemplos de webhooks

Los webHooks son útiles siempre que necesite asegurarse de que un servicio externo obtenga actualizaciones de su aplicación. Puede desarrollar fácilmente en su aplicación este tipo de puntos de entrada de webHooks.

* GET /api/webhook/get Devuelve todo el archivo webHook DB.

* GET /api/webhook/get/[WebHookShortname] Devuelve el WebHook seleccionado.

* POST /api/webhook/add/[WebHookShortname] Agregue una nueva URL para el webHook seleccionado. Requiere parámetros JSON:

* GET /api/webhook/delete/[WebHookShortname] Elimina todas las direcciones URL adjuntas al webHook seleccionado.

* POST /api/webhook/delete/[WebHookShortname] Eliminar solo una única URL adjunta al webHook seleccionado. Se requiere un cuerpo json con el parámetro url: { "url": "http://..." }

* POST /api/webhook/trigger/[WebHookShortname] Activar un webHook. Requiere un cuerpo JSON que se entregará a las URL de webHook. También puede proporcionar encabezados personalizados.

<a name="jwt"> </a>

### 🟠 JWT

Tokens web JSON (JWT) es una biblioteca de javascript que crea y verifica tokens. Es un estándar abierto que se utiliza para compartir información entre dos partes: un cliente y un servidor. Usaremos dos funciones de JWT. La primera función es firmar para crear un nuevo token y la segunda función es verificar para verificar el token. Es utilizado para construir API de Nodejs con autenticación JWT. Por otro lado, la autenticación y autorización es el concepto básico de la seguridad informática; en el que se utiliza las credenciales como nombre de usuario y contraseña para probar la identidad y así obtener privilegios adicionales.

Para instalar el paquete de jwt y aplicarlo a su proyecto de node utilice el siguiente comando:

```
npm instalar jsonwebtoken
```

<a name="API-GW"> </a>

### 🟠 API GW

API Gateway es un tipo de servicio en una arquitectura de microservicios que proporciona una capa compartida y una API para que los clientes se comuniquen con los servicios internos. API Gateway puede  enrutar solicitudes , transformar protocolos,  agregar datos  e  implementar lógica compartida  como autenticación y limitadores de velocidad.

Puede pensar en API Gateway como el  punto de entrada  a nuestro mundo de microservicios.
Nuestro sistema puede tener uno o múltiples API Gateways, dependiendo de los requerimientos de los clientes. Por ejemplo, también podemos tener una puerta de enlace separada para navegadores de escritorio, aplicaciones móviles y API públicas.

<p align="center">
<img src="https://blog-assets.risingstack.com/2017/07/api-gateway-1.png" width="50%" alt="Banner"/>
</p>

El objetivo de una puerta de enlace API es proporcionar una capa intermedia entre los clientes y sus microservicios. Al introducir una puerta de enlace API, los clientes envían sus solicitudes a la puerta de enlace que, a su vez, se asegurará de que la solicitud se redirija al microservicio correspondiente.

<p align="center">
<img src="https://miro.medium.com/v2/resize:fit:1100/format:webp/0*vBBQoqJErD_C9k1Q.png" width="50%" alt="Banner"/>
</p>

<a name="autenticacion"> </a>

#### 🔹 Autenticación con API GW

La mayor parte de la infraestructura de microservicios necesita manejar la autenticación. Poner  una lógica compartida  como la autenticación en API Gateway puede ayudarlo a  mantener sus servicios pequeños  y  enfocados en el dominio.

En una arquitectura de microservicios, puede mantener sus servicios protegidos en una DMZ  (zona desmilitarizada)  a través de configuraciones de red y  exponerlos  a los clientes  a través de API Gateway . Esta puerta de enlace también puede manejar más de un método de autenticación. Por ejemplo, puede admitir  la autenticación basada en tokens  y  cookies.

<p align="center">
<img src="https://blog-assets.risingstack.com/2017/07/api-gateway-auth-1.png" width="50%" alt="Banner"/>
</p>

<a name="referencias"></a>

## Referencias

* Node-webhooks. Retrieved May 12, 2023, from [https://www.npmjs.com/package/node-webhooks](https://www.npmjs.com/package/node-webhooks)
* Building an API Gateway using Node.js. Retrieved May 12, 2023, from [https://blog.risingstack.com/building-an-api-gateway-using-nodejs/](https://blog.risingstack.com/building-an-api-gateway-using-nodejs/)