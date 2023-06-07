[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Schemaless DB Design

<p align="center">
<img src="https://resources.infosecinstitute.com/wp-content/uploads/2022/09/Mongo1.png" width="60%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Base de datos sin esquema](#sinEsquema)
  - [Funcionamiento de la base de datos sin esquema](#funcionamiento)
  - [Beneficios del uso de bases de datos sin esquema](#beneficios)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="sinEsquema"> </a>

### 🟠 Base de datos sin esquema

Las bases de datos relacionales tradicionales están bien definidas y utilizan un esquema para describir cada elemento funcional, incluidas tablas, vistas de filas, índices y relaciones. Al ejercer un alto grado de control, el administrador de la base de datos puede mejorar el rendimiento y evitar la captura de datos de baja calidad, incompletos o con formato incorrecto. En una base de datos SQL, el sistema de administración de bases de datos relacionales (RDBMS) aplica el esquema cada vez que se escriben datos en el disco.
Por otro lado, Una base de datos sin esquema, como MongoDB, no tiene estas restricciones iniciales y se asigna a una base de datos más "natural". Incluso cuando se encuentra sobre un lago de datos, cada documento se crea con un esquema parcial para facilitar la recuperación. Cualquier esquema formal se aplica en el código de sus aplicaciones; esta capa de abstracción protege los datos sin procesar en la base de datos NoSQL y permite una transformación rápida a medida que cambian sus necesidades.

<a name="funcionamiento"> </a>

### 🟠 Funcionamiento de la base de datos sin esquema

En las bases de datos sin esquema, la información se almacena en documentos de estilo JSON que pueden tener varios conjuntos de campos con diferentes tipos de datos para cada campo.

```json
    { 
        name : “Joel”, age : 20, interests : ‘tennis’ 
    }
    { 
        name : “Luisa”, age : 23 
    }
```
Con la base de datos MongoDB sin esquema, existe una estructura adicional: el espacio de nombres del sistema contiene una lista explícita de colecciones e índices. 

<a name="beneficios"> </a>

### 🟠 Beneficios del uso de bases de datos sin esquema

A continuación, se muestran un serie de beneficios que se tendrán al momento de usar base de datos sin esquema.

* Mayor flexibilidad sobre los tipos de datos.
* Sin esquemas de base de datos predefinidos.
* Sin truncamiento de datos.
* Adecuado para funciones de análisis en tiempo real.
* Escalabilidad y flexibilidad mejoradas.

<a name="referencias"></a>

## Referencias

* What is a Schemaless Database?. Retrieved May 31, 2023, from [https://www.mongodb.com/unstructured-data/schemaless#:~:text=Is%20MongoDB%20schemaless%3F,explicitly%20listing%20collections%20and%20indexes.](https://www.mongodb.com/unstructured-data/schemaless#:~:text=Is%20MongoDB%20schemaless%3F,explicitly%20listing%20collections%20and%20indexes.)
