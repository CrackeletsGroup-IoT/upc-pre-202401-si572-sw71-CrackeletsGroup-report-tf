### 6.1.3. Source Code Style Guide & Conventions

**Angular:**

• En el caso de HTML, la nomenclatura de los elementos es:

`<name>-content.component.html                                                `

•     	En el caso de CSS, la nomenclatura de los elementos es:

` <name>-content.component.css                                               `

•     	En el caso de TypeScript, la nomenclatura de los elementos es:

`<name>-content.component.ts                                               `

**File structure conventions**

Algunos ejemplos de código muestran un archivo que tiene uno o más archivos complementarios con nombres similares. El uso de este acceso directo hace que las estructuras de archivos de esta guía sean más fáciles de leer y más concisas. Por ejemplo:

`.hero.component.ts |   html    |   css |   spec`

**Appointment**

*General naming Guidelines*

Use nombres consistentes para todos los símbolos. Siga un patrón que describa la característica del símbolo y luego su tipo. El patrón recomendado es :

`feature.type.ts`

*Separate filenames with periods and hyphens*

Use guiones para separar las palabras en el nombre descriptivo. Use puntos para separar el nombre descriptivo del tipo.
Utilice nombres de tipo coherentes para todos los componentes siguiendo un patrón que describa la característica del componente y luego su tipo. 
Un patrón recomendado es:

`feature.type.ts`

Utilice nombres de tipo convencionales como e invente nombres de tipo adicionales si es necesario, pero tenga cuidado de no crear demasiados.

*Servicio:*

Sufija un nombre de clase de servicio con `service`. Por ejemplo, algo que obtiene datos o héroes debe llamarse:

`.ServiceDataServiceHeroService`

Algunos términos son inequívocamente servicios. Por lo general, indican la agencia terminando en "-er".
Es posible que prefiera asignar un nombre a un servicio que registre mensajes en lugar de. Decida si esta excepción es aceptable en su proyecto. Como siempre, esfuérzate por la consistencia

`.LoggerLoggerService`

Para más información sobre las convenciones de CSS se usará como referencia: <https://angular.io/guide/styleguide>

**HTML**

*Use Lowercase Element Names*

Se recomienda usar lowercase para los nombres de los elementos HTML:

    <body>
        <p>This is a paragraph.</p>
    </body>

*Close All HTML Elements*

Se recomienda cerrar todos los elementos HTML:
````
<section>
    <p>This is a paragraph.</p>
    <p>This is a paragraph.</p>
</section>
````

*Use Lowercase Attribute Names*

Se recomienda usar lowercase para los nombres de los atributos HTML:

    <a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a>

*Always Specify alt, width, and height for Images*

Se recomienda seguir estas convenciones en caso de que la imagen no se puede mostrar y ayudar con la disponibilidad del contenido

    <img src="html5.gif" alt="HTML5" style="width:128px;height:128px">

*Spaces and Equal Signs*

Serecomienda no usar espacios en blanco entre las entidades para una mejor lectura:

    <link rel="stylesheet" href="styles.css">

Para más información sobre las convenciones de HTML se usará como referencia: <https://www.w3schools.com/html/html5_syntax.asp>

**CSS**

*Class Naming*

Usar nombres de clases y ID significativos que expresen el propósito del elemento:

    .gallery {}

    .login {}

    .video {}

*Class Name Style*

Usar pronombres cortos para nombrar ID o clases, pero lo suficientemente largo para saber cuál es su propósito

    .nav {}

    .author {}

*Shorthand Properties*

Usar CSS shothand properties tanto como se posible para que el codigo sea mas eficiente y entendible

    border-top: 0;

    font: 100%/1.6 palatino, georgia, serif;

    padding: 0 1em 2em;

*Class Name Delimiters*

Separar las palabras en ID y clases con un guion:

    #video-id {}

    .ads-sample {}

*0 and Units*

Evitar la unidad después de usar 0 en los valores que lo requieran:

    margin: 0;

    padding: 0;

*Declaration Order*

Colocar las declaraciones en orden alfabético para que sea más fácil de mantener y recordar:
```
background: fuchsia;

border: 1px solid;

-moz-border-radius: 4px;

-webkit-border-radius: 4px;

border-radius: 4px;

color: black;

text-align: center;

text-indent: 2em;
```

*Selector and Declaration Separation*

Separar los selectores y declaraciones en nuevas líneas:

