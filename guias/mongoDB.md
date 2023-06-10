[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# MongoDB

<p align="center">
<img src="https://webimages.mongodb.com/_com_assets/cms/kuzt9r42or1fxvlq2-Meta_Generic.png" width="60%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [¿Qué es MongoDB?](#comments)
    - [¿Qué son los documentos?](#url)
    - [¿Qué es una collection?](#col)
    - [¿Qué es una base de datos?](#base)
  - [¿Porque usar MongoDB?](#usar)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 ¿Qué es MongoDB?

* MongoDB es un documento y una base de datos NoSQL.
* En lugar de almacenar datos en tablas de filas o columnas como bases de datos SQL, cada registro en una base de datos MongoDB es un documento, y almacena los datos en una forma no relacional.

<a name="url"> </a>

#### 🔹 ¿Qué son los documentos?

Los documentos son matrices asociativas como objetos JSON o diccionarios de Python.
Por ejemplo, un documento de estudiante:

``` json
"firstName" : "John",
"lastName" : "Doe",
"email" : "john.doe@email.com",
``` 
<p align="center">
<img src="https://webimages.mongodb.com/_com_assets/cms/1-lwnlfl1ryn.png?auto=format%2Ccompress&ch=DPR" width="60%"/>
</p>

<a name="col"> </a>

#### 🔹 ¿Qué es una collection?

Los documentos MongoDB de tipo similar se agrupan en una colección.

<a name="base"> </a>

#### 🔹 ¿Qué es una base de datos?

Siguiendo nuestro ejemplo anterior, el sistema de gestión del campus almacena todos los diferentes tipos de datos relacionados con él en una base de datos MongoDB llamada Campus Management DB.

MongoDB admite una variedad de tipos de datos, por lo que tiene la capacidad total de usar el tipo de datos correcto para almacenar su información. Por ejemplo:

```json
"dateofBirth" : ISODate("2000-01-01T14:45:00.000Z"),
"balance" : 20.01
``` 
<a name="organizacion"> </a>

#### 🔹 Organización de los datos en MongoDB

En resumen, los cuatro atributos que sa MongoDB para orgnaizar los datos son:

* **Base de datos :** una organización de información que le permite almacenar, consultar y administrar datos
* **Colección:** — Un almacén organizado de documentos. Las colecciones contienen uno o más documentos.
* **Documento :** un almacén organizado de clave/valor de conjuntos de datos organizados por pares clave/valor
* **Par clave/valor :** un conjunto de atributos que representan un punto de datos de un documento en particular.

<a name="comments"> </a>

### 🟠 ¿Porque usar MongoDB?

* Trabajar con MongoDB es fácil porque puede concentrarse en los datos que está escribiendo y cómo los va a leer.
* Las bases de datos relacionales tradicionales requerían que primero creara el esquema y luego creara estructuras de tablas que contendrán sus datos. Por lo tanto, si decide almacenar un campo adicional, tendrá que modificar sus tablas.
* MongoDB también le brinda el poder de traer cualquier dato estructurado o no estructurado.
* MongoDB también brinda alta disponibilidad al mantener varias copias de sus datos, que trataremos en temas posteriores.
* Puede diseñar estructuras de datos complejas fácilmente en MongoDB sin preocuparse por la complejidad de cómo se almacenan y cómo deben vincularse.
* MongoDB es una opción popular de base de datos por:
    - Grande y desestructurado
    - Flexible
    - Aplicaciones altamente escalables
    - Autogestionado, híbrido o alojado en la nube