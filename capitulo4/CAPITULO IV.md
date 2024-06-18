# Índice
- [CAPITULO IV: SOLUTION SOFTWARE DESIGN]()
  - []

# CAPITULO IV: SOLUTION SOFTWARE DESIGN



## 4.1. Strategic-Level Domain-Driven Design
### 4.1.1. Event Storming

Para la sesión de event storming nosotros tuvimos una reunión donde expusimos nuestras ideas acerca de este segmento. Con el transcurso de la sesión pudimos encontrar ideas las cuales son muy importantes para nuestra aplicación, además de poder tener las primeras versiones para los bounded context.

Aquí mostraremos como fue nuestro desarrollo del event storming realizado mediante la herramienta Miro.

**STEP 1**

![Una captura de pantalla de un celular con texto e imágenes
Descripción generada automáticamente con confianza baja](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.001.png)

En esta etapa, se identificaron los eventos clave que representan las acciones significativas dentro del sistema. Estos eventos se agruparon según los diferentes segmentos de usuarios y las funcionalidades principales de la aplicación.



**STEP 2: TIMELINES**

![Un conjunto de letras blancas en un fondo blanco
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.002.png)

Durante esta fase, los eventos identificados fueron agrupados en subgrupos liderados por un evento general que encapsula la función principal del grupo. Cada subgrupo incluyó tanto los happy paths, que representan los caminos ideales o exitosos de ejecución de los eventos, como los unhappy paths, que muestran los posibles problemas o situaciones no deseadas que pudieran surgir. Esto ayudó a estructurar los eventos de manera coherente y a comprender mejor las diferentes secuencias de acciones dentro del sistema.




**Step 3: PAINT POINTS**

Durante el proceso, se identificaron los pain points o puntos problemáticos, que son áreas donde los usuarios pueden experimentar dificultades o fricciones en su interacción con la aplicación. Estos puntos son cruciales para mejorar la experiencia del usuario y optimizar el diseño del sistema.

![Escala de tiempo
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.003.png)


**Step 4: PIVOTAL POINTS**

![Diagrama Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.005.png)

Se señalaron los pivotal points o puntos clave, que son eventos críticos que marcan hitos importantes en el flujo de trabajo del sistema. Estos eventos suelen tener un impacto significativo en el comportamiento del sistema o en la experiencia del usuario

![Imagen que contiene Gráfico de cajas y bigotes
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.006.png)



**Step 5: COMMANDS**

![Un conjunto de letras negras en un fondo blanco
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.007.png)

Cada evento se asoció con un comando específico que lo desencadena y un actor que lo realiza. Esto ayudó a clarificar quién es responsable de iniciar cada acción y cómo interactúan los diferentes usuarios con el sistema


![Un conjunto de letras negras en un fondo blanco
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.008.png)

**Step 6: POLICIES**

![Imagen que contiene firmar, pantalla, venta, alimentos
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.009.png)

Durante esta etapa, se identifican y definen las políticas relevantes para cada contexto del sistema. Estas políticas pueden incluir restricciones de negocio, reglas de validación o comportamientos específicos que deben seguirse en determinadas 

**Step 7: READ MODELS**

![Imagen de la pantalla de un celular con letras
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.010.png)

Durante esta fase, se diseñan y desarrollan los modelos de lectura para cada contexto del sistema, asegurando que proporcionen la información necesaria de manera eficiente y coherente

![Un conjunto de letras negras en un fondo blanco
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.011.png)


**Step 8: EXTERNAL SYSTEMS**

![Imagen que contiene Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.012.png)

Durante esta etapa, se identifican los sistemas externos relevantes para cada contexto del sistema y se establecen las interfaces y comunicaciones necesarias para integrarlos de manera efectiva.


**Step 9: AGGREGATES**

Durante esta etapa, se definen y diseñan los agregados para cada contexto del sistema, asegurando que representen correctamente las transacciones y operaciones coherentes dentro del sistema.

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.013.png)


#### 4.1.1.1. Candidate Context Discovery     

