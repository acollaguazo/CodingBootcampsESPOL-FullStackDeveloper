# Web Sockets

<img src="https://www.holdapp.com/wp-content/uploads/2021/03/WebSockets-cover.png" alt="Banner  Web Sockets"/>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Web Sockets](#web_sockets)
  - [Utilización de web socket](#utilidad_socket)
  - [Ventajas de web socket](#ventaja_socket)
  - [Ejemplos de uso web socket](#ejemplo_socket)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="web_sockets"> </a>

### 🟠 Web Sockets

WebSocket es un protocolo de red basado en TCP que establece cómo deben intercambiarse datos entre redes. Puesto que es un protocolo fiable y eficiente, es utilizado por prácticamente todos los clientes. El protocolo TCP establece conexiones entre dos puntos finales de comunicación, llamados sockets. De esta manera, el intercambio de datos puede producirse en las dos direcciones.

<a name="utilidad_socket"> </a>

### 🟠 Utilización de web socket

Se utiliza WebSocket siempre que se trate de establecer conexiones de forma rápida. Es el caso, por ejemplo, de los chats de asistencia técnica, de los tickers de noticias o de actualizaciones de bolsa en directo, de los servicios de mensajería instantánea y de los juegos en tiempo real. En las redes sociales también resulta muy útil WebSocket: para establecer conexiones en directo con otras personas.

<p align="center">
  <img src="data:image/png;base64,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" width="50%">
</p>

<a name="ventaja_socket"> </a>

### 🟠 Ventajas de web socket

WebSocket tiene la ventaja de crear conexiones bidireccionales que permiten el intercambio de datos en ambos sentidos, lo cual hace posible el contacto directo con el navegador y, con ello, permite cortos periodos de carga: en cuanto se envía un mensaje, como podría ser uno en un chat de soporte técnico, este llega y se muestra directamente al otro lado.

<p align="center">
  <img src="https://geekflare.com/wp-content/uploads/2022/10/Websocket-Servers-for-Reliable-Real-time-Applications.png" alt="ventaja socket" width="50%">
</p>

<a name="ejemplo_socket"> </a>

### 🟠 Ejemplos de uso web socket

Hoy en día, son muchos los ámbitos que requieren una conexión en tiempo real entre el cliente y el servidor para poder así ofrecer sus servicios sin complicaciones. Algunos de estos campos de aplicación son los siguientes:
  + Juegos en línea.
  + Plataformas de compra y de venta, como eBay.
  + Chats de atención al usuario.
  + Tickers de noticias deportivas en directo.
  + Actualizaciones en tiempo real de las redes sociales 

<p align="center">
  <img src="https://cloudfront-us-east-1.images.arcpublishing.com/infobae/SZJGOOHWPZC4VMGDJGPUECCJH4.jpg" alt="ejemplo socket" width="50%">
</p>

<a name="referencias"></a>

## Referencias

* ¿Qué es WebSocket?. Retrieved February 11, 2023, from https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/que-es-websocket/