````
h1,
h2,
h3 {
  font-weight: normal;
  line-height: 1.2;
}
````
Para más información sobre las convenciones de CSS se usará como referencia: <https://google.github.io/styleguide/htmlcssguide.html>

**JavaScript**

*Use expanded syntax*

Cada línea de JavaScript en una nueva línea con la llave de apertura en la misma línea de su declaración y la llave de cierre en una nueva línea final:

    Function myFunc(){
        Console.log(‘Hello!’);
    }

*Variable naming*

Para el nombre de las variables usar:

    lowerCamelCase:

    let playerScore=0;

    let speed= distance / time;

*Declaring variables:*

Para la declaración de las variables usar las palabras reservadas let y const, no usar var:

````
const myName=’Chris’;

Console.log(myName);

let myAge=’40’;

myAge++;

console.log(‘Happy birthday’);
````

*Use strict equality*

Siempre usar la igualdad o inigualdad estricta:
````
Name===’Chris’;

Age!==25;
````
*Function naming*

Para el nombre de las funciones usar lowerCamelCase:
````
Function sayHello(){

Alert (‘Hello’);

}
````
*Creating objects*

Usar literales para la creación de objetos:

    let myObject = {};

*Object classes*

Usar la sintaxis de clase de ES para objetos:
````
class Person {

    Constructor (name,age,gender){

        this.name = name;

        this.age = age;

        this.gender = gender;

    }

    Greeting(){

        Console.log(`Hi! I’m ${this,name}`);

    };

};
````
*Creating arrays*

Usar literales para la construcción de arrays:

    let myArray = [];

Para más información sobre las convenciones de JavaScript se usará como referencia: <https://developer.mozilla.org/en-US/docs/MDN/Guidelines/Code_guidelines/JavaScript%23creating_arrays>

**TypeScript**

*Visibility*

No es necesario usar el modificador publico cuando se declaran atributos, funciones o métodos públicos:

    class Foo {
        bar = new Bar();
    }

*Constructors*

La llamada  a constructores siempre debe usar paréntesis, incluso cuando reciban ningún parámetro:

    const x = new Foo();

*No #private fields*

No usar campo privados, en su lugar usar las anotaciones de visibilidad de TypeScript

    class Clazz {
        private ident = 1;
    }

*Getters and Setters (Accessors)*

Se pueden usar getters y setter para los miembros de clase, son muy útiles como un medio para restringir la visibilidad de los detalles de implementación internos:

````
class Foo {

    constructor(private readonly someService: SomeService) {}

    get someMember(): string {

        return this.someService.someVariable;

    }

    set someMember(newValue: string) {

        this.someService.someVariable = newValue;

    }

};
````

*Array constructor*

No usar el constructor Array(), en cambio, utilizar la notación de corchetes o from para inicializar una matriz con un cierto tamaño;
````
const a = [2];

const b = [2, 3];

// Equivalent to Array(2):

const c = [];

c.length = 2;

// [0, 0, 0, 0, 0]

Array.from<number>({length: 5}).fill(0);
````
*Variables*

Siempre usar const y let para declarar variables. Nunca usar var:

    const foo = otherValue;

    let bar = someValue;

*Function Declarations*

Usar function para declarar funciones en lugar de asignar una expresión de fuction a una variable local:

    function foo() { ... }

Para más información sobre las convenciones de JavaScript se usará como referencia: <https://google.github.io/styleguide/tsguide.html#visibility>

**JAVA**

*Interface Names*

Los nombres de interfaces utilizarán el sufijo Interface y estarán compuestos por palabras con la primera letra en mayúscula (CamelCase). Se debe evitar el uso de abreviaciones que dificulten la comprensión del código.

Example: `ConexionInterface, ComponenteTablaInterface`

*Class names*

![Tabla Descripción generada automáticamente](Aspose.Words.89381664-fd92-4088-845b-626cbcd03fbf.002.png)

Los nombres de clases deben ser mezclas de mayúsculas y minúsculas, con la primera letra de cada palabra interna en mayúsculas (CamelCase). 
Debemos intentar mantener los nombres de clases simples y descriptivos. Debemos usar palabras completas y evitar acrónimos y abreviaturas (se permiten DAO, DTO, URL, HTML, etc.). Si la clase cumpliese algún patrón determinado o tuviese una funcionalidad específica es recomendable definirlo en el nombre.

*Variables*