Para este punto nosotros elegimos utilizar la técnica de start-with-value ya que pensamos que empezar por el valor de la aplicación (core) es importante para tener una mejor visión del producto.

- **Identificación de Valores del Negocio:** Analizamos los valores clave del negocio, como la experiencia del usuario al reservar eventos, la seguridad en el procesamiento de pagos y la eficiencia en la gestión de perfiles de usuario.

- **Identificación de Funcionalidades Clave:** Identificar las funcionalidades esenciales de la aplicación, como la gestión de perfiles de usuario (Profile), la reserva de eventos (Booking) y el procesamiento de pagos (Payment), que contribuyen directamente a la entrega de los valores empresariales.
- **Priorización de Contextos:** Priorizar los bounded contexts en función de su importancia para el core del negocio y la satisfacción de los usuarios. Identificar los temas claves que se deben desarrollar al principio para lograr rápidamente beneficios funcionales, como mejorar la experiencia del usuario al reservar eventos y garantizar la seguridad en los pagos.

##### Candidate para Bounded Context: Booking

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.014.png)


##### Candidate para Bounded Context: Profile

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.015.png)     


##### Candidate para Bounded Context: Payment

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.016.png)


##### Candidate para Bounded Context: Security

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.017.png)

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.018.png)


#### 4.1.1.2. Domain Message Flows Modeling    

**Usuario**

Scenario: El usuario desea iniciar sesión

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.019.png)



**Attende (Asistente)**

Scenario: Asistente desea pagar las entradas de un evento 

![Escala de tiempo
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.020.png)


**Organizer (Organizador)**

Scenario: Organizador crea un evento 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.021.png)

Scenario: Organizador visualizar a los asistentes de su evento 

![Diagrama
Descripción generada automáticamente con confianza baja](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.022.png)

Link del Miro: <https://miro.com/welcomeonboard/WE0yOExVSTd6Z1JQZzJJcU5PaTdaSWY3SGgxdGhRZk9Kd3ZkMU9Jd2x0b0VuTXowRHR0Q3hTSGZodlpZdWZTVnwzMDc0NDU3MzYwMzgxNjUwNjgxfDI=?share_link_id=694203895269>

#### 4.1.1.3. Bounded Context Canvases 

Link: <https://miro.com/app/board/uXjVKXA46xc=/?share_link_id=35955665241> 

**Booking**

![Texto
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.023.png)



**Profile**

![Interfaz de usuario gráfica, Aplicación
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.024.png)

**Payment**

![Interfaz de usuario gráfica, Aplicación
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.025.png)

**Security**

![Interfaz de usuario gráfica, Aplicación
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.026.png)

### 4.1.2. Context Mapping    

Después de realizar la técnica de EventStorming se identificó 4 bounded Context: Profile, Booking, Payment y Security. 

Se ha decidido hacer uso los patrones de Conformist y de Customer/Supplier:

**Conformist:**

Definición: Los Bounded Contexts tienen modelos de dominio similares y pueden adaptarse fácilmente entre sí sin comprometer la integridad de sus modelos, el enfoque conformista puede ser apropiado.

Uso: El Bounded Context de "Booking" necesita acceder a datos de usuarios y autenticación del Bounded Context de "Profile", y los modelos de usuario y autenticación en "Security" son compatibles con las necesidades de "Booking".


**Customer/Supplier (Cliente/Proveedor):**

Definición: En este patrón, un Bounded Context (cliente) depende de otro Bounded Context (proveedor) para ciertas funcionalidades o datos.

Uso: El Bounded Context de "Payment" es un cliente de "Booking" para realizar transacciones financieras. El Bounded Context de "Profile" es un cliente de "Security" para manejar los datos de usuario.


Link: <https://lucid.app/lucidchart/8ef0e66c-e927-443a-9e41-6ab129aa23d5/edit?viewport_loc=-1810%2C-1218%2C1128%2C721%2C0_0&invitationId=inv_6030b295-fd49-482a-8d80-5c33a7535d54> 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.027.png)



### 4.1.3. Software Architecture     

