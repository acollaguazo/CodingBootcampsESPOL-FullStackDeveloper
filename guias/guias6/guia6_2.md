[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Session

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Session](#session)
  - [Fases de una session](#fases)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="session"> </a>

### 🟠 Session

Las sesiones son realmente una forma más conveniente de mantener el estado. Para implementar sesiones, se debe almacenar algo en el cliente; de lo contrario, el servidor no podría identificar al cliente de una solicitud a la siguiente. El método habitual para hacer esto es una cookie que
contiene un identificador único. Luego, el servidor usa ese identificador para recuperar la información de sesión adecuada.

<a name="fases"> </a>

### 🟠 Fases de una session

En los protocolos basados en el modelo cliente-servidor, como es el caso del HTTP, una sesión consta de tres fases:

1. El cliente establece una conexión TCP (o la conexión correspondiente si la capa de transporte corresponde a otro protocolo).
2. El cliente manda su petición, y espera por la respuesta.
3. El servidor procesa la petición, y responde con un código de estado y los datos correspondientes.

Las cookies no son la única forma de lograr esto: durante el apogeo del "miedo a las cookies" (cuando el abuso de las cookies era desenfrenado), muchos usuarios simplemente desactivaban las cookies y se idearon otras formas de mantener el estado, como decorar las URL con información de la sesión. Estas técnicas eran complicadas, difíciles e ineficaces, y era mejor dejarlas en el pasado. HTML5 proporciona otra opción para las sesiones, llamada almacenamiento local, pero actualmente no hay una razón convincente para usar esta técnica sobre las cookies probadas y verdaderas.
En términos generales, hay dos formas de implementar sesiones: almacenar todo en la cookie o almacenar solo un identificador único en la cookie y todo lo demás en el servidor.
Las primeras se denominan "sesiones basadas en cookies" y simplemente representan una conveniencia sobre el uso de cookies. Sin embargo, todavía significa que todo lo que agregue a la sesión se almacenará en el navegador del cliente, lo cual es un enfoque que no recomiendo. Recomendaría este enfoque solo si sabe que almacenará solo una pequeña cantidad de información, que no le importa que el usuario tenga acceso a la información y que no crecerá fuera de control con el tiempo. Si desea adoptar este enfoque, consulte [cookie-session](https://www.npmjs.com/package/cookie-session).


<a name="referencias"></a>

## Referencias

* Brown, E. (2014). Web Development with Node and Express. Sebastopol, CA: O'Reilly Media.
