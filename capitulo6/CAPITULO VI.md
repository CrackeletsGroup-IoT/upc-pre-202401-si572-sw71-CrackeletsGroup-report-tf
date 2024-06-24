# Índice
- [CAPITULO VI: PRODUCT IMPLEMENTATION, VALIDATION & DEPLOYMENT](#capitulo-vi-product-implementation-validation--deployment)
  - [6.1. Software Configuration Management](#61-software-configuration-management)
    - [6.1.1. Software Development Enviorement Configuration](#611-software-development-enviorement-configuration)
    - [6.1.2. Source Code Management](#612-source-code-management)
    - [6.1.3. Source Code Style & Conventions](#613-source-code-style-guide--conventions)
    - [6.1.4. Software Deployment Configuration](#614-software-deployment-configuration)
  - [6.2. Landing Page, Services & Applications Implementation](#62-landing-page-services--applications-implementation)
    - [6.2.1. Sprint 1](https://github.com/CrackeletsGroup-IoT/upc-pre-202401-si572-sw71-CrackeletsGroup-report-tf/blob/capitulo6/capitulo6/sprint1/Sprint%201.md)
    - [6.2.2. Sprint 2](https://github.com/CrackeletsGroup-IoT/upc-pre-202401-si572-sw71-CrackeletsGroup-report-tf/blob/capitulo6/capitulo6/sprint2/Sprint%202.md)
  - [6.3. Validation Interviews]()
    - [6.3.1. Diseño de Entrevistas]()
    - [6.3.2. Registro de Entrevistas]()
    - [6.3.3. Evaluaciones según heurísticas]()
  - [6.4. Video About-the-Product]()


# CAPITULO VI: PRODUCT IMPLEMENTATION, VALIDATION & DEPLOYMENT

## 6.1. Software Configuration Management
### 6.1.1. Software Development Enviorement Configuration

**Product UX/UI Design:**

*Figma:*

- *Descripción: Un programa de edición gráfica y prototipado. Una plataforma que se utiliza principalmente para el diseño digital, es decir, para diseñar páginas web e interfaces de aplicaciones

- *Propósito en el proyecto: Para el diseño del proyecto, el equipo ha utilizado Figma para la creación de los wireframes de alta fidelidad, así como para la elaboración de los prototipos de la aplicación web y móvil.

- *Ruta: <https://www.figma.com/login>  


*Lucidchart:*

- *Descripción: Permite que los usuarios creen borradores y compartan diagramas de flujo profesionales, proporcionando diseños para todo, desde procesos de lluvia de ideas hasta administración de proyectos.

- *Propósito en el proyecto: Para los wireflows, user flows y diagramas de clases.

- *Ruta: <https://lucid.app/es-LA/users/login#/loggedOut>  

*UXPressia:*

- *Descripción: es una herramienta en línea para el mapeo de la trayectoria del cliente que crea mapas de impacto y personas. 

- *Propósito en el proyecto: Para la elaboración de user personas e integrados con los múltiples mapas para evaluar sus prioridades.

- *Ruta: <https://uxpressia.com/>  

**Software Development:**   

*Angular:*

- *Descripción: es un framework de ingeniería de software de código abierto mantenido por Google, que sirve para desarrollar aplicaciones web de estilo Single Page Application (SPA) y Progressive Web App (PWA). Sirve tanto para versiones móviles como de escritorio.

- *Propósito en el proyecto: Para el desarrollo del software, el equipo utilizó Angular para el frontend, permitiéndonos crear una aplicación eficiente y escalable. 

- *Ruta: <https://angular.io/guide/styleguide>  

*HTML5:*

- *Descripción: es la quinta revisión del lenguaje HTML y permite definir los nuevos estándares de desarrollo web, modificando el código existente para solucionar problemas y actualizándolo a las nuevas necesidades de hoy en día.

- *Propósito en el proyecto: Lenguaje para elaboración del landing page.

- *Ruta: <https://www.w3schools.com/html/html5_syntax.asp>  

*CSS3:*

- *Descripción: un tipo de lenguaje que permite generar el diseño visual de páginas web e interfaces de usuario.

- *Propósito en el proyecto: Tecnología para darle estilo a nuestra página web.

- *Ruta: <https://google.github.io/styleguide/htmlcssguide.html>  

*JavaScript:* 

- *Descripción: es un lenguaje de programación basada en prototipos, multiparadigma, de un solo hilo, dinámico, con soporte para programación orientada a objetos, imperativa y declarativa (por ejemplo, programación funcional).

- *Propósito en el proyecto: Lenguaje de programación orientado a objetos, que nos sirvió para implementar funcionalidades en nuestra Landing Page.

- *Ruta: <https://developer.mozilla.org/es/docs/Web/JavaScript>  

**Software Deployment:** 

*GitHub:* 

- *Descripción: te permite subir tus repositorios de código para almacenarlos en la nube mediante el sistema de control de versiones de Git y participar en proyectos de terceros.

- *Propósito en el proyecto: Para alojar y desplegar el landing page y frontend, asi como poder visualizar e interactuar con el trabajo presentado. Git para poder realizar el control de versions

- *Ruta: <https://github.com/>  

*Zeabur:*

- *Descripción: Utiliza un proveedor de servicios en la nube para desplegar un servicio web, en este caso se utilizó un servidor de Amazon.

- *Ruta: <https://zeabur.com/> 

**Software Documentation:** 

GitHub es una compañía sin fines de lucro que ofrece un servicio de hosting de repositorios almacenados en la nube. En nuestro proyecto se utiliza para potenciar el trabajo colaborativo entre miembros del equipo permitiéndonos trabajar con repositorios remotos almacenados dentro de los distintos proyectos del startup como el Landing Page, en donde cada miembro del equipo se encarga de una parte especifica del proyecto trabajando de modo modular.

### 6.1.2. Source Code Management

Utilizamos GitHub como plataforma y sistema de control de versiones.

**Link de la organización en GitHub:** <https://github.com/orgs/CrackeletsGroup-IoT/repositories>

**Link del repositorio para el Landing Page:** <a name="_int_x3nxpq4m"></a>https://github.com/CrackeletsGroup-IoT/the-big-fun-landing-page

**Link del repositorio para el Frontend Web Applications:** <a name="_int_n7qqtb1f"></a><https://github.com/CrackeletsGroup-IoT/the-big-fun-landing-page>

**Link del repositorio para el Web Services:** <https://github.com/CrackeletsGroup-IoT/the-big-fun-web-application>

Para la implementación del flujo de trabajo Gitflow, usando la herramienta de control de versiones Git, se usó de referencia la entrada de blog “A successful Git branching model” de Vincent Driessen, que nos ayudó a detallar las siguientes convenciones que se usarán en el proyecto:

![Imagen que contiene pequeño, colgando, alambre, verde Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.001.png)


**Master Branch**

La Master branch es la principal rama de desarrollo del proyecto. En esta rama se encontrará el código que se encuentra actualmente en producción.

Notación: master

**Develop Branch**

La Develop branch será la rama que contendrá las últimas actualizaciones y cambios agregados que se entregarán en la siguiente versión del proyecto.

Notación: develop

Creación:

    git checkout -b develop master

**Release Branch**

La Release branch ayudará a la preparación de una nueva versión del producto. Esta rama permitirá solucionar errores y a la rama Develop recibir más actualizaciones.
Debe derivarse de la rama Develop.
Debe fusionarse con la rama Develop y Master.

Notación: release

Creación: 
    
    git checkout -b release develop

**Feature branches**

Las Feature branches se utilizarán para desarrollar nuevas funcionalidades o características del producto que se agregarán en la siguiente versión o en versiones futuras. Estas funcionalidades se deberán fusionar eventualmente a la rama Develop.
Debe derivarse de la rama Develop.
Debe fusionarse de vuelta a la rama Develop.

Notación: 

- Para los user stories       : feature/<us-->/create-<name>-component

- Para los technical stories: technical/<ts-->/create-<name>

Creación: 

    git checkout -b feature/[name of feature] develop

**Hotfix branch**

La Hotfix branch se utilizará para solucionar y actuar de manera inmediata a posibles errores de la versión en producción del producto. La principal característica de esta rama es que permite preparar una solución rápida mientras que el resto del equipo continúa trabajando.
Debe derivarse de la rama Master.
Debe fusionarse con la rama Develop y Master.

Notación: hotfix

Creación: 
    
    git checkout -b hotfix master

**Semantic Versioning**

Para la redacción de las siguientes convenciones del nombramiento de versiones se utilizó de referencia el artículo Semantic Versioning 2.0.0.

- Cada número de versión debe tener la forma X.Y.Z conformado solo por números enteros no negativos. Donde X esla versión principal, Y la versión secundaria y Z la versión de parche.

- La versión inicial tendrá la forma 0.X.Y.

- La versión de parche Z debe incrementarse solo si se corrigen errores compatibles con versiones anteriores.

- La versión secundaria Y debe incrementarse si introduce una nueva funcionalidad compatible con versiones anteriores. Puede incrementar si se introducen mejoras en el código privado. Puede incluir cambios en el parche. Cada vez que aumenta la versión secundaria, la versión del parche debe restablecerse a 0.

- La versión principal X debe incrementarse cuando se introducen funcionalidades incompatibles con versiones anteriores. También pueden introducirse algunos cambios y correcciones en el nivel de parche. El parche y la versión secundaria deben restablecerse a 0.

**Conventional Commits**

Para la redacción de las siguientes convenciones de commits se utilizó de referencia el artículo Conventional Commits 1.0.0.

Se debe seguir la siguiente estructura para un commit:

    git commit -m “<type>[optional scopel: <title>"-m "<description"

*Types:*

- add: se usará para indicar que se añadieron archivos o carpetas.

- fix: este tipo de commit se utilizará para la confirmación de una corrección de un error en el código.

- feat: este tipo de commit se utilizará para la confirmación de que se ha añadido una nueva funcionalidad.

- test: se usará para indicar que se añadieron archivos de test

* BREAKING CHANGE: este tipo de commit se utilizará para confirmar la introducción de un cambio importante en el código.

*Optional scope*

[optional scope]: el optional scope se utilizará para solo en las ramas release, hotfix y master para indicar la versión del producto.


### [6.1.3. Source Code Style Guide & Conventions](https://github.com/CrackeletsGroup-IoT/upc-pre-202401-si572-sw71-CrackeletsGroup-report-tf/blob/capitulo6/capitulo6/Source%20Code%20Conventions.md)

### 6.1.4. Software Deployment Configuration

**Despliegue del Landing Page:**

Link de despliegue: [https://crackeletsgroup-iot.github.io/the-big-fun-landing-page/](https://crackeletsgroup-iot.github.io/the-big-fun-landing-page/)

Paso 1:

Subir todos los archivos y carpetas de la landing page en el repositorio de la organización. No olvidarse del archivo Index.html que nos servirá más adelante para ejecutar el despliegue.

![Captura de pantalla de computadora
Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.003.png)

Paso 2:

Para configurar la opción de deployment debemos dirigirnos a Settings > Pages y elegir la rama en donde se encuentra el proyecto, después darle click en save para guardar los cambios.

![Captura de pantalla de computadora
Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.004.png)

Paso 3:

Copia el link de la landing page que te da github page y agregale “/Index.html” en un navegador.

![Captura de pantalla de un celular
Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.005.png)

![](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.006.png)


**Web Application Frontend**

Creamos un proyecto en la plataforma de Firebase Register

![Interfaz de usuario gráfica, Texto, Aplicación
Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.007.png)

Luego tenemos que instalar el firebase a través de
    
    npm install -g firebase-tools

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.008.png)

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.009.png)

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.010.png)


Después tenemos que iniciar sesión, en caso no tengas la sesión de Google iniciada, te manda un link en el cual te solicitará que nos registremos para poder seguir haciendo uso.


Después tenemos que ejecutar el directorio raíz el comando para realizar esto es
    
    firebase init

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.011.png)

Nos preguntarán si queremos proceder, en este caso le damos que sí.

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.012.png)

![Texto](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.013.png)

En este apartado nos pide elegir qué feature queremos instalar en el directorio, en este caso elegimos el hosting porque nuestro objetivo es hostear nuestro sitio web y seleccionamos que sea opcional el setup github action deploys:

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.014.png)


Nos preguntan que, si deseamos usar un proyecto existente o crear uno nuevo, en este caso ya tenemos uno generado así que le damos a usar un proyecto existente tenemos:

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.015.png)

Una vez realizado esto nos muestra el nombre de nuestro proyecto ya creado en la página de Firebase.

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.016.png)

Nos detecta que ya hay un codebase de angular en nuestro directorio y nos pregunta si deseamos usarlo:

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.017.png)

En este caso nos preguntan si queremos generar un single page dinámico así que aceptamos:

![Captura de pantalla de computadora Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.018.png)

Una vez hechos todos estos pasos, Firebase ha iniciado completamente, generando la información de configuración en el archivo `firebase.json` y la información de nuestro proyecto en `.firebaserc`.

![Captura de pantalla de computadora Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.019.png)

Ahora usamos el comando

    npm run build 
para compilar nuestra aplicación y convertir nuestro código de TypeScript a HTML y CSS.
Le damos Enter y se empezaria a compilar nuestra aplicación:

![Texto Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.020.png)

Como se visualiza, no se ha presentado ningún error, por lo que podemos continuar desplegando nuestra aplicación.
Una vez que nuestra aplicación está corriendo se genera una carpeta en nuestro directorio llamada `dist`.
Nos vamos al apartado de `firebase.json` y colocamos la ruta de la carpeta que se ha creado el cual sería `dist/thebigfun-frontend`, así indicamos que desde esta ruta se va a subir al Firebase.

![Captura de pantalla de computadora Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.021.png)

Por último, colocamos el ultimo comando que es 

    firebase deploy

![Captura de pantalla de computadora Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.022.png)

Una vez cargada la aplicación nos genera los links donde podremos visualizar nuestro proyecto desplegado.

![Captura de pantalla de computadora Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.023.png)

## 6.2. Landing Page, Services & Applications Implementation
### [6.2.1. Sprint 1](https://github.com/CrackeletsGroup-IoT/upc-pre-202401-si572-sw71-CrackeletsGroup-report-tf/blob/capitulo6/capitulo6/sprint1/Sprint%201.md)
### [6.2.2. Sprint 2](https://github.com/CrackeletsGroup-IoT/upc-pre-202401-si572-sw71-CrackeletsGroup-report-tf/blob/capitulo6/capitulo6/sprint2/Sprint%202.md)

## 6.3. Validation Interviews
## 6.4. Video About-the-Product


