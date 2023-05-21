---
remote_theme: pages-themes/architect@v0.2.0
---
[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

Personalizar la visualización de modelos
==========================================

<p align="center">
<img src="https://i.morioh.com/2022/07/25/b6e75c02.webp" width="70%" alt="Banner Node.js"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Express - ORM](#express)
- [Software a utilizar](#software)
- [Parte práctica](#practica)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="express"> </a>

Express
==========================================

Sequelize es un ORM moderno de TypeScript y Node.js para Oracle, Postgres, MySQL, MariaDB, SQLite y SQL Server, y más. Con un sólido soporte de transacciones, relaciones, carga ansiosa y diferida, replicación de lectura y más.

<a name="software"></a>

Software a utilizar
===================
* * *

De [MySQL Community Downloads](https://dev.mysql.com/downloads/), descargue e instale:
* Motor de base de datos: [MySQL Community Server](https://dev.mysql.com/downloads/mysql/)
* Interfaz gráfica: [MySQL Workbench](https://dev.mysql.com/downloads/workbench/)

<a name="practica"></a>

Parte práctica
===================

* * *

Crea un nuevo proyecto web, de acuerdo a las instrucciones de [Configuración de servidor web con Node.js](https://acollaguazo.github.io/CodingBootcampsESPOL-FullStackDeveloper/guias/guias2/guia2_3.html)

* O, Clone el proyecto con las [aplicaciones del curso](https://github.com/acollaguazo/noRDDW-apps/) 
    - Para la rama: **`hito1-sitio`**

Nodemon
=======

Desde la línea de comandos del proyecto:

* Agregue nodemon como módulo del proyecto, con: `npm install --save-dev nodemon`
  + Con esta instrucción se agregará la clave **devDependencies** en el package.json

	<pre><code>
	"devDependencies": {  
	     "nodemon": "X.Y.Z"  
	}
	</code></pre>

* En el `package.json`, dentro de la clave **scripts**, agregue la clave **devstart**:

	<pre><code>
	"scripts": {  
	  ...
	  <b style="color:red">
	  "devstart": "nodemon ./bin/www"
		</b>
		...
	}  
	</code></pre>

* En adelante, levante el servidor, con: **`npm run devstart`**
  + Con este script, ya no será necesario reiniciar el servidor para ver los cambios en el navegador.
<a name="referencias"></a>

## Referencias

* Sequelize. Retrieved February 24, 2023, from https://sequelize.org/ 

