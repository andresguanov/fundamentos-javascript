El tipo de dato `string` es una **cadena de caracteres** que se utiliza para almacenar texto. Este tipo de dato se puede declarar utilizando comillas simples `'` o dobles `"`. 

## Cómo declarar strings
Para declarar un string, puedes utilizar comillas simples `'` o dobles `"`.

```js
let nombre = 'Andres'
let apellido = "Comillas dobles"
```

Aunque el resultado sea el mismo, es importante ser **consistente en el uso de comillas** para tu equipo de trabajo.

### Diferencia entre comillas simples y dobles

Aunque parecen lo mismo, hay una diferencia entre las comillas simples y dobles. Si necesitas utilizar una comilla simple dentro de un *string*, debes declarar el *string* con comillas dobles y viceversa.

```js
let mensaje = "Andres dijo 'JavaScript es increíble'" // ✅
let mensaje2 = 'Andres dijo "JavaScript es increíble"' // ✅

let mensaje3 = "Andres dijo "JavaScript es increíble"" // Error
```

También si necesitas utilizar comillas dobles y simples dentro de un *string*, puedes utilizar el caracter de escape `\`.

```js
let mensaje3 = 'Andres dijo "JavaScript es increíble" y \'HTML también\'' // ✅
```

### Qué es el operador de concatenación
El operador de concatenación consiste en **unir dos o más *strings***.

```js
let mensaje = "Hola" + "Platzi"

console.log(mensaje)// "HolaPlatzi"
```

Ten en cuenta que el **espacio también es un caracter**, por lo que debes agregarlo si lo necesitas.

El operador de concatenación es **similar al operador de suma**, pero no es el mismo. Si utilizas este operador con diferentes tipos de datos, JavaScript realizará una [coerción implícita](https://platzi.com/clases/10266-javascript/70367-conversion-de-tipos-type-casting-y-coercion/).


## Qué son los *template literals*

Los *template literals* o plantillas literales son una forma de crear *strings* más legibles y mantenibles. En los que se pueden incluir **variables y expresiones**.

### Qué problema resuelven los *template literals*

Sin *template literals*, si necesitas crear una cadena larga o un mensaje, debes utilizar la concatenación. 

```js
let nombre = "Andres"
let edad = 23
let mensaje = "Mi nombre es " + nombre + " y tengo " + edad + " años."

console.log(mensaje)
// 'Mi nombre es Andres y tengo 23 años.'
```

Esto trae varios problemas en la **legibilidad y mantenibilidad del código**. Se convierte cada vez más complejo en mensajes más extensos o el estar pendiente de agregar espacios antes o después de cada variable concatenada.

### Cómo se utilizan los *template literals*

Con los *template literals*, empleas el caracter ( \` ), que no es una comilla simple ( ' ), para envolver el mensaje e incluir las variables con la sintaxis `${variable}`.

```js
var nombre = "Andres"
var edad = 23

var mensaje = `Mi nombre es ${nombre} y tengo ${edad} años.`

console.log(mensaje)
// 'Mi nombre es Andres y tengo 23 años.'
```

De esta forma, el código es más **legible y mantenible**. Además, puedes incluir **expresiones** dentro de los *template literals*, también puedes incluir saltos de línea.

```js
var mensaje = `Mi nombre es ${nombre} y tengo ${edad} años.
Además, el próximo año tendré ${edad + 1} años.`

console.log(mensaje) // Observa el resultado
```

## Cómo obtener los caracteres de un *string*

Los *strings* son **inmutables**, lo que significa que **no lo puedes modificar directamente**. Están **ordenados por índices**, donde el primer caracter tiene el índice 0.

El índice es la posición de un caracter en un *string*. Y se puede acceder a un caracter mediante la notación de corchetes `[]`.

```js
let mensaje = "Hola Platzi"
console.log(mensaje[0]) // 'H'
console.log(mensaje[1]) // 'o'
console.log(mensaje[4]) // ' '
console.log(mensaje[5]) // 'P'
```

Pero no se puede modificar un caracter directamente.

```js
mensaje[0] = 'h' // Error ❌
```

## Cómo manipular *strings*

También puedes hacer **operaciones** con *strings*, como **obtener la longitud**, **convertir a minúsculas o mayúsculas** y **obtener una subcadena**. Esto se logra con los **métodos** de los *strings*.

Rápidamente, los atributos y métodos son valores o modificaciones que se aplican a un *string* mediante la notación de punto (`.`). Pero diferencialos rápidamente en que los atributos son valores y los métodos son funciones que necesitan paréntesis `()` para ejecutarse.

Los conceptos de atributos y métodos serán explicados con más detalle en la [sección sobre objetos](https://platzi.com/clases/10266-javascript/70358-anatomia-de-un-objeto/), que abordaremos más adelante en el curso.

### Cómo obtener la longitud de un *string*

La longitud es la cantidad de caracteres que tiene un *string*. Para obtener este valor de un *string*, puedes utilizar el atributo `length`.

```js
let mensaje = "Hola Platzi"
let longitud = mensaje.length

console.log(longitud) // 10
```

### Cómo convertir un *string* a minúsculas o mayúsculas

Para convertir un *string* a minúsculas o mayúsculas, puedes utilizar los métodos `toLowerCase` y `toUpperCase`.

```js
let mensaje = "Hola Platzi"
let mensajeMinusculas = mensaje.toLowerCase()
let mensajeMayusculas = mensaje.toUpperCase()

console.log(mensajeMinusculas) // 'hola platzi'
console.log(mensajeMayusculas) // 'HOLA PLATZI'
```

### Cómo obtener una subcadena de un *string*

Para obtener una subcadena de un *string*, puedes utilizar el método `substring` con dos parámetros: el índice de inicio y el índice de fin.

```js
let mensaje = "Hola Platzi"
let subcadena1 = mensaje.substring(0, 4)
let subcadena2 = mensaje.substring(5, 11)

console.log(subcadena1) // 'Hola'
console.log(subcadena2) // 'Platzi'
```

## Aprende sobre los operadores aritméticos en JavaScript

Los operadores aritméticos sirven para realizar operaciones matemáticas desde las más básicas como la suma y resta, hasta las más complejas como la exponenciación.

Si quieres saber más sobre este tema, continúa con la clase de **[Operadores aritméticos](https://platzi.com/home/clases/10266-javascript/70338-operadores-aritmeticos/)**.

***Contribución creada por:** Andrés Guano (Associate).*
