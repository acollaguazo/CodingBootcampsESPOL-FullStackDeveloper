[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)
# JSON y XML

<p align="center">
<img src="https://phpenthusiast.com/theme/assets/images/blog/what_is_rest_api.png" width="70%" alt="Banner Node.js"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Introducción a RESTs API](#restAPI)
  - [JSON y XML](#jsonXML)
  - [Ventajas de JSON sobre XML](#VentajasjsonXML)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="restAPI"> </a>

### 🟠 Introducción a RESTs API

En esta unidad, introduciremos el tema de un servicio web a nuestra aplicación (no hay razón para que un servidor web y un servicio web no puedan coexistir en la misma aplicación). El término "servicio web" es un término general que significa cualquier interfaz de programación de aplicaciones (API) a la que se puede acceder a través de HTTP. La idea de los servicios web ha existido durante bastante tiempo, pero hasta hace poco, las tecnologías que los permitían eran sofocantes, bizantinas y demasiado complicadas.
Todavía hay sistemas que usan esas tecnologías (como SOAP y WSDL), y hay paquetes de Node que lo ayudarán a interactuar con estos sistemas. Sin embargo, no los cubriremos: en cambio, nos centraremos en proporcionar los llamados servicios "RESTful", que son mucho más sencillos de interactuar.
El acrónimo REST significa "transferencia de estado representacional", y el gramaticalmente problemático "RESTful" se usa como adjetivo para describir un servicio web que satisface los principios de REST. La descripción formal de REST es complicada y está impregnada de formalidad informática, pero lo básico es que REST es una conexión sin estado entre un cliente y un servidor. La definición formal de REST también especifica que el servicio se puede almacenar en caché y que los servicios se pueden superponer (es decir, cuando usa una API REST, puede haber otras API REST debajo).
Desde un punto de vista práctico, las restricciones de HTTP en realidad dificultan la creación de una API que no sea RESTful; tendrías que hacer todo lo posible para establecer el estado, por ejemplo. Así que nuestro trabajo está mayormente recortado para nosotros.

<a name="jsonXML"> </a>

### 🟠 JSON y XML

Es vital para proporcionar una API tener un lenguaje común para hablar. Parte de la comunicación nos la dictan a nosotros: debemos usar métodos HTTP para comunicarnos con el servidor. Pero más allá de eso, somos libres de usar cualquier lenguaje de datos que elijamos. Tradicionalmente, XML ha sido una opción popular y sigue siendo un lenguaje de marcado importante. Si bien XML no es particularmente complicado, Douglas Crockford vio que había espacio para algo más liviano y así nació la notación de objetos de JavaScript (JSON). Además
además de ser muy amigable con JavaScript (aunque de ninguna manera es propietario: es un formato fácil de analizar para cualquier lenguaje), también tiene la ventaja de ser generalmente más fácil de escribir a mano que XML.

<p align="center">
<img src="https://lh4.googleusercontent.com/PiKaxkILS2lp48u_mUG08hNv5vV58kOc2pOAtk5ln3A8uP5yUUjrQOAvnvZ3QVxUVa4mU_4si8vomNrHFTH7leNCWLUrQQRHr-2DAVIdFTz-7y7ptWe00XeBBIIa54X_pQ5WZhs" width="50%" alt="Banner"/>
</p>

<a name="VentajasjsonXML"> </a>

### 🟠 Ventajas de JSON sobre XML

* JSON suele ser más pequeño en tamaño que XML.
* JSON suele ser más legible para personas, ya que se basa en pares clave-valor y usa notación de objetos y matrices. XML, por otro lado, puede ser más complejo de leer debido a sus etiquetas y anidamientos.
* JSON tiene una sintaxis más sencilla y concisa que XML.
* JSON es nativo de JavaScript, por lo que se integra de manera más natural con esta lengua de programación en comparación con XML.
* Muchas aplicaciones y plataformas ofrecen soporte nativo para JSON, lo que facilita su uso en estas herramientas.

<p align="center">
<img src="https://lordicon.com/icons/wired/outline/1320-json.gif" width="40%" alt="Banner"/>
</p>