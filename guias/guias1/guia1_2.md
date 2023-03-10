---
remote_theme: pages-themes/architect@v0.2.0
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Arquitectura de aplicaciones web

## Contenido

- [Fundamentos te贸ricos](#fundamentos_teoricos)
  - [Arquitectura de aplicaciones web](#arquitectura)
  - [Componentes de la arquitectura web](#componentes)
    - [Cliente](#cliente)
    - [Servidor](#servidor)
    - [Proxy](#proxy)
  - [Arquitectura cliente-servidor](#cliente_servidor)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 馃搼 Fundamentos te贸ricos

<a name="arquitectura"> </a>

### 馃煚 Arquitectura de aplicaciones web

La arquitectura de aplicaciones web es un conjunto de componentes que comprende la interacci贸n l贸gica. Adem谩s, se compone de las interacciones y relaciones entre los elementos de la aplicaci贸n, como las interfaces de usuario, los sistemas de middleware y las bases de datos.

<a name="componentes"> </a>

### 馃煚 Componentes de la arquitectura web

Los componentes de la arquitectura web son: cliente, servidor y proxy. 

<a name="cliente"> </a>

#### 馃敼 Cliente

Los clientes son los que originan el trafico web, es decir env铆an las peticiones y reciben las respuestas. Los navegadores son un tipo de cliente web. El navegador tiene la capacidad de interpretar varios lenguajes de programaci贸n especialmente creados para la visualizaci贸n y maquetaci贸n de contenido. 
<p align="center">
  <img src="https://cdn.computerhoy.com/sites/navi.axelspringer.es/public/media/image/2021/07/navegadores-2397647.jpg?tf=1920x" alt="cliente-servidor" width="50%">
</p>

<a name="servidor"> </a>

#### 馃敼 Servidor

El servidor es un software especializado que esta a la espera de peticiones de recursos web por el lado del cliente. Las acciones que realiza el servidor son:
  + Conexi贸n con el cliente.
  + Recepta el mensaje HTTP de la petici贸n.
  + Procesa el mensaje HTTP.
  + Localiza y env铆a el resultado (en forma de mensaje HTTP). 

<a name="proxy"> </a>

#### 馃敼 Proxy

Un proxy es un intermediario entre el cliente y el servidor, Realizan simult谩neamente el papel de servidor y cliente; con el fin de reducir comunicaci贸n no deseada. Algunas de las funciones del proxy son:
  + Filtrado de peticiones y respuestas.
  + Cach茅
  + Transformaci贸n de peticiones y respuestas. 

<a name="cliente_servidor"> </a>

### 馃煚 Arquitectura cliente-servidor

El modelo cliente-servidor es una arquitectura software
que involucra uno o m谩s clientes solicitando servicios a
uno o m谩s servidores. La separaci贸n entre cliente y servidor es una separaci贸n de tipo l贸gico, donde el servidor no se ejecuta necesariamente sobre una sola m谩quina ni es necesariamente un s贸lo programa. Los tipos espec铆ficos de servidores incluyen los servidores web, los servidores de archivo, los servidores del correo, etc. Mientras que sus prop贸sitos var铆an de unos servicios a otros, la arquitectura b谩sica seguir谩 siendo la misma.

<p align="center">
  <img src="https://static.wixstatic.com/media/1899d0_a19fc771edff4ca89be429574e681f95.jpg/v1/fill/w_521,h_397,al_c,lg_1,q_80,enc_auto/1899d0_a19fc771edff4ca89be429574e681f95.jpg" alt="cliente-servidor" width="50%">
</p>

<a name="referencias"></a>

## Referencias

* Arquitectura Cliente-Servidor. Retrieved February 10, 2023, from https://reactiveprogramming.io/blog/es/estilos-arquitectonicos/cliente-servidor
