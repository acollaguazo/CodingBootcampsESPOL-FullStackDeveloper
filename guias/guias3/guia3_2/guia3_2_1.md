[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Comments
<p align="center">
<img src="https://user-images.githubusercontent.com/12859467/205955427-7d74d0cc-a061-4fcb-aa04-72d58f7073d9.png" width="70%"/>
</p>

## Contenido

- [Fundamentos te贸ricos](#fundamentos_teoricos)
  - [Comments](#comments)
  - [Ejemplo de comments](#ejemplo_comments)
- [Parte pr谩ctica](#practica)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 馃搼 Fundamentos te贸ricos

<a name="comments"> </a>

### 馃煚 Comments

Puede usar comentarios en su c贸digo de handlebars tal como lo har铆a en su c贸digo. Dado que generalmente hay cierto nivel de l贸gica, esta es una buena pr谩ctica.

Los comentarios no estar谩n en la salida resultante. Si desea que se muestren los comentarios, simplemente use los comentarios HTML y se generar谩n. 

<a name="ejemplo_comments"> </a>

### 馃煚 Ejemplo de comments

Es importante comprender la distinci贸n entre los comentarios de Handlebars y los comentarios de HTML. Debe preferir los comentarios de Handlebars para cualquier cosa que exponga los detalles de implementaci贸n o cualquier otra cosa que no desee exponer.
Cualquier comentario que deba contener }}u otros tokens de handlebars debe usar la sintaxis `{{!-- --}}`.

```handlebars 
{{! Comentario en handlebars. }}
<!-- Comentario en html. -->
```

<a name="practica"> </a>

## 馃捇 Parte pr谩ctica


<a name="referencias"></a>

## Referencias

* Template comments. Retrieved February 21, 2023, from https://handlebarsjs.com/guide/#template-comments 