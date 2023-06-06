[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Patrón de Arquitectura MVC

<p align="center">
<img src="https://www.easyappcode.com/upload/post-792545902.jpg" width="60%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Patrón de Arquitectura MVC](#comments)
  - [Fundamento de MVC](#mvc)
  - [Ejemplo de MVC](#ejmvc)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Patrón de Arquitectura MVC

Uno de los paradigmas de desarrollo más populares que ha cobrado importancia en los últimos años es el patrón modelo-vista-controlador (MVC). Este es un concepto bastante antiguo, en realidad, que se remonta a la década de 1970. Ha experimentado un resurgimiento gracias a su idoneidad para el desarrollo web.

<a name="mvc"> </a>

### 🟠 Fundamento de MVC

A continuación, se describirán las tres partes del patron de arquitectura MVC:

* **1. Modelo:** 

El modelo es una vista "pura" de sus datos y lógica. No se preocupa en absoluto de la interacción del usuario.

* **2. Vista:** 

Las vistas transmiten modelos al usuario, y el controlador acepta la entrada del usuario, manipula los modelos y elige qué vista(s) mostrar.

* **3. Controlador:** 

Enruta comandos a los modelos y vistas.

<a name="ejmvc"> </a>

### 🟠 Ejemplo de MVC

El ejemplo se basa en una aplicación de lista de compras, en la se requiere tener los siguientes datos: nombre del artículo, cantidad, precio, entre otros. A continuación, se muestra gráficamente como sería la implementación usando MVC.

<p align="center">
<img src="https://developer.mozilla.org/en-US/docs/Glossary/MVC/model-view-controller-light-blue.png
" width="70%"/>
</p>

**Modelo**

En la aplicación de lista de compras, el modelo especificará qué datos deben contener los artículos de la lista (artículo, precio, etc.) y qué artículos de la lista ya están presentes.

**Vista**

En la aplicación de lista de compras, la vista definiría cómo se presenta la lista al usuario y recibiría los datos para mostrar desde el modelo.

**Controlador**

En la aplicación de lista de compras, uestra lista de compras podría tener formularios de entrada y botones que nos permitan agregar o eliminar artículos. Estas acciones requieren que se actualice el modelo, por lo que la entrada se envía al controlador, que luego manipula el modelo según corresponda, que luego envía datos actualizados a la vista.

<a name="referencias"></a>

## Referencias

* Brown, E. (2014). Web Development with Node and Express. Sebastopol, CA: O'Reilly Media.

* MVC. Retrieved May 31, 2023, from [https://developer.mozilla.org/es/docs/Glossary/MVC](https://developer.mozilla.org/es/docs/Glossary/MVC)