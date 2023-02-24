---
remote_theme: daviddarnes/alembic@main
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Arquitectura de aplicaciones web

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Arquitectura de aplicaciones web](#arquitectura)
  - [Componentes de la arquitectura web](#componentes)
    - [Cliente](#cliente)
    - [Servidor](#servidor)
    - [Proxy](#proxy)
  - [Arquitectura cliente-servidor](#cliente_servidor)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="arquitectura"> </a>

### 🟠 Arquitectura de aplicaciones web

La arquitectura de aplicaciones web es un conjunto de componentes que comprende la interacción lógica. Además, se compone de las interacciones y relaciones entre los elementos de la aplicación, como las interfaces de usuario, los sistemas de middleware y las bases de datos.

<a name="componentes"> </a>

### 🟠 Componentes de la arquitectura web

Los componentes de la arquitectura web son: cliente, servidor y proxy. 

<a name="cliente"> </a>

#### 🔹 Cliente

Los clientes son los que originan el trafico web, es decir envían las peticiones y reciben las respuestas. Los navegadores son un tipo de cliente web. El navegador tiene la capacidad de interpretar varios lenguajes de programación especialmente creados para la visualización y maquetación de contenido. 
<p align="center">
  <img src="https://cdn.computerhoy.com/sites/navi.axelspringer.es/public/media/image/2021/07/navegadores-2397647.jpg?tf=1920x" alt="cliente-servidor" width="50%">
</p>

<a name="servidor"> </a>

#### 🔹 Servidor

El servidor es un software especializado que esta a la espera de peticiones de recursos web por el lado del cliente. Las acciones que realiza el servidor son:
  + Conexión con el cliente.
  + Recepta el mensaje HTTP de la petición.
  + Procesa el mensaje HTTP.
  + Localiza y envía el resultado (en forma de mensaje HTTP). 

<a name="proxy"> </a>

#### 🔹 Proxy

Un proxy es un intermediario entre el cliente y el servidor, Realizan simultáneamente el papel de servidor y cliente; con el fin de reducir comunicación no deseada. Algunas de las funciones del proxy son:
  + Filtrado de peticiones y respuestas.
  + Caché
  + Transformación de peticiones y respuestas. 

<a name="cliente_servidor"> </a>

### 🟠 Arquitectura cliente-servidor

El modelo cliente-servidor es una arquitectura software
que involucra uno o más clientes solicitando servicios a
uno o más servidores. La separación entre cliente y servidor es una separación de tipo lógico, donde el servidor no se ejecuta necesariamente sobre una sola máquina ni es necesariamente un sólo programa. Los tipos específicos de servidores incluyen los servidores web, los servidores de archivo, los servidores del correo, etc. Mientras que sus propósitos varían de unos servicios a otros, la arquitectura básica seguirá siendo la misma.

<p align="center">
  <img src="https://static.wixstatic.com/media/1899d0_a19fc771edff4ca89be429574e681f95.jpg/v1/fill/w_521,h_397,al_c,lg_1,q_80,enc_auto/1899d0_a19fc771edff4ca89be429574e681f95.jpg" alt="cliente-servidor" width="50%">
</p>

<a name="referencias"></a>

## Referencias

* Arquitectura Cliente-Servidor. Retrieved February 10, 2023, from https://reactiveprogramming.io/blog/es/estilos-arquitectonicos/cliente-servidor
