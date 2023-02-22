[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Encoding

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Encoding](#encoding)
  - [Tipos de encoding](#tipos)
    - [Codificados con URL](#codificados-con-url)
    - [Codificados de varias partes](#codificados-de-varias-partes)
- [Parte práctica](#practica)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="encoding"> </a>

### 🟠 Encoding

Cuando se envía el formulario (ya sea por el navegador o mediante AJAX), debe codificarse de alguna manera. Si no especifica explícitamente una codificación, el valor predeterminado es application/x-wwwform-urlencoded (este es solo un tipo de medio largo para "URL codificado"). Esta es una codificación básica y fácil de usar compatible con Express desde el primer momento.

Si necesita cargar archivos, las cosas se complican más. No existe una forma sencilla de enviar archivos mediante la codificación de URL, por lo que se ve obligado a utilizar el tipo de codificación multipart/form-data, que es y no es manejado directamente por Express

<a name="tipos"> </a>

### 🟠 Tipos de encoding

Los formularios HTML contienen dos codificaciones, los formularios codificados con URL y los formularios de varias partes.

<a name="url"> </a>

#### 🔹 Codificados con URL

Los datos que se envían mediante este tipo de codificación de formulario están codificados en URL, como se desprende claramente de su nombre. Por defecto, se asigna al atributo enctype. 

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>URL Encoded Forms</title>
  </head>
  <body>
    <form
      action="/urlencoded?firstname=Geeks&lastname=forGeeks"
      method="POST"
      enctype="application/x-www-form-urlencoded">
      <input type="text" name="username" value="GeeksforGeeks" />
      <input type="text" name="password" value="GFG@123" />
      <input type="submit" value="Submit" />
    </form>
  </body>
</html>
``` 

<a name="partes"> </a>

#### 🔹 Codificados de varias partes

Este tipo de formularios se utilizan cuando el usuario carga algunos archivos en el servidor.

```html
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8" />
	<title>Multipart Forms</title>
</head>
<body>
	<form
	action="/multipart?firstname=Geeks for&lastname=Geeks"
	method="POST"
	enctype="multipart/form-data">
	<input type="text" name="username" value="Geeks for Geeks" />
	<input type="text" name="password" value="GFG@123" />
	<input type="submit" value="Submit" />
	</form>
</body>
</html>

```

<a name="practica"> </a>

## 💻 Parte práctica


<a name="referencias"></a>

## Referencias

* Understanding HTML Form Encoding: URL Encoded and Multipart Forms. Retrieved February 23, 2023, from https://www.geeksforgeeks.org/understanding-html-form-encoding-url-encoded-and-multipart-forms/ 