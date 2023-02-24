---
remote_theme: chrisrhymes/bulma-clean-theme
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