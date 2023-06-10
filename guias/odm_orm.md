[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# ODM/ORM

<p align="center">
<img src="https://resources.infosecinstitute.com/wp-content/uploads/2022/09/Mongo1.png" width="60%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [ODM](#odm)
  - [ORM](#orm)
  - [ORM vs ODM](#orm-odm)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="orm"> </a>

### 🟠 ORM

ORM significa Mapeo Relacional de Objetos. ORM es una técnica utilizada para la consultar o realizar operaciones CRUD(Crear, Leer, Actualizar, Eliminar) a la base de datos, en especial RDBMS(Bases de Datos Relacionales) que utiliza un paradigma orientado a objetos.
Con ORM no se necesita usar SQL , ya que se puede interactuar directamente con la base de datos y por ende realizar consultas para su código back-end. 

<p align="center">
<img src="https://i0.wp.com/hanamon.kr/wp-content/uploads/2021/09/ORM.png?resize=601%2C306&ssl=1" width="60%"/>
</p>

<a name="odm"> </a>

### 🟠 ODM

ODM significa mapeo de documentos de objetos. Es como un ORM pero en este caso para bases de datos no relacionales o distribuidas como MongoDB, es decir, mapeando un modelo de objetos y una base de datos NoSQL.

Por otro lado, es importante tener en consideración que en las bases de datos NoSQL orientadas a documentos, los documentos se almacenan en formato json en la colección (una tabla en las bases de datos SQL es como una colección en las bases de datos NoSQL).


<a name="orm-odm"> </a>

### 🟠 ORM vs ODM

* En bases a las definiciones anteriores tenemos que la principal diferencia entre ORM y ODM es el tipo de base de datos para el que se utilizan estos mapeadores de datos.
    - Para base de datos relacional como MySQL o PostgresSQL se usa ORM. En cambio, para base de datos no relacionales con MongoDB, Cassandra o Redis, se usa ODM.
<p align="center">
<img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*6VVjUEphkSkbu_Zcqn0Dyg.png" width="60%"/>
</p>

**Bases de datos relacionales y no relacionales**

A continuación, se describirán dos criterios para saber elegir el tipo de bases de datos. 

* **Depende del tipo de datos que usará.** 
Si sus datos caben cómodamente en filas y columnas, use una base de datos relacional. Si sus datos necesitan un espacio flexible, una base de datos no relacional sería una mejor opción para lograr sus objetivos.

* **Cuanto más grande sea el conjunto de datos:**

Las bases de datos no relacionales pueden almacenar conjuntos ilimitados de datos de cualquier tipo y tienen la flexibilidad de cambiar el tipo de datos. Pero las bases de datos relacionales funcionan mejor cuando se realizan operaciones intensivas de lectura/escritura en conjuntos de datos pequeños o medianos.

<a name="referencias"></a>

## Referencias

* ORM and ODM — A Brief Introduction. Retrieved May 31, 2023, from [https://medium.com/spidernitt/orm-and-odm-a-brief-introduction-369046ec57eb#ef3c](https://medium.com/spidernitt/orm-and-odm-a-brief-introduction-369046ec57eb#ef3c)