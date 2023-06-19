[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Session stores

<p align="center">
<img src="https://jankleinert.com/assets/images/blog/node-redis-cookie.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Memory Stores](#comments)
  - [Using Sessions](#usar)
  - [Uso de sesiones para implementar mensajes flash](#usarD)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Memory Stores

Si prefiere almacenar la información de la sesión en el servidor, lo cual se recomienda, debe existir un lugar para almacenarla. La opción de nivel de entrada son las sesiones de memoria. Son muy fáciles de configurar, pero tienen una gran desventaja: cuando reinicias el servidor, la información de tu sesión desaparece. Peor aún, si escala horizontalmente al tener varios servidores, un servidor diferente podría atender una solicitud cada vez: los datos de la sesión a veces estarían allí y otras veces no. Esta es claramente una experiencia de usuario inaceptable. Sin embargo, para necesidades de desarrollo y pruebas, será suficiente.

Para el uso de sesiones de memoria, instale express-session.

```
npm install --save express-session
```
Luego, después de vincular en el analizador de cookies, vincular en sesión express:

```js
app.use(require('cookie-parser')(credentials.cookieSecret));
app.use(require('sesión-express')());
```

El middleware de sesión express acepta un objeto de configuración con las siguientes opciones:
  * Key
El nombre de la cookie que almacenará el identificador de sesión único. El valor predeterminado es connect.sid.
  * Store
Una instancia de un almacén de sesiones. El valor predeterminado es una instancia de MemoryStore.
  * Cookie
Configuración de cookies para la cookie de sesión (ruta, dominio, seguro, etc.). Se aplican los valores predeterminados regulares de cookies.

Una vez que haya configurado las sesiones, usarlas no podría ser más simple: simplemente use las propiedades de la variable de sesión del objeto de solicitud:

<a name="usar"> </a>

### 🟠 Using Sessions

Una vez que se haya configurado las sesiones, usarlas no podría ser más simple: simplemente use las propiedades de la variable de sesión del objeto de solicitud:

```js
req.session.userName = 'Anonymous';
var colorScheme = req.session.colorScheme || 'dark';
```

Tenga en cuenta que con las sesiones, no tenemos que usar el objeto de solicitud para recuperar el valor y el objeto de respuesta para establecer el valor: todo se realiza en el objeto de solicitud.
(El objeto de respuesta no tiene una propiedad de sesión). Para eliminar una sesión, puede usar el operador de eliminación de JavaScript:

```js
req.session.userName = null;  // this sets 'userName' to null,
                              // but doesn't remove it
delete req.session.colorScheme; // this removes 'colorScheme'
```

<a name="usarD"> </a>

### 🟠  Uso de sesiones para implementar mensajes flash

Los mensajes "Flash" (que no deben confundirse con Adobe Flash) son simplemente una forma de proporcionar comentarios a los usuarios de una manera que no interrumpa su navegación. La forma más fácil de
implementar mensajes flash es usar sesiones (también puede usar la cadena de consulta, pero además de aquellos que tienen URL más feas, los mensajes flash se incluirán en un marcador, que probablemente no sea lo que desea). Configuremos nuestro HTML primero. Estaremos usando los mensajes de alerta de Bootstrap para mostrar nuestros mensajes flash, así que asegúrese de tener Bootstrap vinculado. En su archivo de plantilla, en algún lugar destacado (generalmente directamente debajo del encabezado de su sitio), agregue lo siguiente:

```js
{{#if flash}}
      <div class="alert alert-dismissible alert-{{flash.type}}">
           <button type="button" class="close" data-dismiss="alert"    aria-hidden="true">&times;<button>
           <strong>{{flash.intro}}</strong> {{{flash.message}}}
      </div>
{{/if}}
```

Tenga en cuenta que usamos tres corchetes para flash.message: esto nos permitirá proporcionar algo de HTML simple en nuestros mensajes (podríamos querer enfatizar palabras o incluir hipervínculos). Ahora agreguemos algo de middleware para agregar el objeto flash al contexto si hay uno en la sesión. Una vez que mostramos un mensaje flash una vez, queremos eliminarlo de la sesión para que no se muestre en la siguiente solicitud. Agrega este código antes de tus rutas:

```js
app.use(function(req, res, next){
    // if there's a flash message, transfer
    // it to the context, then clear it
    res.locals.flash = req.session.flash;
    delete req.session.flash;
    next();
});
```

Ahora veamos cómo usar realmente el mensaje flash. Imagine que estamos registrando usuarios para un newsletter y queremos redirigirlos al archivo del newsletter después de que se registren.
Así es como se vería nuestro controlador de formulario:

```js
app.post('/newsletter', function(req, res){
    var name = req.body.name || '', email = req.body.email || '';
    // input validation
    if(!email.match(VALID_EMAIL_REGEX)) {
       if(req.xhr) return res.json({ error: 'Invalid name email address.' });
        req.session.flash = {
            type: 'danger',
            intro: 'Validation error!',
            message: 'The email address you entered was not valid.',
        };
        return res.redirect(303, '/newsletter/archive');
    }
    new NewsletterSignup({ name: name, email: email }).save(function(err){
    if(err) {
        if(req.xhr) return res.json({ error: 'Database error.' });
        req.session.flash = {
             type: 'danger',
             intro: 'Database error!',
             message: 'There was a database error; please try again later.',
        }
        return res.redirect(303, '/newsletter/archive');
    }
    if(req.xhr) return res.json({ success: true });
    req.session.flash = {
            type: 'success',
            intro: 'Thank you!',
            message: 'You have now been signed up for the newsletter.',
    };
    return res.redirect(303, '/newsletter/archive');
    });
});
```
Los mensajes flash son un excelente mecanismo para tener disponible en su sitio web, incluso si otros métodos son más apropiados en ciertas áreas (por ejemplo, los mensajes flash no siempre son apropiados para "asistentes" multiformes o flujos de pago de carritos de compras). Los mensajes flash también son excelentes durante el desarrollo, ya que son una manera fácil de proporcionar comentarios, incluso si los reemplaza con una técnica diferente más adelante.

<a name="referencias"></a>

## Referencias

* Brown, E. (2014). Web Development with Node and Express. Sebastopol, CA: O'Reilly Media.