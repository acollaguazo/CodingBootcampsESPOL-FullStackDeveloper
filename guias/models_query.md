[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Models & Query

<p align="center">
<img src="https://resources.infosecinstitute.com/wp-content/uploads/2022/09/Mongo1.png" width="60%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Modelado de datos](#sinEsquema)
  - [Esquema flexible](#flexible)
  - [Datos incrustados](#datos)
  - [Queries](#queries)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="sinEsquema"> </a>

### 🟠 Modelado de datos

La clave clave en el modelado de datos es equilibrar las necesidades de la aplicación, las características de rendimiento del motor de la base de datos y los patrones de recuperación de datos. Al diseñar modelos de datos, siempre tenga en cuenta el uso de la aplicación de los datos (es decir, consultas, actualizaciones y procesamiento de los datos), así como la estructura inherente de los datos en sí.

<a name="flexible"> </a>

### 🟠 Esquema flexible

A diferencia de las bases de datos SQL, donde debe determinar y declarar el esquema de una tabla antes de insertar datos, las colecciones de MongoDB , por defecto, no requieren que sus documentos tengan el mismo esquema. Eso es:

- No es necesario que los documentos de una sola colección tengan el mismo conjunto de campos y el tipo de datos de un campo puede diferir entre los documentos de una colección.
- Para cambiar la estructura de los documentos en una colección, como agregar nuevos campos, eliminar campos existentes o cambiar los valores de campo a un nuevo tipo, actualice los documentos a la nueva estructura.

Esta flexibilidad facilita la asignación de documentos a una entidad o un objeto. Cada documento puede coincidir con los campos de datos de la entidad representada, incluso si el documento tiene una variación sustancial de otros documentos en la colección.

<a name="datos"> </a>

### 🟠 Datos incrustados

Los documentos incrustados capturan las relaciones entre los datos almacenando los datos relacionados en una única estructura de documento. Los documentos de MongoDB permiten incrustar estructuras de documentos en un campo o matriz dentro de un documento. Estos modelos de datos desnormalizados permiten que las aplicaciones recuperen y manipulen datos relacionados en una sola operación de base de datos.

<p align="center">
<img src="https://www.mongodb.com/docs/manual/images/data-model-denormalized.bakedsvg.svg" width="60%"/>
</p>

<a name="queries"> </a>

### 🟠 Queries

A continuación, se presentarán los métodos para consultar documentos de la colección en MongoDB.

#### 🔹 Método find()

Para consultar datos de la colección MongoDB, debe usar el método find() de MongoDB.

**Sintaxis:**
El método find() mostrará todos los documentos de forma no estructurada. La sintaxis básica del método find() es la siguiente:

```
db.COLLECTION_NAME.find()
``` 

#### 🔹 Método pretty()

Para mostrar los resultados de forma formateada, puede usar el método pretty().

**Sintaxis:**
La sintaxis básica del método pretty() es la siguiente:

```
db.COLLECTION_NAME.find().pretty()
``` 
#### 🔹 Método findOne()

Además del método find(), existe el método findOne() , que devuelve solo un documento.

**Sintaxis:**
La sintaxis básica del método findOne() es la siguiente:

```
db.COLLECTIONNAME.findOne()
```

#### 🔹 Condición AND

Para consultar documentos basados ​​en la condición AND, debe usar la palabra clave $and. La sintaxis básica de AND es la siguiente:

```
db.mycol.find({ $and: [ {<key1>:<value1>}, { <key2>:<value2>} ] })
```
#### 🔹 Condición OR

Para consultar documentos basados ​​en la condición OR, debe usar la palabra clave $or. La sintaxis básica de OR es la siguiente:

```
db.mycol.find(
   {
      $or: [
         {key1: value1}, {key2:value2}
      ]
   }
).pretty()
```

<a name="referencias"></a>

## Referencias

* Data Modeling Introduction. Retrieved May 31, 2023, from [https://www.mongodb.com/docs/manual/core/data-modeling-introduction/](https://www.mongodb.com/docs/manual/core/data-modeling-introduction/)
* Query Documents. Retrieved May 31, 2023, from [https://www.mongodb.com/docs/manual/tutorial/query-documents/](https://www.mongodb.com/docs/manual/tutorial/query-documents/)
* MongoDB - Query Document. Retrieved May 31, 2023, from [https://www.tutorialspoint.com/mongodb/mongodb_query_document.htm#](https://www.tutorialspoint.com/mongodb/mongodb_query_document.htm#)