A continuación, se muestra los diagramas C4 donde se visualiza la arquitectura de la aplicación creada.

#### 4.1.3.1. Software Architecture System Landscape Diagram  

Nuestra Startup cuenta con un sistema de software TheBigFun (aplicación web y móvil), adicionalmente se cuenta con un sistema que maneja dispositivos IoT, el que a su vez se relaciona con un sistema CRM para poder almacenar y gestionar información de nuestros clientes

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.028.jpeg)Link: <https://lucid.app/lucidchart/8ef0e66c-e927-443a-9e41-6ab129aa23d5/edit?viewport_loc=-1810%2C-1218%2C1128%2C721%2C0_0&invitationId=inv_6030b295-fd49-482a-8d80-5c33a7535d54> 


#### 4.1.3.2. Software Architecture Context Level Diagrams      

Link:   <https://structurizr.com/share/81375/c73aa1d5-8609-4de7-88a0-62da5a9750ba> 

En la siguiente imagen se aprecia tres usuarios que interactúan con el sistema, “organizer” y “attendee” son el segmento objetivo, mientras que “admin” somo es rol de desarrollador. Además, existe una dependencia a un sistema externo, GoogleMaps.


![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.029.png)}


#### 4.1.3.3 Software Architecture Container Level Diagrams     

En la siguiente imagen se visualizan cuatro contextos, los cuales sirven para dividir el sistema de la aplicación y poder distribuir las responsabilidades. 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.030.png)




#### 4.1.3.4. Software Architecture Deployment Diagrams 

<https://lucid.app/lucidchart/8ef0e66c-e927-443a-9e41-6ab129aa23d5/edit?viewport_loc=-581%2C-1312%2C2694%2C1313%2C0_0&invitationId=inv_6030b295-fd49-482a-8d80-5c33a7535d54> 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.031.jpeg)


## 4.2. Tactical-Level Domain-Driven Design

### [4.2.1. Bounded Contexts Design]()
### 4.2.2. Aggregates Design
### 4.2.3. Domain Events Design
### 4.2.4. Value Objects Design










## 4.1. Strategic-Level Domain-Driven Design
### 4.1.1. Event Storming

Para la sesión de event storming nosotros tuvimos una reunión donde expusimos nuestras ideas acerca de este segmento. Con el transcurso de la sesión pudimos encontrar ideas las cuales son muy importantes para nuestra aplicación, además de poder tener las primeras versiones para los bounded context.

Aquí mostraremos como fue nuestro desarrollo del event storming realizado mediante la herramienta Miro.

**STEP 1**

![Una captura de pantalla de un celular con texto e imágenes
Descripción generada automáticamente con confianza baja](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.001.png)

En esta etapa, se identificaron los eventos clave que representan las acciones significativas dentro del sistema. Estos eventos se agruparon según los diferentes segmentos de usuarios y las funcionalidades principales de la aplicación.



**STEP 2: TIMELINES**

![Un conjunto de letras blancas en un fondo blanco
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.002.png)

Durante esta fase, los eventos identificados fueron agrupados en subgrupos liderados por un evento general que encapsula la función principal del grupo. Cada subgrupo incluyó tanto los happy paths, que representan los caminos ideales o exitosos de ejecución de los eventos, como los unhappy paths, que muestran los posibles problemas o situaciones no deseadas que pudieran surgir. Esto ayudó a estructurar los eventos de manera coherente y a comprender mejor las diferentes secuencias de acciones dentro del sistema.




**Step 3: PAINT POINTS**

Durante el proceso, se identificaron los pain points o puntos problemáticos, que son áreas donde los usuarios pueden experimentar dificultades o fricciones en su interacción con la aplicación. Estos puntos son cruciales para mejorar la experiencia del usuario y optimizar el diseño del sistema.

![Escala de tiempo
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.003.png)


**Step 4: PIVOTAL POINTS**

![Diagrama Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.005.png)

Se señalaron los pivotal points o puntos clave, que son eventos críticos que marcan hitos importantes en el flujo de trabajo del sistema. Estos eventos suelen tener un impacto significativo en el comportamiento del sistema o en la experiencia del usuario

