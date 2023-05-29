---
remote_theme: pages-themes/architect@v0.2.0
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Internet y protocolo HTTP
<p align="center">
<img src="https://www.simplilearn.com/ice9/free_resources_article_thumb/what_is_Internet.jpg"  alt="Banner Internet" width="80%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Internet](#internet)
  - [Protocolo HTTP](#protocolo_http)
  - [Arquitectura Cliente-Servidor](#cliente_servidor)
  - [HTTP Request](#http_request)
  - [HTTP Response](#http_response)
- [Parte práctica](#practica)
  - [Funcionamiento HTTP](#funcionamiento_http)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="internet"> </a>

### 🟠 Internet

Es una red global que conecta millones y miles de millones de computadoras en todo el mundo. Miles de millones de usuarios en todo el mundo están conectados a través del conjunto estándar de protocolos de Internet (TCP/IP). Internet se configura mediante el uso de tecnologías inalámbricas, de redes y electrónicas. Es el medio más rápido para enviar e intercambiar datos e información entre las computadoras de todo el mundo.
<a name="protocolo_http"> </a>

### 🟠 Protocolo HTTP

HTTP, de sus siglas en inglés: "Hypertext Transfer Protocol", es el nombre de un protocolo el cual nos permite realizar una petición de datos y recursos. Es la base de cualquier intercambio de datos en la Web, y un protocolo de estructura cliente-servidor, esto quiere decir que una petición de datos es iniciada por el elemento que recibirá los datos (el cliente), normalmente un navegador Web.
Clientes y servidores se comunican intercambiando mensajes individuales (en contraposición a las comunicaciones que utilizan flujos continuos de datos). Los mensajes que envía el cliente, normalmente un navegador Web, se llaman peticiones, y los mensajes enviados por el servidor se llaman respuestas.

<a name="cliente_servidor"> </a>

### 🟠 Arquitectura Cliente-Servidor

El modelo cliente-servidor es una arquitectura software que involucra uno o más clientes solicitando servicios a uno o más servidores. La separación entre cliente y servidor es una separación de tipo lógico, donde el servidor no se ejecuta necesariamente sobre una sola máquina ni es necesariamente un sólo programa. Los tipos específicos de servidores incluyen los servidores web, los servidores de archivo, los servidores del correo, etc. Mientras que sus propósitos varían de unos servicios a otros, la arquitectura básica seguirá siendo la misma.

<p align="center">
  <img src="https://static.wixstatic.com/media/1899d0_a19fc771edff4ca89be429574e681f95.jpg/v1/fill/w_521,h_397,al_c,lg_1,q_80,enc_auto/1899d0_a19fc771edff4ca89be429574e681f95.jpg" alt="cliente-servidor" width="50%">
</p>

Los componentes de esta arquitectura son: cliente, servidor y proxy. 

🔹 Cliente

Los clientes son los que originan el trafico web, es decir envían las peticiones y reciben las respuestas. Los navegadores son un tipo de cliente web. El navegador tiene la capacidad de interpretar varios lenguajes de programación especialmente creados para la visualización y maquetación de contenido. 
<p align="center">
  <img src="https://cdn.computerhoy.com/sites/navi.axelspringer.es/public/media/image/2021/07/navegadores-2397647.jpg?tf=1920x" alt="cliente-servidor" width="50%">
</p>

🔹 Servidor

El servidor es un software especializado que esta a la espera de peticiones de recursos web por el lado del cliente. Las acciones que realiza el servidor son:
  + Conexión con el cliente.
  + Recepta el mensaje HTTP de la petición.
  + Procesa el mensaje HTTP.
  + Localiza y envía el resultado (en forma de mensaje HTTP). 

🔹 Proxy

Un proxy es un intermediario entre el cliente y el servidor, Realizan simultáneamente el papel de servidor y cliente; con el fin de reducir comunicación no deseada. Algunas de las funciones del proxy son:
  + Filtrado de peticiones y respuestas.
  + Caché
  + Transformación de peticiones y respuestas. 


<a name="http_request"> </a>

### 🟠 HTTP Request (peticiones)

<img src="https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview/http_request.png" alt="http-request">

<a name="http_response"> </a>

### 🟠 HTTP Response (respuestas)

<img src="https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview/http_response.png" alt="http-response">


<a name="practica"> </a>

## 💻 Parte práctica
<a name="funcionamiento_http"> </a>

### 🟠 Funcionamiento HTTP

1️⃣ En la barra de direcciones del navegador, ingrese la siguiente dirección de [Youtube.](https://www.youtube.com/)
  + El navegador envía esa solicitud, es decir, la petición HTTP, al servidor web que administre el dominio youtube.com.
  + El servidor web recibe la solicitud HTTP, busca el archivo en cuestión y envía en primer lugar una cabecera o header. Esta cabecera le comunica al cliente, mediante un código de estado, el resultado de la búsqueda.
  + Si se ha encontrado el archivo solicitado y el cliente ha solicitado recibirlo (y no solo saber si existe), el servidor envía, tras el header, el message bodyo cuerpo del mensaje.

2️⃣ Una vez que des clic, el navegador recibe la y lo abre en forma de página web.
<p align="center">
  <img src="https://media.istockphoto.com/id/458984485/es/foto/youtube-la-p%C3%A1gina-de-primer-plano-con-pantalla-de-lcd-cromo-navegador-web.jpg?s=612x612&w=0&k=20&c=64R3RzXfRlWIWXsKJrHcO04I2vw0YuklkCQkrC-ISoY=" alt="Pagina de YouTube" width="50%">
</p>
<a name="referencias"></a>

## Referencias

* Internet. Retrieved February 10, 2023, from https://www.w3schools.blog/internet
* ¿Qué es el HTTP?. (2020). Retrieved 10 February 2023, from https://www.ionos.es/digitalguide/hosting/cuestiones-tecnicas/protocolo-http/
