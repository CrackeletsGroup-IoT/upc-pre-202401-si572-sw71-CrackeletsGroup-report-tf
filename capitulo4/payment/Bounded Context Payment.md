### Índice
 - [4.2. Tactical-Level Domain-Driven Design](https://github.com/CrackeletsGroup-IoT/upc-pre-202401-si572-sw71-CrackeletsGroup-report-tf/blob/capitulo4/capitulo4/CAPITULO%20IV.md#42-tactical-level-domain-driven-design)
    - [4.2.3. Bounded Context: Payment](423-bounded-context--payment)
        - [4.2.3.1. Domain Layer](#4231-domain-layer)
        - [4.2.3.2. Interface Layer](#4232-interface-layer)
        - [4.2.3.3. Application Layer](#4233-application-layer)
        - [4.2.3.4. Infrastructure Layer](#4234-infrastructure-layer)
        - [4.2.3.5. Bounded Context Software Architecture Component Level Diagrams](#4235-bounded-context-software-architecture-component-level-diagrams)
        - [4.2.3.6. Bounded Context Software Architecture Code Level Diagrams](#4236-bounded-context-software-architecture-code-level-diagrams)
          - [4.2.3.6.1. Bounded Context Domain Layer Class Diagrams](#42361-bounded-context-domain-layer-class-diagrams)
          - [4.2.3.6.2. Bounded Context Database Design Diagram](#42362-bounded-context-database-design-diagram)

### 4.2.3. Bounded Context :  Payment 

En este bounded context se gestiona los pagos que realizan los usuarios dentro de la aplicación.

#### 4.2.3.1. Domain Layer

En la capa de dominio se encuentran nuestros modelos y entidades.

**Entity**

| **Nombre** | **Categoría** | **Propósito**                                            |
|:----------:|:--------------|:---------------------------------------------------------|
|  Payment   | Entity        | Es la clase que representa el pago y sus características |

*Atributos*

| **Nombre** | **Tipo de dato** | **Visibilidad** | **Descripción**                          |
|:----------:|:-----------------|:----------------|:-----------------------------------------|
|     id     | Long             | Private         | Identificador único                      |
|    date    | Date             | Private         | Fecha en la que se realiza el pago       |
|   qrImg    | String           | Private         | Enlace al código QR que confirma el pago |

*Métodos*

| **Nombre**  | **Tipo de retorno** | **Visibilidad** | **Descripción**          |
|:-----------:|:--------------------|:----------------|:-------------------------|
| Constructor | Void                | Public          | Constructor para Payment |

#### 4.2.3.2. Interface Layer

**Controller**

|    **Nombre**     | **Categoría** | **Propósito**            |
|:-----------------:|:--------------|:-------------------------|
| PaymentController | Controller    | Controlador para Payment |

*Atributos*

|   **Nombre**   | **Tipo de dato** | **Visibilidad** | **Descripción**       |
|:--------------:|:-----------------|:----------------|:----------------------|
| paymentService | PaymentService   | Private         | Servicio para Payment |
|     mapper     | PaymentMapper    | Private         | Mapper para Payment   |

*Métodos*

|   **Nombre**   | **Tipo de retorno**    | **Visibilidad** | **Descripción**             |
|:--------------:|:-----------------------|:----------------|:----------------------------|
|  Constructor   | Void                   | Public          | Constructor del controlador |
| createPayment  | ResponseEntity         | Public          | Crear un Payment            |
| getPaymentById | PaymentResource        | Public          | Buscar Payment según Id     |
| getAllPayment  | Page\<PaymentResource> | Public          | Obtener todos los Payment   |

#### 4.2.3.3. Application Layer

**Service**

|   **Nombre**   | **Categoría** | **Propósito**                                |
|:--------------:|:--------------|:---------------------------------------------|
| PaymentService | Service       | Servicio con la lógica de negocio de Payment |

*Atributos*

|   **Nombre**    | **Tipo de dato**  | **Visibilidad** | **Descripción**        |
|:---------------:|:------------------|:----------------|:-----------------------|
|paymentRepository| PaymentRepository | Private         | Repositorio de Payment |
|    validator    | Validator         | Private         | Validador de atributos |

*Método*   

| **Nombre** | **Tipo de retorno** | **Visibilidad** | **Descripción**                              |
|:----------:|:--------------------|:----------------|:---------------------------------------------|
|   getAll   | PageList\<Payment>  | Public          | Obtener todos los Payment en List o Pageable |
|  getById   | Payment             | Public          | Obtener un Payment según su Id               |
|   create   | Payment             | Public          | Crear un Payment                             |
|   delete   | ResponseEntity      | Public          | Eliminar un Payment                          |

#### 4.2.3.4. Infrastructure Layer

**Repository**

|    **Nombre**     | **Categoría** | **Propósito**                     |
|:-----------------:|:--------------|:----------------------------------|
| PaymentRepository | Repository    | Repositorio que almacena Payments |

*Métodos*

| **Nombre** | **Tipo de retorno** | **Visibilidad** | **Descripción**                                         |
|:----------:|:--------------------|:----------------|:--------------------------------------------------------|
| findByDate | Payment             | Public          | Devolver la primera coincidencia de Payment según Fecha |



#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams

![Diagrama Descripción generada automáticamente](Aspose.Words.899d9df1-c45f-47c8-8b32-bcdffb4a0c6e.001.png)



#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams
##### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams

![Imagen que contiene metal, lado, estacionado, tabla Descripción generada automáticamente](Aspose.Words.899d9df1-c45f-47c8-8b32-bcdffb4a0c6e.002.png)
 
##### 4.2.3.6.2. Bounded Context Database Design Diagram

![Pantalla de computadora con letras Descripción generada automáticamente con confianza media](Aspose.Words.899d9df1-c45f-47c8-8b32-bcdffb4a0c6e.003.png)