![Imagen que contiene Gráfico de cajas y bigotes
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.006.png)



**Step 5: COMMANDS**

![Un conjunto de letras negras en un fondo blanco
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.007.png)

Cada evento se asoció con un comando específico que lo desencadena y un actor que lo realiza. Esto ayudó a clarificar quién es responsable de iniciar cada acción y cómo interactúan los diferentes usuarios con el sistema


![Un conjunto de letras negras en un fondo blanco
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.008.png)

**Step 6: POLICIES**

![Imagen que contiene firmar, pantalla, venta, alimentos
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.009.png)

Durante esta etapa, se identifican y definen las políticas relevantes para cada contexto del sistema. Estas políticas pueden incluir restricciones de negocio, reglas de validación o comportamientos específicos que deben seguirse en determinadas 

**Step 7: READ MODELS**

![Imagen de la pantalla de un celular con letras
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.010.png)

Durante esta fase, se diseñan y desarrollan los modelos de lectura para cada contexto del sistema, asegurando que proporcionen la información necesaria de manera eficiente y coherente

![Un conjunto de letras negras en un fondo blanco
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.011.png)


**Step 8: EXTERNAL SYSTEMS**

![Imagen que contiene Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.012.png)

Durante esta etapa, se identifican los sistemas externos relevantes para cada contexto del sistema y se establecen las interfaces y comunicaciones necesarias para integrarlos de manera efectiva.


**Step 9: AGGREGATES**

Durante esta etapa, se definen y diseñan los agregados para cada contexto del sistema, asegurando que representen correctamente las transacciones y operaciones coherentes dentro del sistema.

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.013.png)


#### 4.1.1.1. Candidate Context Discovery     

Para este punto nosotros elegimos utilizar la técnica de start-with-value ya que pensamos que empezar por el valor de la aplicación (core) es importante para tener una mejor visión del producto.

- **Identificación de Valores del Negocio:** Analizamos los valores clave del negocio, como la experiencia del usuario al reservar eventos, la seguridad en el procesamiento de pagos y la eficiencia en la gestión de perfiles de usuario.

- **Identificación de Funcionalidades Clave:** Identificar las funcionalidades esenciales de la aplicación, como la gestión de perfiles de usuario (Profile), la reserva de eventos (Booking) y el procesamiento de pagos (Payment), que contribuyen directamente a la entrega de los valores empresariales.
- **Priorización de Contextos:** Priorizar los bounded contexts en función de su importancia para el core del negocio y la satisfacción de los usuarios. Identificar los temas claves que se deben desarrollar al principio para lograr rápidamente beneficios funcionales, como mejorar la experiencia del usuario al reservar eventos y garantizar la seguridad en los pagos.

##### Candidate para Bounded Context: Booking

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.014.png)


##### Candidate para Bounded Context: Profile

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.015.png)     


##### Candidate para Bounded Context: Payment

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.016.png)


##### Candidate para Bounded Context: Security

![Gráfico, Gráfico en cascada
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.017.png)

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.018.png)


#### 4.1.1.2. Domain Message Flows Modeling    

**Usuario**

Scenario: El usuario desea iniciar sesión

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.019.png)



**Attende (Asistente)**

Scenario: Asistente desea pagar las entradas de un evento 

![Escala de tiempo
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.020.png)


**Organizer (Organizador)**

Scenario: Organizador crea un evento 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.021.png)

Scenario: Organizador visualizar a los asistentes de su evento 

![Diagrama
Descripción generada automáticamente con confianza baja](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.022.png)

Link del Miro: <https://miro.com/welcomeonboard/WE0yOExVSTd6Z1JQZzJJcU5PaTdaSWY3SGgxdGhRZk9Kd3ZkMU9Jd2x0b0VuTXowRHR0Q3hTSGZodlpZdWZTVnwzMDc0NDU3MzYwMzgxNjUwNjgxfDI=?share_link_id=694203895269>

#### 4.1.1.3. Bounded Context Canvases 

