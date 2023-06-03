[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Handlebars
<p align="center">
<img src="https://i0.wp.com/blog.fossasia.org/wp-content/uploads/2017/07/handlebars-js.png?fit=500%2C500&ssl=1" width="70%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Handlebars](#handlebars)
  - [Funcionamiento de Handlebar](#funcionamiento_handlebars)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="handlebars"> </a>

### 🟠 Handlebars

Handlebars es una extensión de Moustache, otro popular motor de plantilla. Se recomienda Handlebars por su fácil. integración de JavaScript (tanto frontend como backend) y su sintaxis familiar. 

<a name="funcionamiento_handlebars"> </a>

### 🟠 Funcionamiento de Handlebar

Para entender el funcionamiento de la plantilla se debe comprender el concepto de contexto. Cuando renderizas una plantilla, pasas al motor de plantillas un objeto llamado objeto de contexto, y esto es lo que permite que los reemplazos funcionen.
Por ejemplo, si mi objeto de contexto es ` { nombre: 'Buttercup' }`, y mi plantilla es `<p>¡Hola, {{name}}!</p>`, {{name}} se reemplazará con Buttercup. ¿Qué sucede si desea pasar HTML a la plantilla? Por ejemplo, si nuestro contexto fuera `{ name: '<b>Buttercup</b>' }`, usar la plantilla anterior dará como resultado `<p>Hola,&lt;b&gt;Buttercup&lt;b&gt;</p>`, que es probablemente no sea lo que estás buscando. Para resolver este problema, simplemente use tres corchetes en lugar de dos: {{{nombre}}}.

<p align="center">
<img src="./handlebars.png" width="70%" alt="Banner"/>
</p>
En la imagen anterior vemos cómo el motor Handlebars utiliza el contexto (representado por un óvalo) combinado con la plantilla para renderizar HTML.

<a name="referencias"></a>

## Referencias

* Brown, E. (2014). Web Development with Node and Express. Sebastopol, CA: O'Reilly Media.