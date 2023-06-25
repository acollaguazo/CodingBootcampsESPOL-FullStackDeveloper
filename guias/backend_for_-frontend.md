[Regresar](/CodingBootcampsESPOL-FullStackDeveloper/)

# Backend for Frontend

<p align="center">
<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--iChK9STG--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://miro.medium.com/max/2372/1%2Axi1CWtBDQh_OyUpEEGawVg.png" width="50%"/>
</p>

## Contenido

- [Fundamentos teóricos](#fundamentos_teoricos)
  - [Backend for Frontend](#comments)
  - [¿Qué es un BFF?](#usar)
  - [Beneficios de un BFF](#SigAPI)
- [Referencias](#referencias)

<a name="fundamentos_teoricos"> </a>

## 📑 Fundamentos teóricos

<a name="comments"> </a>

### 🟠 Backend for Frontend

Uno de los patrones arquitectónicos más nuevos  es el **backend para frontend** (BFF), se basa en dominios y simplifica la comunicación entre el frontend y el backend y simplificar el desarrollo del frontend.

<a name="usar"> </a>

### 🟠 ¿Qué es un BFF?

Un BFF es un backend dedicado para el frontend. Como se mencionó anteriormente se encarga de traducir la comunicación entre los servicios del dominio y el frontend , facilitando el trabajo en el frontend.

<p align="center">
<img src="https://i0.wp.com/christianlydemann.com/wp-content/uploads/2021/11/Untitled-Diagram.drawio-2.png?w=601&ssl=1" width="50%" alt="Banner"/>
</p>

<a name="SigAPI"> </a>

### 🟠 Beneficios de un BFF

* Simplifica la comunicación entre el frontend y el backend .
* Tener el BFF en la misma red y los servicios descendentes garantiza una baja latencia entre ellos, en comparación con realizar estas solicitudes desde el navegador del cliente. 
* Mejor seguridad. 
* El BFF es un buen lugar para configurar la lógica de almacenamiento en caché del servidor.


<a name="referencias"></a>

## Referencias

* The Complete Guide To BFF (Backend For Frontend). Retrieved May 12, 2023, from [https://christianlydemann.com/the-complete-guide-to-backend-for-frontend-bff/](https://christianlydemann.com/the-complete-guide-to-backend-for-frontend-bff/)