Link: <https://miro.com/app/board/uXjVKXA46xc=/?share_link_id=35955665241> 

**Booking**

![Texto
Descripción generada automáticamente con confianza media](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.023.png)



**Profile**

![Interfaz de usuario gráfica, Aplicación
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.024.png)

**Payment**

![Interfaz de usuario gráfica, Aplicación
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.025.png)

**Security**

![Interfaz de usuario gráfica, Aplicación
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.026.png)

### 4.1.2. Context Mapping    

Después de realizar la técnica de EventStorming se identificó 4 bounded Context: Profile, Booking, Payment y Security. 

Se ha decidido hacer uso los patrones de Conformist y de Customer/Supplier:

**Conformist:**

Definición: Los Bounded Contexts tienen modelos de dominio similares y pueden adaptarse fácilmente entre sí sin comprometer la integridad de sus modelos, el enfoque conformista puede ser apropiado.

Uso: El Bounded Context de "Booking" necesita acceder a datos de usuarios y autenticación del Bounded Context de "Profile", y los modelos de usuario y autenticación en "Security" son compatibles con las necesidades de "Booking".


**Customer/Supplier (Cliente/Proveedor):**

Definición: En este patrón, un Bounded Context (cliente) depende de otro Bounded Context (proveedor) para ciertas funcionalidades o datos.

Uso: El Bounded Context de "Payment" es un cliente de "Booking" para realizar transacciones financieras. El Bounded Context de "Profile" es un cliente de "Security" para manejar los datos de usuario.


Link: <https://lucid.app/lucidchart/8ef0e66c-e927-443a-9e41-6ab129aa23d5/edit?viewport_loc=-1810%2C-1218%2C1128%2C721%2C0_0&invitationId=inv_6030b295-fd49-482a-8d80-5c33a7535d54> 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.027.png)



### 4.1.3. Software Architecture     

A continuación, se muestra los diagramas C4 donde se visualiza la arquitectura de la aplicación creada.

#### 4.1.3.1. Software Architecture System Landscape Diagram  

Nuestra Startup cuenta con un sistema de software TheBigFun (aplicación web y móvil), adicionalmente se cuenta con un sistema que maneja dispositivos IoT, el que a su vez se relaciona con un sistema CRM para poder almacenar y gestionar información de nuestros clientes

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.028.jpeg)

Link: <https://lucid.app/lucidchart/8ef0e66c-e927-443a-9e41-6ab129aa23d5/edit?viewport_loc=-1810%2C-1218%2C1128%2C721%2C0_0&invitationId=inv_6030b295-fd49-482a-8d80-5c33a7535d54> 


#### 4.1.3.2. Software Architecture Context Level Diagrams      

Link:   <https://structurizr.com/share/81375/c73aa1d5-8609-4de7-88a0-62da5a9750ba> 

En la siguiente imagen se aprecia tres usuarios que interactúan con el sistema, “organizer” y “attendee” son el segmento objetivo, mientras que “admin” somo es rol de desarrollador. Además, existe una dependencia a un sistema externo, GoogleMaps.


![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.029.png)


#### 4.1.3.3 Software Architecture Container Level Diagrams     

En la siguiente imagen se visualizan cuatro contextos, los cuales sirven para dividir el sistema de la aplicación y poder distribuir las responsabilidades. 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.030.png)




#### 4.1.3.4. Software Architecture Deployment Diagrams 

<https://lucid.app/lucidchart/8ef0e66c-e927-443a-9e41-6ab129aa23d5/edit?viewport_loc=-581%2C-1312%2C2694%2C1313%2C0_0&invitationId=inv_6030b295-fd49-482a-8d80-5c33a7535d54> 

![Diagrama
Descripción generada automáticamente](Aspose.Words.0d655031-c374-4bfe-9bc3-7266c547a909.031.jpeg)


## 4.2. Tactical-Level Domain-Driven Design

### [4.2.1. Bounded Contexts Design]()
### 4.2.2. Aggregates Design
### 4.2.3. Domain Events Design
### 4.2.4. Value Objects Design
