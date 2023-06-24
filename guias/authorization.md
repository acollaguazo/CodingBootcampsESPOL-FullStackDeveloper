[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Authorization

<p align="center">
<img src="https://i.morioh.com/0240508d22.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Autenticación](#comments)
  - [JWT](#usar)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Autenticación

Al construir una  API se debe considerar el tema de autenticación y existen diferentes opciones disponibles. Entre las opciones incluyen el token web JSON, OAuth, la clave API y más. 

### 🟠 JWT

Los tokens web JSON (JWT) se han introducido como un método de comunicación segura entre dos partes.

Aunque estaba destinado a cualquier comunicación segura, JWT se asocia principalmente con la autenticación y la autorización.

Un ejemplo de token de JWT seria el siguiente.

```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.cThIIoDvwdueQB468K5xDc5633seEFoqwxjF\ _xSJyQQ
```

El token se construye a partir de lo siguiente:


```js
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  your - 256 - bit - secret
)
```

La primera parte es el encabezado codificado en base64, que se ve así cuando se decodifica

```js
{
  "alg": "HS256",
  "typ": "JWT"
}
```

Básicamente, contiene el tipo de algoritmo, que es HMAC SHA 256, y el tipo de token, que es JWT.

La segunda parte contiene datos JSON codificados en base64 que se intercambian (principalmente algunos detalles de usuario en el caso de la autenticación), que en nuestro token se ve así:

```js
{
  "sub": "1234567890",
  "name": "John Doe",
  "iat": 1516239022
}
```

La tercera parte es una firma para verificar que el token es legítimo y que la información no ha cambiado.

Se recomienda no incluir ningún dato confidencial en JWT como la contraseña de usuario.

A continuación se muestra un diagrama de trabajo de autenticación y autorización JWT.

<p align="center">
<img src="https://images.ctfassets.net/piwi0eufbb2g/1cMXWBjSogZJs9FuxpXYf2/d1ef31b8f161696cf8aa0ff63ab4753e/image.png" width="50%"/>
</p>

Primero, el cliente envía una solicitud de inicio de sesión con las credenciales de inicio de sesión (principalmente nombre de usuario, correo electrónico, contraseña), luego, en el lado del servidor, verificamos si las credenciales de inicio de sesión proporcionadas son correctas. Si es así, generamos un token JWT firmado con información de usuario y lo enviamos al cliente.

Una vez que el usuario inicia sesión, el cliente envía una solicitud de datos con un token JWT firmado (para informar al servidor quién está solicitando datos). En el lado del servidor, verificamos si el JWT proporcionado es válido, luego verificamos si el usuario puede ver los datos que se solicitaron (este paso se conoce como autorización). Enviamos los datos si ambos pasos se verifican, de lo contrario, enviamos un mensaje de error.

<a name="referencias"></a>

## Referencias

* AUTHENTICATION AND AUTHORIZATION IN EXPRESS.JS API USING JWT. Retrieved June 10, 2023, from [https://www.topcoder.com/thrive/articles/authentication-and-authorization-in-express-js-api-using-jwt](https://www.topcoder.com/thrive/articles/authentication-and-authorization-in-express-js-api-using-jwt)