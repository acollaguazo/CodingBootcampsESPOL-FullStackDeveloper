[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Comments
<p align="center">
<img src="https://user-images.githubusercontent.com/12859467/205955427-7d74d0cc-a061-4fcb-aa04-72d58f7073d9.png" width="70%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Comments](#comments)
  - [Ejemplo de comments](#ejemplo_comments)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Comments

Puede usar comentarios en su código de handlebars tal como lo haría en su código. Dado que generalmente hay cierto nivel de lógica, esta es una buena práctica.

Los comentarios no estarán en la salida resultante. Si desea que se muestren los comentarios, simplemente use los comentarios HTML y se generarán. 

<a name="ejemplo_comments"> </a>

### 🟠 Ejemplo de comments

Es importante comprender la distinción entre los comentarios de Handlebars y los comentarios de HTML. Debe preferir los comentarios de Handlebars para cualquier cosa que exponga los detalles de implementación o cualquier otra cosa que no desee exponer.
Cualquier comentario que deba contener }}u otros tokens de handlebars debe usar la sintaxis `{{!-- --}}`.

```handlebars 
{{! Comentario en handlebars. }}
<!-- Comentario en html. -->
```

<a name="referencias"></a>

## Referencias

* Template comments. Retrieved February 21, 2023, from https://handlebarsjs.com/guide/#template-comments 
* Brown, E. (2014). Web Development with Node and Express. Sebastopol, CA: O'Reilly Media.