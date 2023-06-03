[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)


# Server-side templates

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Server-side templates](#server_side_template)
  - [Características](#caracteristica)
  - [Ejemplo de server-side templates](#ejemplo)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="server_side_template"> </a>

### 🟠 Server-side templates

Las plantillas del lado del servidor le permiten renderizar HTML antes de enviarlo al cliente. A diferencia de las plantillas del lado del cliente, donde las plantillas están disponibles para el usuario curioso que sabe cómo ver el código fuente HTML, sus usuarios nunca verán su plantilla del lado del servidor o los objetos de contexto utilizados para generar el HTML final.

<a name="caracteristica"> </a>

### 🟠 Características

+ Ocultan detalles de implementación.
+ Soporte de almacenamiento en caché.
    + El motor de plantillas almacenará en caché las plantillas compiladas (solo las volverá a compilar y almacenar en caché cuando cambie la plantilla), lo que mejorará el rendimiento de las vistas con plantilla. 
    + De forma predeterminada, el almacenamiento en caché de vistas es deshabilitado en el modo de desarrollo y habilitado en el modo de producción.

<a name="ejemplo"> </a>

### 🟠 Ejemplo de server-side templates

Express es compatible desde el primer momento con Jade, EJS y JSHTML. Por lo tanto, necesitaremos agregar un paquete de nodos que brinde compatibilidad con Handlebars para Express.

```
npm install --save express3-handlebars
```
Luego se debe vincular a Express.

```js
var handlebars = require('express3-handlebars')
.create({ defaultLayout: 'main' });
app.engine('handlebars', handlebars.engine);
app.set('view engine', 'handlebars');
```



<a name="referencias"></a>

## Referencias

* Server-side templates. Retrieved February 21, 2023, from https://www.oreilly.com/library/view/node-for-front-end/9781449329112/ch04.html 