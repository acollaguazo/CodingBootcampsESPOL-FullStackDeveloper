[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Sending client data to the server

## Contenido

- [Fundamentos te贸ricos](#fundamentos_teoricos)
  - [Introducci贸n](#introduccion)
  - [Sending client data to the server](#sending_client_data)
    - [Querystring](#querystring)
    - [Request body](#request_body)
  - [Consideraciones](#consideraciones)
- [Parte pr谩ctica](#practica)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 馃搼 Fundamentos te贸ricos

<a name="introduccion"> </a>

### 馃煚 Introducci贸n

La forma habitual de recopilar informaci贸n de sus usuarios es mediante formularios HTML. Ya sea que permita que el navegador env铆e el formulario normalmente, use AJAX o emplee controles sofisticados, el mecanismo subyacente generalmente sigue siendo un formulario HTML.

<p align="center">
<img src="https://images01.nicepagecdn.com/page/17/91/es/plantilla-html-preview-179165.jpg" width="70%"/>
</p>

<a name="sending_client_data"> </a>

### 馃煚 Sending client data to the server

Para el env铆o de datos del cliente al servidor, existen 2 opciones: querystring y request body.

<a name="querystring"> </a>

#### 馃敼 Querystring

Querystring le permite pasar informaci贸n hacia y desde un sitio web simplemente agregando o "adjuntando" esa informaci贸n al final de una URL. Esta informaci贸n se almacena en la cadena de consulta y el sitio web la captura cuando lee la URL. Es decir, se est谩 realizando una solicitud GET.

<a name="request_body"> </a>

#### 馃敼 Request body

Request body utiliza una solicitud POST. El m茅todo POST  utiliza el navegador para comunicarse con el servidor cuando solicita una respuesta que tenga en cuenta los datos proporcionados en el cuerpo de la solicitud HTTP. 

<a name="consideraciones"> </a>

### 馃煚 Consideraciones

+ Es una percepci贸n err贸nea com煤n que POST es seguro y GET no lo es: en realidad, ambos son seguros si usa HTTPS.

+ Si no est谩 utilizando HTTPS, un intruso puede mirar los request body para un POST tan f谩cilmente como querystring de una solicitud GET. 

+ Si utiliza solictudes GET, los usuarios ver谩n todas sus entradas en la querystring (incluido los campos ocultos). 

+ Generalmente se recomienda usar POST para enviar formularios. 
<a name="practica"> </a>

## 馃捇 Parte pr谩ctica


<a name="referencias"></a>

## Referencias

* Querystring. Retrieved February 21, 2023, from https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/standard-elements/passing-information-through-query-strings/ 
* Sendind form data. (2020). Retrieved 21 February 2023, from https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data 