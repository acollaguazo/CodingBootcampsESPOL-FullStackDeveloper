[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Serverless Architecture

<p align="center">
<img src="https://bs-uploads.toptal.io/blackfish-uploads/components/seo/content/og_image_file/og_image/912630/REDESIGN_Implementing-Serverless-Node.js-Functions-Using-Google-Cloud_Luke-Social-e771294bfbdc9fd474c07d98cd10cd72.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Serverless Architecture](#comments)
  - [Ventajas de las aplicaciones sin servidor](#comment)
  - [Crear una aplicación de microservicio simple con Node.js](#comment)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Serverless Architecture

La mayoría de las aplicaciones web se ejecutan en servidores de alto mantenimiento. Hoy en día, los equipos de ingeniería de software cuentan con ingenieros dedicados de DevOps/infraestructura para ayudar a administrar, aprovisionar y mantener estos servidores. Debido a los desafíos asociados con esta configuración, se hizo necesaria la necesidad de impulsar soluciones alternativas. La pila sin servidor brilla en este sentido.

La belleza de serverless como marco es que solo tiene que pagar una cantidad equivalente por los recursos necesarios para ejecutar toda su infraestructura, de hecho, con gastos generales y costos radicalmente menores.

El código sin servidor es una función sin estado activada o ejecutada por la ocurrencia de eventos, por ejemplo, eventos de red (ciclo de solicitud/respuesta HTTP). Para las aplicaciones sin servidor, los contextos de función vinculados a eventos específicos deben ejecutarse antes de que finalicen esos eventos.

<a name="comment"> </a>

### 🟠 Ventajas de las aplicaciones sin servidor

*  Las aplicaciones sin servidor se escalan según la demanda en función de la cantidad de recursos necesarios para gestionar el servicio de solicitudes, por lo que no hay necesidad de temer fallar cuando se producen picos repentinos de tráfico.
*  Las solicitudes simultáneas se activan en nuevas instancias de contenedor
*  Las actualizaciones de seguridad o los parches se gestionan por nosotros.
*  Todos los demás detalles técnicos son manejados por los proveedores de la nube en cuestión para que, como ingenieros, podamos centrarnos más en el mantenimiento de la aplicación central y la implementación de funciones.
*  Ciclo de implementación más rápido ejecutado a través de un solo comando,sls deploy.
*  Serverless ofrece una abstracción para la infraestructura de la nube.
*  Lo más importante es pagar por los recursos exactos consumidos, ya que la administración del servidor se maneja en nuestro nombre.


<a name="referencias"></a>

## Referencias

* Going serverless with Node.js apps. Retrieved May 12, 2023, from [https://blog.logrocket.com/going-serverless-node-js-apps/](https://blog.logrocket.com/going-serverless-node-js-apps/)