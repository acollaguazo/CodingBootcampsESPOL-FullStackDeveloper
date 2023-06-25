[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# CDN

<p align="center">
<img src="https://flaviocopes.com/images/cdn/cdn-how-it-works.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [CDN](#comments)
  - [Ventajas de usar un CDN](#usar)
  - [Herramientas y bibliotecas necesarias construir una CDN](#usarH)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 CDN

El rendimiento en las aplicaciones web es primordial para brindar una experiencia de usuario excepcional.  Las redes de entrega de contenido (CDN) se han convertido en una herramienta indispensable para lograr un rendimiento óptimo, asegurando que el contenido web se entregue de manera rápida y eficiente a los usuarios de todo el mundo. 
Los proveedores más populares son:

* Cloudflare
* Akamai
* Amazon CloudFront

<a name="usar"> </a>

### 🟠 Ventajas de usar un CDN

* Rendimiento mejorado
* Escalabilidad
* Fiabilidad mejorada
* Reducción de la carga del servidor
* Alcance global

<a name="usarH"> </a>

### 🟠 Herramientas y bibliotecas necesarias construir una CDN

Para crear su CDN personalizado con Node.js, necesitará varias herramientas y bibliotecas para ayudarlo en el camino.

1. Node.js
2. NPM (Node Package Manager)
3. Express
4. Bibliotecas adicionales
En base a los requisitos específicos de CDN, es posible que deba instalar y usar otras bibliotecas, como las de almacenamiento en caché (por ejemplo, Redis o Memcached), equilibrio de carga o funciones de seguridad.

Los primeros pasos para crear una CDN con Nodejs son:

* Inicialice un nuevo proyecto de Node.js ejecutando el siguiente comando:

```
npm init -y
```
El comando anterior creará un archivo `package.json` en el directorio de su proyecto, que almacenará información sobre su proyecto y sus dependencias.

* En relación a la instalación de Express y otras bibliotecas necesarias, ya con el proyecto inicializado, ahora puede instalar Express, el marco web que usará para crear su CDN personalizado. Ejecute el siguiente comando:

```
npm install express
```
Según los requisitos específicos de su CDN, es posible que deba instalar bibliotecas adicionales para el almacenamiento en caché, el equilibrio de carga, la seguridad u otras funciones. Utilice NPM para buscar e instalar estas bibliotecas según sea necesario.

Por ejemplo, si planea usar Redis para el almacenamiento en caché. Ejecute el siguiente comando:

```
npm install redis
```
Ahora que ha configurado su entorno de desarrollo, está listo para comenzar a crear su CDN personalizado con Node.js. 


<a name="referencias"></a>

## Referencias

* Build a High-Performance Custom Content Delivery Network (CDN) with Node.js. Retrieved May 12, 2023, from [https://voskan.host/2023/04/09/build-a-high-performance-custom-content-delivery-network-cdn-with-node-js/#:~:text=A%20CDN%20is%20a%20system,geographically%20closest%20to%20their%20location.](https://voskan.host/2023/04/09/build-a-high-performance-custom-content-delivery-network-cdn-with-node-js/#:~:text=A%20CDN%20is%20a%20system,geographically%20closest%20to%20their%20location.)