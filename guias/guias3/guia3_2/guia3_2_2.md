[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Blocks

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Blocks](#block)
  - [Ejemplo de blocks](#ejemplo_blocks)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="block"> </a>

### 🟠 Blocks

Las cosas comienzan a complicarse cuando consideras los bloques. Los bloques proporcionan control de flujo, ejecución condicional y extensibilidad.

<a name="ejemplo_blocks"> </a>

### 🟠 Ejemplo de blocks

Considere el siguiente objeto de contexto:

```h
{
currency: {
    name: 'United States dollars',
    abbrev: 'USD',
},
tours: [
    { name: 'Hood River', price: '$99.95' },
    { name: 'Oregon Coast', price, '$159.95' },
],
specialsUrl: '/january-specials',
currencies: [ 'USD', 'GBP', 'BTC' ],
}
```

Ahora examinemos una plantilla a la que podemos pasar ese contexto:

```handlebars 
<ul>
    {{#each tours}}
        {{! I'm in a new block...and the context has changed }}
        <li>
            {{name}} - {{price}}
            {{#if ../currencies}}
                ({{../../currency.abbrev}})
            {{/if}}
        </li>
    {{/each}}
</ul>
{{#unless currencies}}
    <p>All prices in {{currency.name}}.</p>
{{/unless}}
{{#if specialsUrl}}
    {{! I'm in a new block...but the context hasn't changed (sortof) }}
    <p>Check out our <a href="{{specialsUrl}}">specials!</p>
{{else}}
    <p>Please check back often for specials.</p>
{{/if}}
<p>
    {{#each currencies}}
        <a href="#" class="currency">{{.}}</a>
    {{else}}
        Unfortunately, we currently only accept {{currency.name}}.
    {{/each}}
</p>
```
En esta plnatilla estám sucediendo algunas cosas que las iremos desglosando:
+ Empieza con los helpers que ayudan a iterar sobre una matriz. Es importante entender la diferencia entre `{{#each tours}}` y `{{/each tours}}` ya que existe un cambio de contexto.
    + En el primer pase, cambia a `{ nombre: 'Hood River', precio: '$9995' }`, y en el segundo pase, el contexto es `{ name: 'Oregon Coast', price: '$159.95' }`.
    + Sin embargo, si queremos acceder al objeto de moneda, debemos usar `../` para acceder al contexto principal.
+ El helper if es especial y un poco confuso. En Handlebars, cualquier bloque cambiará el contexto, por lo que dentro de un bloque if, hay un nuevo contexto... que resulta ser un duplicado del contexto principal.
    + En el bloque `{{#if ../currencies}}`, hemos ingresado un nuevo contexto... así que para llegar al objeto de moneda, tenemos que usar `../../`.
        + El primer `../` llega al contexto del producto y el segundo regresa al contexto más externo.
+ Lo último que se debe tener en cuenta sobre esta plantilla es el uso de {{.}} en el bloque `{{#each currencies}}`,  `{{.}}` simplemente se refiere al contexto actual. 
    + En este caso, el contexto actual es simplemente una cadena en una matriz que queremos imprimir.



<a name="referencias"></a>

## Referencias

* Block Helpers. Retrieved February 21, 2023, from https://handlebarsjs.com/guide/block-helpers.html#simple-iterators 
