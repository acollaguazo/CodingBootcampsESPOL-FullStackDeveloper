[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)
# Configuración de servidor web con Node.js

<p align="center">
<img src="https://phpenthusiast.com/theme/assets/images/blog/what_is_rest_api.png" width="70%" alt="Banner Node.js"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Métodos HTTP](#http)
  - [Códigos de estado de respuesta HTTP](#codigos_estado)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="http"> </a>

### 🟠 Métodos HTTP

Como se mencionaba en secciones anteriores, el internet es una arquitectura cliente-servidor. Es decir, el usuario final interactúa con el cliente, mientras que los servidores administran los servicios en donde operan las aplicaciones, la lógica empresarial y los datos. Por otro lado, los datos se transfieren entre el cliente y el servidor utilizando el protocolo de transferencia de hipertexto, más conocido como HTTP. 

El protocolo HTTP regula la forma en el que el cliente realiza peticiones y la forma en la que responde el servidor, por tal razón, emplea diferentes métodos de petición, que se describirán a continuación:

* **GET**

El método GET se utiliza como una solicitud de recuperación de un recurso. Las peticiones de tipo GET solo se usan para recuperar datos.

* **HEAD**

El método HEAD pide una repuesta idéntica a la de una petición GET. A diferencia del GET, el HEAD envía la respuesta sin el cuerpo de la misma, únicamente el encabezado de la solicitud. 

* **POST**

El método POST envía datos al servidor para crear un recurso lo que implicaría un cambio de estado en el servidor.

* **PUT**

El método PUT actualiza un recurso o reemplaza uno existente. Es similar a un UPDATE a nivel de base de datos. Devuelve el código 200_OK si el recurso ya existe, en caso de que no existe el recurso devuelve el código 404_NOT_FOUND. 

* **DELETE**

El método HTTP DELETE elimina un recurso y devuelve el código 204_NO_CONTENT si el recurso existe y pudo eliminarlo. Es similar a un DELETE a nivel de base de datos.

* **PATCH**

El método PATCH se emplea para realizar modificaciones parciales a un recurso en particular. 

Debemos considerar que los métodos **PUT** & **DELETE** son idempotentes, lo que significa que si se ejecutan múltiples veces tiene el mismo efecto. En cambio, el método POST cada que se ejecuta se agrega un nuevo objeto. 

<a name="codigos_estado"> </a>

### 🟠 Códigos de estado de respuesta HTTP

Los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica. Las respuestas se agrupan en cinco clases:

1. Respuestas informativas (100–199),
2. Respuestas satisfactorias (200–299),
3. Redirecciones (300–399),
4. Errores de los clientes (400–499),
5. y errores de los servidores (500–599).

A continuación se indica las respuestas satisfactorias que se obtienen de los métodos HTTP.

* **GET**

El recurso se ha obtenido y se transmite en el cuerpo del mensaje.

* **HEAD**

Los encabezados de entidad están en el cuerpo del mensaje.

* **PUT o POST**

El recurso que describe el resultado de la acción se transmite en el cuerpo del mensaje.

* **TRACE**

El cuerpo del mensaje contiene el mensaje de solicitud recibido por el servidor.

| Código | Descripción |
|----------|----------|
| 200 OK    | La solicitud ha tenido éxito. El significado de un éxito varía dependiendo del método HTTP.   |
| 400 Bad Request    | Esta respuesta significa que el servidor no pudo interpretar la solicitud dada una sintaxis inválida.   |
| 404 Not Found    | El servidor no pudo encontrar el contenido solicitado. Este código de respuesta es uno de los más famosos dada su alta ocurrencia en la web.   |
| 500 Internal Server Error    | El servidor ha encontrado una situación que no sabe cómo manejarla.   |

 

<p align="center">
<img src="https://www.lucushost.com/blog/wp-content/uploads/2018/09/codigos-estado-http.png" width="70%" alt="Banner"/>
</p>

<a name="referencias"></a>

## Referencias

* Node.js Get Started. Retrieved February 12, 2023, from [https://www.w3schools.com/nodejs/nodejs_get_started.asp](https://www.w3schools.com/nodejs/nodejs_get_started.asp)
* Códigos de estado de respuesta HTTP. Retrieved May 12, 2023, from [https://developer.mozilla.org/es/docs/Web/HTTP/Status](https://developer.mozilla.org/es/docs/Web/HTTP/Status)