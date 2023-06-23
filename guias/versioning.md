[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Versioning

<p align="center">
<img src="https://procodeguide.b-cdn.net/wp-content/uploads/2020/06/ASP.NET-Core-Web-API-Versioning-1024x624.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Control de versiones](#comments)
  - [Implementación de versiones de API](#usar)
    - [Control de versiones basado en URL](#usarD)
    - [Control de versiones basado en encabezado](#usrD)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Control de versiones

Al momento de implementar la API será crucial hacer uso del control de versiones del API. 
Un escenario que requiere el control de versiones del API es cuando la implementación afecta a las solicitudes y respuestas del API existente y por ende el cliente no puede consumir los recursos porque se ha cambiado la integración de la API. 

<a name="usar"> </a>

### 🟠 Implementación de versiones de API

Para la implementación de versiones de API existen varios enfoques. De forma general, el proveedor de servicios de API necesita un indicador en la solicitud de API para comprender qué versión necesita el consumidor de API. A continuación, se describirán dos de los principales enfoques. 

  * Control de versiones basado en URL.
  * Control de versiones basado en encabezados.

Estos 2 enfoques tienen sus pros y sus contras cuando se trata de la implementación. Depende de sus requerimientos y del enfoque que se ajuste a sus necesidades.

<a name="usarD"> </a>

### 🟠 Control de versiones basado en URL

Como sugiere el nombre, el control de versiones basado en URL incluye la versión en la URL de solicitud de API. Es posible que vea una URL como [https://example.com/api/v1/holamundo](https://example.com/api/v1/holamundo). Este es un enfoque sencillo para el control de versiones de API. El consumidor de API puede identificar fácilmente la versión mirando la URL. Con el número de versión incluido en la URL, también será más fácil si necesita almacenar en caché la respuesta de la API.

<a name="usrD"> </a>

### 🟠 Control de versiones basado en encabezado

La ventaja de esta implementación es que continúa manteniendo la misma URL para las 2 versiones del código. Además, no necesita 2 controladores de procesos para mantener las 2 implementaciones. Será más fácil si necesita mantener una lógica común dentro del mismo archivo JS.

<a name="referencias"></a>

## Referencias

* API Versioning with Node.JS. Retrieved June 10, 2023, from [https://medium.com/@pengyeng/api-versioning-with-node-js-47ddd2956715](https://medium.com/@pengyeng/api-versioning-with-node-js-47ddd2956715)