Los nombres de las variables tanto de instancia como estáticas reciben el mismo tratamiento que para los métodos, con la salvedad de que aquí sí importa más la relación entre la regla mnemónica y la longitud del nombre.

Ejemplo:

Correctos: `diaCalculo, fechaIncoporacion`

Incorrectos: `dC, DCal, fI, FI¿`

Se evitará en la medida de lo posible la utilización de caracteres especiales, así como nombre sin ningún tipo de significado funcional.

Las excepciones son las variables utilizadas en bucles `for`, para esos casos se permite utilizar `i, j, k, l` y siempre en ese orden de anidamiento.

El primer bucle siempre será el que tenga la variable `i` como iterador. (Esta variable se definirá para el bucle en cuestión).

*Constants*

Los nombres de constantes de clases deberían escribirse todo en mayúsculas con las palabras separadas por subrayados ("_"). Todas serán declaradas como `public static final`.

    public static final String PROPERTY\_URL\_SERVICIO = "urlServicio";

*Use of optional braces*

Las llaves se usan con declaraciones `if, else, for, do` y `while`, incluso cuando el cuerpo está vacío o contiene una sola declaración.

Otras llaves opcionales, como las de una expresión lambda, siguen siendo opcionales.

*Empty blocks: may be concise*

Un bloque vacío o una construcción similar a un bloque puede cerrarse inmediatamente después de abrirse, sin caracteres ni saltos de línea entre `({})`, a menos que forme parte de una declaración de varios bloques (una que contenga directamente varios bloques: `if/else` o `try/catch/finally`).
````
// This is acceptable

    void doNothing() {}

// This is equally acceptable

    void doNothingElse() {

    }
````

*Enum classes*

Después de cada coma que sigue a una constante de enumeración, un salto de línea es opcional. También se permiten líneas en blanco adicionales (generalmente solo una):
````
private enum Answer {

    YES {

       @Override public String toString() {

        return "yes";

        }

    },

    NO,

    MAYBE

}
````
*Package names*

Los nombres de los paquetes usan solo letras minúsculas y dígitos (sin guiones bajos). Las palabras consecutivas simplemente se concatenan juntas. Por ejemplo:

`com.example.deepspace`, not `com.example.deepSpace` or `com.example.deep_space`.

Para más información sobre las convenciones de Java se usará como referencia: <https://google.github.io/styleguide/javaguide.html#s5.1-identifier-names>


**Gherking**

|      Sintaxis      |                                                                                                                                                 Propósito                                                                                                                                                  |
|:------------------:|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
|      FEATURE       |                                                                               El propósito del FEATURE es proporcionar una descripción de alto nivel de una de las funciones de software y agrupar SCENARIOs22 relacionados.                                                                               |
| SCENARIO O EXAMPLE |                                                                                Un SCENARIO es un ejemplo concreto que contiene una regla de negocio. Consiste básicamente en una definición en el patrón ‘Given-When-Then’.                                                                                |
|       GIVEN        | GIVEN es una parte del patrón ‘Given-When-Then’. Se utiliza para describir la escena del escenario. Su propósito es poner el sistema en un estado concreto antes de que el usuario (o sistema externo) comience a interactuar con el sistema. No se habla sobre la interacción del usuario en este patrón. |
|        WHEN        |                                           WHEN es el segundo requisito del patrón ‘Given-When-Then’. Se utiliza para describir un evento o una acción. Puede ser una persona que interactúa con el sistema o puede ser un evento desencadenado por otro sistema.                                           |
|        THEN        |                 THEN, el lo ultimo del patron ‘Given-When-Then’. Permite describir el resultado esperado. La definición de un THEN debe usar una aserción para comparar el resultado real (lo que el sistema hace) con el resultado esperado (lo que se supone que debe hacer el sistema)                  |
|        AND         |                                                                                                            AND se utiliza para añadir condiciones en alguno de los patrones ‘Given-When-Then’.                                                                                                             |
|        BUT         |                                                                                                                    Se utiliza como condición extra para los patrones ‘Given-When-Then’.                                                                                                                    |
|     BACKGROUND     |                   Ocurre que se repiten muchos GIVEN en muchos SCENARIO de una FEATURE. De ser el caso, esto es una indicación de que los patrones no son esenciales para describir los escenarios; son detalles generales. Literalmente, puede moverlos agrupándoles en un BACKGROUND.                    |
