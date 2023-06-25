[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Cache

<p align="center">
<img src="https://progressivecoder.com/wp-content/uploads/2023/01/image-2.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Almacenamiento en caché](#comments)
  - [¿Por qué almacenar datos en caché?](#usar)
  - [Tipos de almacenamiento en caché de bases de datos](#usarT)
  - [Paquetes comunes de almacenamiento en caché](#usarP)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Almacenamiento en caché

En el desarollo web se necesita usar una técnica de almacenamiento en caché. Esto nos beneficiara en el aspecto de manejar los cuellos de botella de rendimiento relacionados con la forma en que se administran, almacenan y recuperan los datos.

El caché es un servidor de almacenamiento secundaria, generalmente más rápida y de alto rendimiento para almacenar temporalmente un subconjunto de datos. Se espera que los datos almacenados en un caché no cambien con frecuencia.

Una de las ventajas de la caché es que las solicitudes que se realicen se respondan mucho más rápido debido  a la ubicación de la caché en relación a la ubicación de almacenamiento principal de los datos (generalmente una base de datos). 

El almacenamiento en caché proporciona una forma más eficiente de reutilizar datos previamente recuperados o calculados.

<a name="usar"> </a>

### 🟠 ¿Por qué almacenar datos en caché?

El almacenamiento en caché generalmente se recomienda para los casos en los que el estado de los datos en un punto particular de la aplicación rara vez cambia. Casos como:

* Listas de productos
* Códigos de llamadas de países
* Ubicaciones de tiendas

En los casos anteriores, se necesitaria de una función para obtener la lista de bancos de una API externa y almacenar la respuesta en un caché. Esto significa que, posteriormente, no necesitaremos hacer esa misma llamada a la API a través de Internet; más bien, podemos simplemente recuperar los datos de nuestro caché ya que no esperaríamos que cambie repentinamente.

Con los sistemas de almacenamiento en caché, los procesos de recuperación de datos ya están optimizados porque los datos se almacenan en la memoria.

<a name="usarT"> </a>

### 🟠 Tipos de almacenamiento en caché de bases de datos

El tipo o enfoque para el almacenamiento en caché de datos depende en gran medida de los tipos de caché (que pueden caer en el nivel de la aplicación o el almacenamiento en caché local, el almacenamiento en caché integrado en la base de datos y el almacenamiento en caché independiente o remoto) y en el objetivo de la configuración de caché de la aplicación en cuestión. Si bien el nivel de aplicación o el almacenamiento en caché local es beneficioso porque la base de datos puede actualizar su caché automáticamente cuando cambian los datos subyacentes, el caché puede estar limitado en términos de tamaño y disponibilidad de memoria o recursos.

<a name="usarP"> </a>

### 🟠 Paquetes comunes de almacenamiento en caché

Entre los paquetes de almacenamiento en caché están:

* node-cache
* memcache
* flat-cache
* cacache

### 🟠 Node-cache

Node-cachees un módulo de almacenamiento en caché interno de nodo interno simple que tiene set, gety deletemétodos similares a otras bibliotecas de almacenamiento en caché. Está disponible en npm y se puede instalar con el comando:

```
npm install node-cache --save
```

Para la inicialización de la biblioteca se usa:

```js
const NodeCache = require ( "node-cache" ); 
const myCache = new NodeCache ();      
```
Luego podemos proceder a almacenar una clave usando el setmétodo. El formato para configurar un par clave/valor con un TTL (en segundos) se muestra a continuación:

```js
myCache.set( key, val, [ ttl ] )
```

Si tiene éxito, devolverá true.

<a name="referencias"></a>

## Referencias

* Caching in Node.js to optimize app performance. Retrieved June 10, 2023, from [https://blog.logrocket.com/caching-node-js-optimize-app-performance/#:~:text=Caching%20is%20basically%20a%20layer,optimized%20for%20that%20particular%20purpose.](https://blog.logrocket.com/caching-node-js-optimize-app-performance/#:~:text=Caching%20is%20basically%20a%20layer,optimized%20for%20that%20particular%20purpose.)