# Índice

- [CAPITULO III: REQUIREMENTS ESPECIFICATION](#capitulo-iii-requirements-especification)
  - [3.1. To-Be Scenario Mapping](#31-to-be-scenario-mapping)
  - [3.2. User Stories](#32-user-stories)
  - [3.3. Impact Mapping](#33-impact-mapping)
  - [3.4. Product Backlog](#34-product-backlog)


# CAPITULO III: REQUIREMENTS ESPECIFICATION

## 3.1. To-Be Scenario Mapping

Basándonos en nuestras posibles soluciones elaboramos un To-Be Scenario Mapping para observar cómo es que nuestras ideas podrían abordar las necesidades del usuario

**Segmento Objetivo-Attendee:**

[Ver enlace 4](#_anexos)

![Interfaz de usuario gráfica Descripción generada automáticamente](Aspose.Words.a0dd4f9a-8c6c-4a02-978d-f8d17446a191.001.png)[](#_anexos)

**Segmento Objetivo-Organizer:**

[Ver enlace 5](#_anexos)

[](#_anexos)![Interfaz de usuario gráfica Descripción generada automáticamente](Aspose.Words.a0dd4f9a-8c6c-4a02-978d-f8d17446a191.002.png)

## 3.2. User Stories   

En esta sección redactamos las historias de usuario necesarias para el correcto funcionamiento de nuestra aplicación según las necesidades de nuestros segmentos objetivos, considerando con ello un mínimo de un criterio de aceptación para cada historia de usuario.

|<a name="_hlk162522748"></a># Epic|Descripción|
| :-: | :-: |
|EP01|Como usuario quiero conocer lo que ofrece la aplicación para hacer o no uso de ella.|
|EP02|Como Attendee quiero acceder a las funcionalidades propias de mi rol en la aplicación.|
|EP03|Como usuario quiero tener una cuenta en la aplicación, además de personalizarla.|
|EP04|Como Organizer quiero acceder a las funcionalidades propias de mi rol en la aplicación.|
|EP05|Cómo developer quiero acceder a endpoints para interactuar con la aplicación.|

|<a name="_hlk162522812"></a>Epic / Story|Título|Descripción|Criterio de aceptación|Relacionado con (Epic ID)|
| :-: | :-: | :-: | :-: | :-: |
|EP05/TS01|Acceder a EndPoints|Como developer quiero acceder a endpoints para interactuar con la aplicación|<p>**Escenario 1:** Persistencia del endpoint</p><p>**Dado que** el Developer hace uso del endpoint para interactuar con la aplicación</p><p>**Y** existe la solicitud </p><p>**Entonces** el api devuelve un response con toda la data solicitada</p><p></p><p>` `**Escenario 2**: No funciona la persistencia del endpoint</p><p>**Dado que** el Developer hace uso del endpoint para interactuar con la aplicación</p><p>**Y** existe un error en la solicitud</p><p>**Entonces** el api devuelve un bad request indicando los errores</p>|EP05|
|EP01/US01|Conocer propósito del sitio web |**Como** visitante **quiero** conocer el propósito del sitio web **para** conocer qué es lo que ofrece a los usuarios|<p>**Escenario 1:** El “visitante” visualiza la sección  “Quienes somos” </p><p>**Dado que** observo el landing page. **Y** me dirijo a la sección “Quienes somos”. **Entonces** visualizo una descripción del propósito de la aplicación web.</p><p>**Escenario 2:** El “visitante” no visualiza la sección  “Quienes somos”</p><p>**Dado que** observo el landing page. **Y** me dirijo a la sección “Quienes somos”. **Entonces** visualizo un mensaje de error </p>|EP03|
|EP01/US02|Conocer a qué tipo de usuario satisfacen|**Como** “visitante” **quiero** conocer a qué tipo de usuarios satisface esta aplicación **para** decidir obtenerla o no|<p>**Escenario 1:** El “visitante” visualiza las secciones de “Organizador y Publico”</p><p>**Dado que** observo el landing page. **Y** me dirijo a las secciones de “Organizador” y “Público”. **Entonces** leo una descripción de a qué tipo de usuarios busca satisfacer la aplicación.</p><p>**Escenario 2:** El “visitante” no visualiza las secciones de “Organizador y Publico”</p><p>**Dado que** observo el landing page. **Y** me dirijo a las secciones de “Organizador” y “Público”. **Entonces** visualizo un mensaje de error.</p>|EP03|
|EP03/US03|Registrar Usuario en la aplicación|**Como** visitante **quiero** crear una cuenta en la aplicación **para** hacer uso de los servicios de la misma|<p>**Escenario 1:** El “visitante” registra sus datos correctamente.</p><p>**Dado que** no poseo una cuenta en la aplicación. **Cuando** accedo a la página de registro. **Y** completo los datos del formulario referentes al “Username”, “Email” , “Password“,  y “UserType”. **Y** guardo el registro. **Entonces** recibo una confirmación en pantalla de que se creo mi cuenta.</p><p></p><p>**Escenario 2:** El “visitante” registra sus datos incorrectamente.</p><p>**Dado que** no poseo una cuenta en la aplicación. **Cuando** accedo a la página de registro. **Y** complete incorrectamente los datos del formulario referentes al “Username”, “Email” , “Password“,  y “UserType”. **Y** guardo el registro. **Entonces** recibo un mensaje de error.</p>|EP01|
|EP02/US04|Visualizar eventos sociales |**Como** visitante del segmento objetivo de “Attendee” **quiero** encontrar eventos sociales para reservar entradas|<p>**Escenario 1:** Attendee” busca eventos sociales </p><p>**Dado que** soy un "Attendee” **Y** quiero encontrar un evento social. **Cuando** ingreso a la seccion de eventos. **Entonces** visualizo los eventos sociales disponibles.</p><p></p><p> **Escenario 2:** Attendee no encuentra eventos sociales </p><p> **Dado que** soy un “Attendee” Y quiero encontrar un evento social. **Cuando** ingreso a la seccion de eventos. **Entonces** no visualize ningun evento social disponible.</p>|EP03|
|EP04/US05|Registrar un evento social |**Como** visitante del segmento objetivo de “Organizer” **quiero** crear eventos para promocionarlos |<p>**Escenario 1:**  “Organizer” crea eventos sociales que está organizando</p><p>**Dado que** soy un “Organizer”. **Cuando** ingreso al formulario de crear un evento. **Y** completo correctamente los datos de “NameEvent”, “District”, “Choose date”, “Image”, “Hour”,”Price”, “Address” y “Capacity”. **Entonces** se publica el evento social mostrando las caracteristicas del mismo.</p><p>**Escenario 2:**  “Organizer” no puede crear eventos sociales que está organizando</p><p>**Dado que** soy un “Organizer”. **Cuando** ingreso al formulario de crear un evento. **Y** completo correctamente los datos de “NameEvent”, “District”, “Choose date”, “Image”, “Hour”,”Price”, “Address” y “Capacity” Y uno de los datos no cumpla las validaciones. **Entonces** aparecera un mensaje de error y no se registrar el evento.</p>|EP03|
|EP05/TS02|<p>Registrar asistentes</p><p> </p>|**Como** Developer **quiero** contar con un endpoint **para** registrar asistentes a eventos|<p>**Escenario 1:** Registro exitoso de un usuario</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta se valida correctamente</p><p>**Entonces** se registra al asistente de eventos en la base de datos y se recibe el código de respuesta 200 del API rest.</p><p></p><p>**Escenario 2:** Registro no exitoso del asistente a eventos</p><p>**Dado que** se recibe la data incompleta del front</p><p>**Y** por ende no se valida correctamente</p><p>**Entonces** no se registra al asistente de eventos en la base de datos</p><p>**Y** el API devuelve una respuesta de error con el mensaje de que no se realizó el registro del asistente a eventos y el código 400 BAD REQUEST</p>|EP05|
|EP02/US06|Conocer precio de los boletos|**Como** visitante del segmento objetivo de “Attendee” **quiero** conocer el precio de los boletos **para** asistir al evento social de mi interes |<p>**Escenario 1:** “Attendee” conoce el precio de los boletos</p><p>**Dado que** soy un “Attendee” y me encuentro visualizando los distintos eventos sociales publicitados. **Cuando** encuentre uno de mi interés y lo seleccione. **Entonces** puedo conocer el precio del boleto de dicho evento.</p><p>**Escenario 2:** “Attendee” no puede conocer el precio de los boletos</p><p>**Dado que** soy un “Attendee” y me encuentro visualizando los distintos eventos sociales publicitados. **Cuando** encuentre uno de mi interés y lo seleccione. Y la informacion de dicho evento no se cargue correctamente. **Entonces** no puedo conocer el precio del boleto de dicho evento.</p>|EP04|
|EP05/TS03|Registrar organizadores|**Como** developer **quiero** contar con un endpoint **para** registrar a los organizadores de eventos|<p>**Escenario 1:** Registro exitoso de un usuario</p><p>**Dado que** se recibe la data del exterior y esta se valida correctamente</p><p>**Entonces** se registra al organizador de eventos en la base de datos y se recibe el código de respuesta 200 del API Rest.</p><p>**Escenario 2:** Registro no exitoso del organizador de eventos</p><p>**Dado que** se recibe la data incompleta del front y por ende no se valida correctamente **Entonces** no se registra al organizador de eventos en la base de datos y el API devuelve una respuesta de error con el mensaje de que no se realizó el registro del asistente a eventos y el código 400 BAD REQUEST</p>|EP05|
|EP02/US07|Obtener el/los boleto/s de un evento social |**Como** visitante del segmento objetivo de “Attendee” **quiero** obtener el/los boleto/s **para** asistir al evento social de mi interés|<p>**Escenario 1:** “Attendee” desea comprar el/los boleto/s</p><p>**Dado que** soy un “Attendee” y estoy viendo los detalles de un evento social. **Cuando** seleccione el boton de compra. **Entonces** soy redirigido a una vista donde puedo realizar la transacción.                                 </p><p>**Escenario 2:** “Attendee” realiza la transacción de la compra de el/los boleto/s</p><p>**Dado que** me encuentro en el formulario de compra. **Cuando** complete los datos “Cantidad de boletos” y los datos de mi tarjeta Y presione el botón Pagar. **Entonces** el sistema procesa la transacción exitosamente.</p><p></p><p>**Escenario 3:** “Attendee” no puede realizar la transacción de la compra de el/los boleto/s</p><p>**Dado que** me encuentro en el formulario de compra. **Cuando** complete los datos “Cantidad de boletos” Y al presionar el botón pagar los datos de mi trajeta no sean válidos. **Entonces** el sistema no procesa la transacción.</p>|EP03|
|EP05/TS04|<p>Registrar Pago</p><p> </p>|**Como** developer **quiero** contar con un endpoint **para** registrar los pagos realizados de los eventos|<p>**Escenario 1:** Registro exitoso de un Pago</p><p>**Dado que** se recibe la data del exterior y esta se valida correctamente</p><p>**Entonces** se registra el pago de un evento en la base de datos y se recibe el código de respuesta 200 del API rest.</p><p>**Escenario 2:** Registro no exitoso del pago</p><p>**Dado que** se recibe la data incompleta del front y por ende no se valida correctamente</p><p>**Entonces** no se registra el pago en la base de datos y el API devuelve una respuesta de error con el mensaje de que no se realizó el registro del asistente a eventos y el código 400 BAD REQUEST</p>|EP03|
|EP05/TS05|Registrar eventos|**Como** developer **quiero** contar con un endpoint **para** registrar los eventos|<p>**Escenario 1:** Registro exitoso de un evento</p><p>**Dado que** se reciben los datos necesarios para la creación de un evento y son validados correctamente</p><p>**Entonces** se registra un evento en la base de datos y se recibe el código de respuesta 200 del API rest.</p><p></p><p>**Escenario 2:**  Registro no exitoso de evento</p><p>**Dado que** se reciben los datos pero no cumplen alguna de nuestras políticas de negocio.</p><p>**Entonces** no se registra el evento en la base de datos y el API devuelve un mensaje de error con el mensaje de que no se realizó el registro de evento con el código 400 BAD REQUEST</p>|EP05|
|EP05/TS06|Creación de persistencia de la entidad Organizer|Como developer necesito hacer persistir los datos de la entidad Organizer|<p>**Escenario 1 :** Registro de la data exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta se valida correctamente</p><p>**Entonces** esta data se registra en la tabla de datos de la entidad Organizer</p><p></p><p>**Escenario 2 :** Registro de la data no exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta no se valida correctamente</p><p>**Entonces** esta data no se registra en la tabla de datos de la entidad Organizer</p><p>**Y** se devuelve un mensaje de error indicando que la data no pudo ser guardada</p>|EP05|
|EP05/TS07|Creación de persistencia de la entidad Attendee|Como developer necesito hacer persistir los datos de la entidad Attendee|<p>**Escenario 1** : Registro de la data exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta se valida correctamente</p><p>**Entonces** esta data se registra en la tabla de datos de la entidad Attendee</p><p></p><p>**Escenario 2** : Registro de la data no exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta no se valida correctamente</p><p>**Entonces** esta data no se registra en la tabla de datos de la entidad Attendee</p><p>**Y** se devuelve un mensaje de error indicando que la data no pudo ser guardada</p>|EP05|
|EP01/US08|Conocer más información del startup|**Como** visitante **quiero** conocer quiénes son los creadores de la aplicación y que ofrecen con la misma **para** advertir los beneficios que me pueden brindar con su uso|<p>**Escenario 1:** El “visitante” visualiza la seccion de “Team Designer”</p><p>**Dado que** observo el landing page. **Y** me dirijo a la seccion de “Team Designer”. **Entonces** visualizo quienes son los creadores de la aplicación.</p><p>**Escenario 2:** El “visitante” no puede visualizar la seccion de “Team Designer”</p><p>**Dado que** observo el landing page. **Y** me dirijo a las secciones de Team Designer”. **Entonces** visualizo un mensaje de error.</p>|EP03|
|EP03/US09|Mostrar el apartado de preguntas frecuentes (FAQ)|**Como** visitante **quiero** acceder a una ventana de preguntas frecuentes (FAQ) **para** encontrar respuestas rápidas a preguntas frecuentes.|<p>**Escenario 1:** Visitante quiere visualizar la seccion de FAQ</p><p>**Dado que soy un** Visitante **Y** me encuentro en la aplicacion web. **Cuando** me dirijo al apartado de FAQ. **Entonces** puedo visualizar y leer las preguntas realizadas frecuentemente para resolver mis dudas.</p><p>**Escenario 2:** Visitante no puede visualizar la seccion de FAQ</p><p>**Dado que soy un** Visitante **Y** me encuentro en la aplicacion web. **Cuando** me dirijo al apartado de FAQ. **Entonces** me devuelve un error.</p>|EP01|
|EP04/US10|Visualizar historial de eventos|**Como** visitante del segmento objetivo de “Organizer” **quiero** visualizar el historial de todos los eventos que he creado, **para** tener un registro de cada uno de ellos|<p>**Escenario 1:** “Organizer” visualiza su historial de eventos creados.</p><p>**Dado** que soy un “Organizer” que me encuentra logueado en la aplicacion. **Cuando** me dirijo a la sección “Mis eventos”. **Entonces** visualizo el registro de todos los eventos que cree.</p><p>**Escenario 2:** “Organizer” no puede visualizar su historial de eventos creados.</p><p>**Dado** que soy un “Organizer” que me encuentra logueado en la aplicacion. **Cuando** me dirijo a la sección “Mis eventos”. **Entonces** visualizo unmensaje de que no hay eventos creados.</p>|EP03|
|EP05/TS08|Creación de persistencia de la entidad Payment|Como developer necesito hacer persistir los datos de la entidad Payment|<p>**Escenario 1** : Registro de la data exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta se valida correctamente</p><p>**Entonces** esta data se registra en la tabla de datos de la entidad Payment</p><p> </p><p>**Escenario 2** : Registro de la data no exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta no se valida correctamente</p><p>**Entonces** esta data no se registra en la tabla de datos de la entidad Payment</p><p>**Y** se devuelve un mensaje de error indicando que la data no pudo ser guardada</p>|EP05|
|EP03/US11|Editar perfil de usuario de “Attendee”|**Como** visitante del segmento objetivo de “Attendee” **quiero** visualizar mi perfil **para** editar mis datos.|<p>**Escenario 1:** “Attendee” edita su perfil de usuario.</p><p>**Dado que** me encuentro en la vista para editar mi perfil. Cuando modifique mis datos de “Username” y “Password”. **Entonces** mis datos se actualizan correctamente.</p><p></p><p>**Escenario 1:** “Attendee” no puede editar su perfil de usuario.</p><p>**Dado que** me encuentro en la vista para editar mi perfil. Cuando modifique mis datos de “Username” y “Password”. **Y** estos no cumplen con las validaciones. **Entonces** recibo un mensaje de error.</p>|EP01|
|EP03/US12|Editar perfil de usuario de “Organizer”|**Como** visitante del segmento objetivo de “Organizer” **quiero** visualizar mi perfil **para** editar mis datos.|<p>**Escenario 1:** “Organizer” edita su perfil de usuario.</p><p>**Dado que** me encuentro en la vista para editar mi perfil. Cuando modifique mis datos de “Username” y “Password”. **Entonces** mis datos se actualizan correctamente.</p><p></p><p>**Escenario 1:** “Organizer” no puede editar su perfil de usuario.</p><p>**Dado que** me encuentro en la vista para editar mi perfil. Cuando modifique mis datos de “Username” y “Password”. **Y** estos no cumplen con las validaciones. **Entonces** recibo un mensaje de error.</p>|EP01|
|EP05/TS09|Creación de persistencia de la entidad Event|Como developer necesito hacer persistir los datos de la entidad Event|<p>**Escenario 1 :** Registro de la data exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta se valida correctamente</p><p>**Entonces** esta data se registra en la tabla de datos de la entidad Event</p><p></p><p>**Escenario 2 :** Registro de la data no exitosa en la base de datos</p><p>**Dado que** se recibe la data del exterior</p><p>**Y** esta no se valida correctamente</p><p>**Entonces** esta data no se registra en la tabla de datos de la entidad Event</p><p>**Y** se devuelve un mensaje de error indicando que la data no pudo ser guardada</p>|EP05|
|EP05/TS10|Creación de resource de la entidad Organizer|Como developer necesito devolver un resource de los datos de la entidad Organizer|<p>**Escenario 1 :** Retorno exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta se procesa correctamente</p><p>**Entonces** se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Organizer</p><p></p><p>**Escenario 2** : Retorno no exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta no se procesa correctamente</p><p>**Entonces** no se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Organizer</p><p>**Y** se devuelve un mensaje de error indicando que la consulta no pudo ser validada</p><p>** </p>|EP05|
|EP04/US13|Mostrar la lista de asistentes de un evento|**Como** visitante del segmento objetivo de “Organizer” **quiero** ver la lista de personas que asistieron a mi evento **para** administrar tal informacion|<p>**Escenario 1:** “Organizer” visualiza los asistentes de su evento.</p><p>**Dado que soy un “Organizer” que me encuentro logueado en la aplicacion**. Cuando en un evento selecciono la opción de ver asistentes. **Entonces,** visualize una lista de asistentes de dicho evento.</p><p>**Escenario 2:** “Organizer” no puede visualizar los asistentes de su evento.</p><p>**Dado que soy un “Organizer” que me encuentro logueado en la aplicacion**. Cuando en un evento selecciono la opción de ver asistentes. **Entonces,** visualize un mensaje de que aún no hay asistentes para dicho evento.</p>|EP03|
|EP05/TS11|Creación de resource de la entidad Payment|Como developer necesito devolver un resource de los datos de la entidad Payment|<p>**Escenario 1 :** Retorno exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta se procesa correctamente</p><p>**Entonces** se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Payment</p><p></p><p>**Escenario 2 :** Retorno no exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta no se procesa correctamente</p><p>**Entonces** no se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Payment</p>|EP05|
|EP02/US14|Visualizar los detalles de un evento|**Como** visitante del segmento objetivo de “Attendee” **quiero** ver los detalles de un evento **para** decidir adquirir boletos de ello.|<p>**Escenario 1:** “Attendee” visualiza los detalles de un evento.</p><p>**Dado que** soy un “Attendee” logueado en la aplicacion. Y me encuentro visualizando todos los evetos. Cuando selecciono la opción ver detalle. **Entonces,** visualizo los detalles del evento como hora, costo, dirección y aforo. </p><p>Escenario 2: “Attendee” no visualiza los detalles de un evento.</p><p>Dado que soy un “Attendee” logueado en la aplicacion. Y me encuentro visualizando todos los evetos. Cuando selecciono la opción ver detalle. Entonces, visualize un mensaje de error.</p>|EP03|
|EP05/TS12|Creación de resource de la entidad Attendee|Como developer necesito devolver un resource de los datos de la entidad Attendee|<p>**Escenario 1 :** Retorno exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta se procesa correctamente</p><p>**Entonces** se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Attendee</p><p></p><p>**Escenario 2 :** Retorno no exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta no se procesa correctamente</p><p>**Entonces** no se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Attendee</p><p>**Y** se devuelve un mensaje de error indicando que la consulta no pudo ser validada</p>|EP05|
|EP03/US15|Iniciar sesión  |**Como** visitante **quiero** ingresar sesión en la aplicación **para** disfrutar de los beneficios de la misma|<p>**Escenario 1:**  Visitante inicia sesión en la aplicación</p><p>**Dado que** soy un usuario. Y me encuentro en la vista de “iniciar sesion” de la aplicación. **Cuando** completo correctamente los datos a “Username” y “Password”. **Entonces** accedo a mi perfil en la aplicacion.     </p><p></p><p>**Escenario 2:**  Visitante no inicia sesión en la aplicación</p><p>**Dado que** soy un usuario. Y me encuentro en la vista de “iniciar sesion” de la aplicación. **Cuando** completo los datos a “Username” y “Password” incorrectamente. **Entonces** recibo un mensaje de error.</p>|EP01|
|EP05/TS13|Creación de resource de la entidad Event|Como developer necesito devolver un resource de los datos de la entidad Event|<p>**Escenario 1** : Retorno exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta se procesa correctamente</p><p>**Entonces** se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Event</p><p></p><p>**Escenario 2 :** Retorno no exitoso de un resource al realizar una consulta a la base de datos</p><p>**Dado que** se recibe una consulta del exterior</p><p>**Y** esta no se procesa correctamente</p><p>**Entonces** no se devuelve el resource correspondiente a la consulta realizada a la tabla de datos de la entidad Event</p><p>**Y** se devuelve un mensaje de error indicando que la consulta no pudo ser validada</p><p></p>|EP05|
|EP03/US16|Visualizar datos de perfil de usuario|**Como** visitante **quiero** visualizar mi perfil de usuario **para** reconocer mi información personal brindada.|<p>**Escenario 1:** “Visitante” visualiza sus datos ingresados en la aplicación.</p><p>**Dado que** me encuentro logueado en la aplicacion. Cuando me dirijo a la seccion “Mi perfil”. **Entonces**, visualizo todos mis datos registrados en la aplicacion.</p><p>**Escenario 2:** “Visitante” no visualiza sus datos ingresados en la aplicación.</p><p>**Dado que** me encuentro logueado en la aplicacion. Cuando me dirijo a la seccion “Mi perfil”. **Entonces**, me devuelve un mensaje de error.</p>|EP01|
|<p>EP02/US17</p><p></p>|Confirmar asistencia|**Como** visitante del segmento objetivo de “Attendee”, **quiero** confirmar mi asistencia al evento **para** participar en las actividades planificadas.|<p>**Escenario 1:** Attende recibe su pulsera inteligente.</p><p>**Dado que** me encuentro en la dirección del evento. **Cuando** este ingresando al lugar muestro el código QR de mi compra en la entrada. **Y** se valida mis datos correctamente. **Entonces**, se verifica mi asistencia al evento y recibo mi pulsera inteligente</p><p>**Escenario 2:** Attende no recibe su pulsera inteligente.</p><p>**Dado que** me encuentro en la dirección del evento. **Cuando** este ingresando al lugar muestro el código QR de mi compra en la entrada. **Y** no se valida mis datos. **Entonces, no se valida mi asistencia al evento ni recibo mi pulsera inteligente.**</p>|EP03|
|<p>EP02/US18</p><p></p>|Libre ingreso y salida del evento|**Como** visitante del segmento objetivo de “Attendee”**, quiero** salir o ingresar nuevamente del evento **para** gestionar mis necesidades personales|<p>**Escenario 1:** Attende ingresa o sale del evento libremente</p><p>**Dado que** ya registré mi asistencia al evento. **Cuando** aviso de mi salida prematura en el punto de entrada del evento. Y me confirman. **Entonces**, salgo o ingreso al evento.</p><p>**Escenario 2:** Attende no puede ingresar o salir del evento libremente</p><p>**Dado que** ya registré mi asistencia al evento. **Cuando** aviso de mi salida prematura en el punto de entrada del evento. Y no me confirman. **Entonces**, no salgo salgo o ingresar del evento.</p>|EP03|
|<p>EP04/US19</p><p></p>|Reconocer a los que asisten al evento|**Como** “Organizer”, **quiero** observar la lista de asistentes al evento, **para** conocer el aforo y quienes han llegado y faltan llegar|<p>Escenario 1: Organizer confirma quienes asisitieron a su evento </p><p>Dado que soy un Organizer. Cuando revise mi lista de asistentes a eventos. Entonces, visualizo una confirmación de quienes han llegado y quiénes no.</p><p>Escenario 2: Organizer no puede confirmar quienes asisitieron a su evento </p><p>Dado que soy un Organizer Cuando vaya a la secci[on asistentes del evento, Entonces, no puedo visualizar la lista y me aparece un mensaje de error.</p>|EP03|
|<p>EP04/US20</p><p></p>|Atención en casos de emergencia|**Como** visitante del segmento objetivo de “Organizer”, **quiero** tener acceso a informes y análisis de las pulseras inteligentes, **para** estar atento a un caso de emergencia.|<p>**Escenario 1:** Organizar recibe una alerta de emergencia</p><p>**Dado** que soy un Organizer, **cuando** en una pulsera se detecta una emergencia en los signos vitales de un asistente. **Entonces**, recibo una alerta para tomar las acciones necesarias.</p><p>Escenario 2: Organizar no recibe una alerta de emergencia</p><p>**Dado** que soy un Organizer, **cuando** hay una emergencia en el evento. Y la pulsera no lo detacta. **Entonces**, tomo las acciones necesarias por mi cuenta.</p>|EP03|
|EP04/US21|Un asistente ubica a otro|**Como** visitante del segmento objetivo de “Attendee”, **quiero** hacer uso de un gps, **para** encontrarme con mi acompañante|<p>**Escenario 1:** Organizar recibe una alerta de emergencia</p><p>**Dado** que soy un Attendee. **Cuando** estoy dentro del evento. Y quiero encontrarme con mi acompañante. **Entonces**, uso un gps proporcionado por la aplicacion para encontrar a mi acompañante.</p><p>Escenario 2: Organizar no recibe una alerta de emergencia</p><p>**Dado** que soy un Attendee. C**uando** estoy dentro del evento. Y quiero encontrarme con mi acompañante. Y el gps proporcionado por la aplicacion no está disponible. **Entonces**, tengo inconveniente para encontrar a mi acompañante facilmente.</p>|EP03|



## 3.3. Impact Mapping

El Impact mapping es una técnica de planificación ligera y colaborativa para los equipos, como el nuestro, que desean tener un gran impacto con los productos de software. Se basa en el diseño de la interacción del usuario, la planificación basada en resultados y la asignación mental.

![Imagen que contiene Diagrama Descripción generada automáticamente](Aspose.Words.a0dd4f9a-8c6c-4a02-978d-f8d17446a191.003.png)
![Imagen que contiene Texto Descripción generada automáticamente](Aspose.Words.a0dd4f9a-8c6c-4a02-978d-f8d17446a191.004.png)

## 3.4. Product Backlog

Se realizo el Product Backlog para elaborar un listado de orden de prioridad de los criterios que deben de tenerse en cuenta durante el desarrollo del proyecto.

|**#Orden**|**User Story ID**|**Título**|**Descripción**|**Story Points (1/2/3/5/8)**|
| :-: | :-: | :-: | :-: | :-: |
|1|US05 |Registrar un evento social  |**Como** visitante del segmento objetivo de “Organizer” **quiero** crear eventos para promocionarlos  |8|
|2|US04 |Visualizar eventos sociales  |**Como** visitante del segmento objetivo de “Attendee” **quiero** encontrar eventos sociales para reservar entradas|5|
|3|US14 |Visualizar los detalles de un evento |**Como** visitante del segmento objetivo de “Attendee” **quiero** ver los detalles de un evento **para** decidir adquirir boletos de ello.|5|
|4|US06 |Conocer precio de los boletos |**Como** visitante del segmento objetivo de “Attendee” **quiero** conocer el precio de los boletos **para** asistir al evento social de mi interés  |3|
|5|US07 |Obtener el/los boleto/s de un evento social  |**Como** visitante del segmento objetivo de “Attendee” **quiero** obtener el/los boleto/s **para** asistir al evento social de mi interés|8|
|6|US13 |Mostrar la lista de asistentes de un evento |**Como** visitante del segmento objetivo de “Organizer” **quiero** ver la lista de personas que asistieron a mi evento **para** administrar tal información|8|
|7|US17 |Confirmar asistencia |**Como** visitante del segmento objetivo de “Attendee”, **quiero** confirmar mi asistencia al evento **para** participar en las actividades planificadas.|5|
|8|US19 |Reconocer a los que asisten al evento |**Como** “Organizer”, **quiero** observar la lista de asistentes al evento, **para** conocer el aforo y quienes han llegado y faltan llegar|5|
|9|US10 |Visualizar historial de eventos |**Como** visitante del segmento objetivo de “Organizer” **quiero** visualizar el historial de todos los eventos que he creado, **para** tener un registro de cada uno de ellos|5|
|10|US21 |Un asistente ubica a otro |**Como** visitante del segmento objetivo de “Attendee”, **quiero** hacer uso de un gps, **para** encontrarme con mi acompañante|8|
|11|US20 |Atención en casos de emergencia |**Como** visitante del segmento objetivo de “Organizer”, **quiero** tener acceso a informes y análisis de las pulseras inteligentes, **para** estar atento a un caso de emergencia.|8|
|12|US18 |Libre ingreso y salida del evento |**Como** visitante del segmento objetivo de “Attendee”**, quiero** poder salir o ingresar nuevamente del evento **para** gestionar mis necesidades personales|5|
|13|US03 |Registrar Usuario en la aplicación |**Como** visitante **quiero** crear una cuenta en la aplicación **para** hacer uso de los servicios de esta|5|
|14|US15 |Iniciar sesión   |**Como** visitante **quiero** ingresar sesión en la aplicación **para** disfrutar de los beneficios de esta|3|
|15|US16 |Visualizar datos de perfil de usuario |**Como** visitante **quiero** visualizar mi perfil de usuario **para** reconocer mi información personal brindada.|3|
|16|US11 |Editar perfil de usuario de “Attendee” |**Como** visitante del segmento objetivo de “Attendee” **quiero** visualizar mi perfil **para** poder editar mis datos.|5|
|17|US12 |Editar perfil de usuario de “Organizer” |**Como** visitante del segmento objetivo de “Organizer” **quiero** visualizar mi perfil **para** poder editar mis datos.|5|
|18|US09 |Mostrar el apartado de preguntas frecuentes (FAQ) |**Como** visitante **quiero** acceder a una ventana de preguntas frecuentes (FAQ) **para** encontrar respuestas rápidas a preguntas frecuentes.|1|
|19|US01 |Conocer propósito del sitio web  |**Como** visitante **quiero** conocer el propósito del sitio web **para** conocer qué es lo que ofrece a los usuarios|3|
|20|US02 |Conocer a qué tipo de usuario satisfacen |**Como** “visitante” **quiero** conocer a qué tipo de usuarios satisface esta aplicación **para** decidir obtenerla o no|3|
|21|US08 |Conocer más información del startup |**Como** visitante **quiero** conocer quiénes son los creadores de la aplicación y que ofrecen con la misma **para** advertir los beneficios que me pueden brindar con su uso|3|
|22|TS01 |Acceder a EndPoints |Como developer quiero acceder a endpoints para interactuar con la aplicación  |8|
|23|TS02 |Registrar asistentes |**Como** Developer **quiero** contar con un endpoint **para** registrar asistentes a eventos**  |8|
|24|TS03 |Registrar organizadores |**Como** developer **quiero** contar con un endpoint **para** registrar a los organizadores de eventos**  |8|
|25|TS04 |Registrar Pago |**Como** developer **quiero** contar con un endpoint **para** registrar los pagos realizados de los eventos**  |8|
|26|TS05 |Registrar eventos |**Como** developer **quiero** contar con un endpoint **para** registrar los eventos**  |8|
|27|TS06 |Creación de persistencia de la entidad Organizer |Como developer necesito hacer persistir los datos de la entidad Organizer  |8|
|28|TS07 |Creación de persistencia de la entidad Attendee |Como developer necesito hacer persistir los datos de la entidad Attendee  |8|
|29|TS08 |Creación de persistencia de la entidad Payment |Como developer necesito hacer persistir los datos de la entidad Payment  |8|
|30|TS09 |Creación de persistencia de la entidad Event |Como developer necesito hacer persistir los datos de la entidad Event  |8|
|31|TS10 |Creación de resource de la entidad Organizer |Como developer necesito devolver un resource de los datos de la entidad Organizer  |8|
|32|TS11 |Creación de resource de la entidad Payment |Como developer necesito devolver un resource de los datos de la entidad Payment  |8|
|33|TS12 |Creación de resource de la entidad Attendee |Como developer necesito devolver un resource de los datos de la entidad Attendee  |8|
|34|TS13 |Creación de resource de la entidad Event |Como developer necesito devolver un resource de los datos de la entidad Event  |8|


**Product Backlog del proyecto en la herramienta Pivotal Tracker:**

[Ver enlace 6](#_anexos)

![Interfaz de usuario gráfica, Texto, Aplicación Descripción generada automáticamente](Aspose.Words.a0dd4f9a-8c6c-4a02-978d-f8d17446a191.005.png)

