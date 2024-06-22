### Índice
- [4.2. Tactical-Level Domain-Driven Design](https://github.com/CrackeletsGroup-IoT/upc-pre-202401-si572-sw71-CrackeletsGroup-report-tf/blob/capitulo4/capitulo4/CAPITULO%20IV.md#42-tactical-level-domain-driven-design)
  - [4.2.4. Bounded Context: Security](#424-bounded-context--security)
    - [4.2.4.1. Domain Layer](#4241-domain-layer)
    - [4.2.4.2. Interface Layer](#4242-interface-layer)
    - [4.2.4.3. Application Layer](#4243-application-layer)
    - [4.2.4.4. Infrastructure Layer](#4244-infrastructure-layer)
    - [4.2.4.5. Bounded Context Software Architecture Component Level Diagrams](#4245-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.4.6. Bounded Context Software Architecture Code Level Diagrams](#4246-bounded-context-software-architecture-code-level-diagrams)
      - [4.2.4.6.1. Bounded Context Domain Layer Class Diagrams](#42461-bounded-context-domain-layer-class-diagrams)
      - [4.2.4.6.2. Bounded Context Database Design Diagram](#42462-bounded-context-database-design-diagram)

### 4.2.4. Bounded Context:  Security

#### 4.2.4.1. Domain Layer

En la capa de dominio del bounded context de Security se encuentran los modelos de Rol, para gestionar los permisos de la aplicación, y User, que contiene la información del usuario, distinta a la del perfil.

**Aggregate 1**

| **Nombre** | **Categoría** | **Propósito**                                        |
|:----------:|:--------------|:-----------------------------------------------------|
|    User    | Entity        | Entidad que representa a un usuario de la aplicación |

*Atributos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|Id|Long|Private|Identificador del user|
|Username|String|Private|Nombre de usuario|
|Email|String |Private|Email del usuario|
|Password|String|Private |Contraseña del usuario|

*Métodos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|Constructor|Void|Public|Constructor de la entidad usuario|

**Aggregate 2**

|**Nombre**|**Categoría**|**Propósito**|
| :-: | :- | :- |
|Role|Entity|Entidad que representa a los roles de la aplicación: Admin, User, Organizer|

*Atributos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|Id|Long|Private|Identificador del user|
|Name|String|Private|Nombre del rol|

#### 4.2.4.2. Interface Layer
En la capa de Interface se moldean los controladores que se comunicaran con la interfaz de usuario. Para este bounded context solo se ha agregado un controlador: User Controller. Role no tiene controlador porque no tiene interacción con el usuario.

**Controller**

|**Nombre**|**Categoría**|**Propósito**|
| :-: | :- | :- |
|UserController|Controller|Controlador de usuario para los métodos CRUD|

*Atributos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|UserService|UserService|Private|Servicio de user para aplicar las reglas de negocio|
|Mapper|UserMapper|Private|Mapper para la entidad User|

*Métodos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|authenticateUser|ResponseEntity|Public|Método para el inicio de sesión de un usuario|
|registerUser|ResponseEntity|Public|Método para el registro de un nuevo usuario|
|getAllUsers|ResponseEntity|Public|Método para retornar la lista de usuarios registrados|


#### 4.2.4.3. Application Layer

En la capa de aplicación se ha armado los servicios para cada entidad del bounded context. Para esta capa se han construido los servicios de User y Role respectivamente. El servicio de User se concentra en la authenticación del usuario y su registro.

**Service 1**

|**Nombre**|**Categoría**|**Propósito**|
| :-: | :- | :- |
|UserService|Service|Servicio con la lógica de negocio para User|

*Atributos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|UserRepository|UserRepository|Private|Repositorio de User|
|RoleRepository|RoleRepository|Private|Repositorio de Role|
|authenticationManager|AuthenticationManager|Private||
|Handler|JwtHandler|Private||
|Encoder|PasswordEncoder|Private||

*Métodos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|Authentication|ResponseEntity|Public|Authenticación de un usuario al iniciar sesión|
|Register|ResponseEntity|Public|Registrar un nuevo usuario|
|getAll|List|Public|Retornar lista de usuarios registrados|
|LoadUserByName|UserDetails|Public|Cargar usuario por nombre de usuario|

|**Service 2**

|**Nombre**|**Categoría**|**Propósito**|
| :-: | :- | :- |
|RoleService|Service|Servicio con la lógica de negocio para Role|

*Atributos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|Default\_Roles|Array|Private|Array de Strings con los roles de la aplicación|
|RoleRepository|RoleRepository|Private|Repositorio de Role|

*Métodos*

|**Nombre**|**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|seed|void|Public|Guarda los roles en el repositorio|
|getAll|List|Public|Retonar lista de todos los Roles|

#### 4.2.4.4. Infrastructure Layer

En la capa de Infrastructura se encuntran los repositorios que se comunican con la base de datos. En el repositorio de Rol se encuentran los roles disponibles de la aplicación mientras que el de Usuario se basa en la busqueda y verificación de usuarios.

**Repository 1**

|    **Nombre**    |**Categoría**|**Propósito**|
| :-: | :- | :- |
|  RoleRepository  |Repository|Repositorio para Role|

*Métodos*

|    **Nombre**    |**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|    findByName    |Optional|Public|Retonar role según nombre del rol|
|   existsByName   |Boleean|Public|Verificar si existe un rol según nombre del rol|

**Repository 2**

|    **Nombre**    |**Categoría**|**Propósito**|
| :-: | :- | :- |
|  UserRepository  |Repository|Repositorio para User|

*Métodos*

|    **Nombre**    |**Tipo de retorno**|**Visibilidad**|**Descripción**|
| :-: | :- | :- | :- |
|  findByUsername  |Optional|Public|Encontrar usuarios por nombre de usuario|
| existsByUsername |Boleean|Public|Verificar la existencia de un usuario según nombre de usuario|
|  existsByEmail   |Boleean|Public|Verificar la existencia de un usuario según email|



#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams

![Una captura de pantalla de un celular con letras Descripción generada automáticamente con confianza media](Aspose.Words.ca98a84d-2f9e-4792-821f-4ab9bf9a28f1.001.png)


#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams

![Imagen que contiene Interfaz de usuario gráfica Descripción generada automáticamente](Aspose.Words.ca98a84d-2f9e-4792-821f-4ab9bf9a28f1.002.png)

##### 4.2.4.6.2. Bounded Context Database Design Diagram

![Diagrama](Aspose.Words.ca98a84d-2f9e-4792-821f-4ab9bf9a28f1.003.png)

