[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)
# API Design

<p align="center">
<img src="https://www.b2chat.io/wp-content/uploads/2022/04/diagrama-de-un-api.webp" width="50%" alt="Banner"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [¿Qué es una API?](#API)
  - [¿Qué signifca API?](#SigAPI)
  - [¿Cómo funcionan las API?](#FuncionamientoAPI)
  - [API REST](#APIRest)
  - [Tipos de API](#tipos)
- [Referencias](#jsonXML)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="API"> </a>

### 🟠 ¿Qué es una API?

Las API son mecanismos que permiten a dos componentes de software comunicarse entre sí mediante un conjunto de definiciones y protocolos. Por ejemplo, un sistema de software de prevención de incendios forestales contendrá todos los datos relacionados que se necesitan para determinar un posible incendio, por tal razón, es ahi cuando la aplicación o sistema se comunicará a traves de las API y se mostrará en su telefono las actualizaciones diarias en su teléfono de alguna zona en particular. 

<a name="SigAPI"> </a>

### 🟠 ¿Qué signifca API?

El término API es una abreviatura de las siguientes palabras **A**pplication **P**rogramming **I**nterfaces, que es español significa “interfaz de programación de aplicaciones”. En el contexto de las API, la plabra aplicación hace referencia a cualquier software que tiene una funcionalidad distinta. La interfaz es el medio entre el cúal se recepten las solicitudes y respuestas. 

<a name="FuncionamientoAPI"> </a>

### 🟠 ¿Cómo funcionan las API?

La arquitectura de las API suele explicarse en términos de cliente y servidor. La aplicación que envía la solicitud se llama cliente, y la que envía la respuesta se llama servidor. En el ejemplo que se mencionaba de una aplicación de prevención de incendios forestales, la base de datos es el servidor y la aplicación móvil es el cliente.

Las API pueden funcionar de cuatro maneras diferentes, según el momento y el motivo de su creación.

**API de SOAP**
Estas API utilizan el protocolo simple de acceso a objetos. El cliente y el servidor intercambian mensajes mediante XML. Se trata de una API menos flexible que era más popular en el pasado.

**API de RPC**
Estas API se denominan llamadas a procedimientos remotos. El cliente completa una función (o procedimiento) en el servidor, y el servidor devuelve el resultado al cliente.

**API de WebSocket**
La API de WebSocket es otro desarrollo moderno de la API web que utiliza objetos JSON para transmitir datos. La API de WebSocket admite la comunicación bidireccional entre las aplicaciones cliente y el servidor. El servidor puede enviar mensajes de devolución de llamada a los clientes conectados, por lo que es más eficiente que la API de REST.

**API de REST**
Estas son las API más populares y flexibles que se encuentran en la web actualmente. El cliente envía las solicitudes al servidor como datos. El servidor utiliza esta entrada del cliente para iniciar funciones internas y devuelve los datos de salida al cliente. Veamos las API de REST con más detalle a continuación.

<a name="APIRest"> </a>

### 🟠 API REST

REST significa transferencia de estado representacional. REST define un conjunto de funciones como GET, PUT, DELETE, etc. que los clientes pueden utilizar para acceder a los datos del servidor. Los clientes y los servidores intercambian datos mediante HTTP.

La principal característica de la API de REST es que no tiene estado. La ausencia de estado significa que los servidores no guardan los datos del cliente entre las solicitudes. Las solicitudes de los clientes al servidor son similares a las URL que se escriben en el navegador para visitar un sitio web. La respuesta del servidor son datos simples, sin la típica representación gráfica de una página web.

<p align="center">
<img src="https://dossetenta.com/wp-content/uploads/2021/12/R6qFq3n.png" width="50%" alt="Banner"/>
</p>

<a name="tipos"> </a>

### 🟠 Tipos de API

Las API se clasifican tanto en función de su arquitectura como de su ámbito de uso. Ya exploramos los principales tipos de arquitecturas de API, ahora veamos el ámbito de uso.

**API privadas**
Estas son internas de una empresa y solo se utilizan para conectar sistemas y datos dentro de la empresa.

**API públicas** 
Están abiertas al público y pueden cualquier persona puede utilizarlas. Puede haber o no alguna autorización y coste asociado a este tipo de API.

**API de socios** 
Solo pueden acceder a ellas los desarrolladores externos autorizados para ayudar a las asociaciones entre empresas.

**API compuestas** 
Estas combinan dos o más API diferentes para abordar requisitos o comportamientos complejos del sistema. 

<a name="referencias"></a>

## Referencias

* ¿Qué es una API?. Retrieved May 12, 2023, from [https://aws.amazon.com/es/what-is/api/#:~:text=en%20su%20tel%C3%A9fono.-,%C2%BFQu%C3%A9%20significa%20API%3F,de%20servicio%20entre%20dos%20aplicaciones.](https://aws.amazon.com/es/what-is/api/#:~:text=en%20su%20tel%C3%A9fono.-,%C2%BFQu%C3%A9%20significa%20API%3F,de%20servicio%20entre%20dos%20aplicaciones.)