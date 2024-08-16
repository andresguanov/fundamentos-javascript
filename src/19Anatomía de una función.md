Las funciones son bloques de código que se pueden reutilizar en diferentes partes de un programa. Existen dos tipos de funciones: declarativas y expresivas.

## Qué es una función

Una función es un bloque de código que se puede reutilizar en diferentes partes de un programa. Imagina que tienes un bloque de código que se repite en diferentes partes de tu programa. 

En lugar de escribir ese bloque de código cada vez que lo necesites, puedes escribir una función que contenga ese bloque de código y ejecutar esa función cada vez que necesites ejecutar instrucciones.

## Qué son las funciones declarativas

Las funciones declarativas son aquellas que permiten **almacenar un bloque de código** específico que se puede ejecutar en cualquier momento.

Las funciones están constituidas por dos partes: la declaración y la invocación.

* **Declaración**: es el bloque de código que se almacenará en memoria.
* **Invocación**: es el llamado a la función para ejecutar el bloque de código almacenado.

![Estructura de una función en JavaScript](https://static.platzi.com/media/user_upload/image-fe1ff80d-7a98-4499-b30c-e753345af856.jpg)

### Cómo declarar una función

La declaración de una función está constituida por las siguientes partes:

* La palabra reservada `function`.
* El **nombre de la función**: el cual será guardado como referencia en memoria, similar a las variables.
* Los **parámetros**: están envueltos en paréntesis `()`, son variables propias de la función y deberán utilizarse en el contenido. Hacen referencia a los argumentos en la invocación.
* El **bloque de código**: está envuelto por llaves `{}`, contendrá las líneas de código correspondientes a la lógica del problema a reutilizar.
* El **valor retornado**: es un único valor que devuelve la función cuando es llamada. Se lo especifica por la palabra reservada `return`. Si no existe, la función devolverá un valor `undefined` por defecto.


### Cómo invocar una función

La invocación o llamada de la función está constituida por dos partes:

* El **nombre** de la función especificada en la declaración.
* Los **argumentos**: son los valores para cada uno de parámetros de la función.

La invocación de una función sirve para ejecutar el bloque de código almacenado en memoria con diferentes argumentos. La invocación de una función puede ser almacenada en una variable para su posterior uso.

```js
let resultado1 = suma(2,3)
let resultado2 = suma(4,6)
let resultado3 = suma(10,12)

console.log(resultado1) //5
console.log(resultado2) //10
console.log(resultado3) //22
```

También existen funciones que simplemente se invocan, pero debes tener en cuenta que **retornan por defecto `undefined`.**

```js
// Declaración
function saludar(nombre){
  console.log("Hola " + nombre) 
}
// Invocaciones
saludar("JavaScript") //"Hola JavaScript"
saludar("Platzi") // "Hola Platzi"
```

## Aprende sobre la diferencia entre funciones y métodos

Las funciones y los métodos son bloques de código que se pueden reutilizar en diferentes partes de un programa. La diferencia entre ambos radica en su **contexto de ejecución**.

Si quieres saber más sobre este tema, continúa con la clase de **[Funciones vs Métodos](https://platzi.com/home/clases/10266-javascript/70369-funciones-vs-metodos/)**.

***Contribución creada por:** Andrés Guano (Associate).*
