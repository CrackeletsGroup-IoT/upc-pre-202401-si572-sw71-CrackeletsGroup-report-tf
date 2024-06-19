### 4.2.1. Bounded Context:  Booking    

En el contexto del bounded context de Booking para eventos, se centra en la gestión y coordinación de reservas para eventos específicos, como conferencias, conciertos, festivales u otras actividades programadas. Este contexto delimitado aborda las necesidades particulares relacionadas con la planificación, reserva y gestión de asistentes para eventos.            

#### 4.2.1.1. Domain Layer

En la capa de Dominio (Domain Layer), el contexto de "Event" se modela utilizando una clase que representa la entidad principal del negocio.

*Aggregate*

| **Nombre**      | **Categoría**     |**Propósito**|
|:--------------------------------------| :- | :- |
|        Event         | Entity/Aggregate  |Representación de un evento con sus atributos requeridos ||

*Atributos*

|      **Nombre**      | **Tipo de dato**  |**Visibilidad**|**Descripción**|
|:--------------------:|:------------------| :- | :- |
|          id          | Long              |Private|Identificador único|
|         name         | String            |Private|Nombre del evento|
|       address        | String            |Private|Dirección del evento|
|       capacity       | String            |Private|Capacidad del evento|
|        Image         | String            |Private|Imagen del evento|
|         date         | Date              |Private|Fecha del evento|
|         cost         | Int               |Private|Costo del evento|
|       district       | String            |Private|Distrito del evento|
| attendeesListByEvent | Set               |Private|Asistentes de un evento|
|       payments       | Set               |Private|Pagos del evento|

*Métodos* 

| **Nombre**       | **Tipo de retorno**|**Visibilidad**|**Descripción**|
|:----------------:|:------------------| :- | :- |
|   addAttendee    | Void              |Public|Añadir un asistente|

#### 4.2.1.2. Interface Layer

En el contexto de Booking, la capa de Interfaz es fundamental para facilitar la interacción entre los usuarios y el sistema de reservas. Esta capa proporciona interfaces intuitivas, como la aplicación web o móvil, donde los usuarios pueden buscar, seleccionar y reservar un evento.

*Controller*

|**Nombre**|**Categoría**|**Propósito**|
| :-: | :- | :- |
|EventsController|Controller|Controlador para  Evento|

*Atributos*

|**Nombre**|**Tipo de dato**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|eventService|EventService|Private|Servicio para Event|
|mapper|EventMapper|Private|Mapper para Event|

*Métodos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|Constructor|Void|Public|Constructor del controlador|
|getAllEvents|Page|Public|Obtener todos los eventos|
|createEvent|EventResource|Public|Crear un evento|
|updateEvent|EventResource|Public|Actualizar datos de un evento|
|deleteEvent|ResponseEntity|Public|Eliminar un evento|

#### 4.2.1.3. Application Layer

La capa de Aplicación en el contexto de Booking se encarga de gestionar la lógica empresarial y la funcionalidad específica de reserva. Esta capa implementa casos de uso como la creación de reservas, la gestión de disponibilidad, y la integración con proveedores de servicios. Actúa como un puente entre la capa de Interfaz y la capa de Dominio.

*Service*

|**Nombre**|**Categoría**|**Propósito**|
| :-: | :- | :- |
|EventService|Service|Servicio con reglas de negocio del Event|

*Atributos*

|**Nombre**|**Tipo de dato**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|eventRepository|EventRepository|Private|Repositorio de Event|
|validator|Validator|Private|Validador de atributos|

*Método*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|getAll|Page/List|Public|Obtener todos los Event en List o Pageable|
|getById|Event|Public|Obtener un Event según su Id|
|create|Event|Public|Crear un Event|
|update|Event|Public|Actualizar datos de un Event|
|delete |ResponseEntity|Public|Eliminar un Event|
|addAttendeeToEvent|Event|Public|Agregar asistente a Event|


#### 4.2.1.4. Infrastructure Layer

En la capa de Infraestructura se gestiona la persistencia de datos; específicamente para el contexto delimitado de Event, se utiliza su propio almacén de datos.

*Repository*

|**Nombre**|**Categoría**|**Propósito**|
| :-: | :- | :- |
|EventRepository|Repository|Repositorio que guarda la información del Event|

*Métodos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|findByName|Event|Public|Devolver la primera coincidencia de Event según nombre|



#### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams

![Diagrama Descripción generada automáticamente](Aspose.Words.2fb0ddb5-1691-49c4-982a-8d6c2ef2b3e0.001.png)

#### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams

![Interfaz de usuario gráfica Descripción generada automáticamente](Aspose.Words.2fb0ddb5-1691-49c4-982a-8d6c2ef2b3e0.002.png)


##### 4.2.1.6.2. Bounded Context Database Design Diagram

![Interfaz de usuario gráfica Descripción generada automáticamente](Aspose.Words.2fb0ddb5-1691-49c4-982a-8d6c2ef2b3e0.003.png)
