Una variable es la representación de un lugar en memoria que reservamos para **guardar un valor en específico**. El valor puede ser cualquier **tipo de dato**, como un número, un texto, entre otros. Ten en cuenta el concepto de **tipo de dato** porque es fundamental en la programación.

## Cómo declarar y asignar variables
En JavaScript, una variable se crea con la palabra reservada `var`, seguido del nombre de la variable. Esto se denomina **declaración**.

```js
var nombre
```

De esta manera, existirá un espacio en memoria que haga referencia a la variable `nombre`. Por defecto, una variable tendrá un valor `undefined`. Así es como JavaScript maneja las variables que no tienen un valor asignado.

Para guardar un valor en esa variable, se utiliza el símbolo de igual (`=`) , seguido del valor. Esto se denomina **asignación**.

```js
var nombre
nombre = 'JavaScript'
```

Se puede declarar y asignar una variable en una misma línea, sin repetir el nombre de la variable. A esto se le dice **inicializar una variable**.

```js
var nombre = 'JavaScript'
```

## Valores por consola
Para mostrar valores por consola o terminal, se utiliza la función `console.log()` para **imprimir el valor de una variable**. Tranquilo con el concepto de función, ya aprenderás lo que es.

Ejecuta lo siguiente en la terminal con el comando `node`. Así como se explicó en la clase de instalación de [Mac](https://platzi.com/clases/10266-javascript/70442-hola-mundo-en-mac/) y [Windows](https://platzi.com/clases/10266-javascript/70443-hola-mundo-en-winows/). Observa lo que sucede.

```js
console.log("Hola Mundo")
```

## Cómo acceder a una variable
Una vez que hayas declarado y asignado un valor a una variable. Ya puedes utilizar en tu código utilizando su nombre, sin la necesidad de utilizar nuevamente `var`.

```js
var nombre = 'JavaScript'

console.log(nombre) //'JavaScript'
```

Si ejecutas el código anterior, verás que en la terminal se imprime el valor de la variable `nombre`, que es igual a `'JavaScript'`.

## Comentarios en JavaScript

Los comentarios son **descripciones que escribimos, pero que JavaScript ignorará**. Se escriben de dos maneras: 
* En una sola línea con `//`
* En múltiples líneas utilizando `/*  */`.

Por ejemplo, observa los siguientes comentarios:

```js
// Este es un comentario de una línea
/*
Este es un comentarios
con múltiples líneas
*/
```

## *Let* y *const*, la nueva forma para declarar variables

Existen dos formas de declarar variables adicionales en JavaScript: `let` y `const`.

### Cómo declarar variables con `let`

La palabra reservada `let` se utiliza para declarar variables que pueden ser re-asignadas, es decir, que pueden cambiar su valor en el futuro.

```js
let contador = 1
contador = contador + 1
console.log(contador) // 2
```

### Cómo declarar variables con `const`

La palabra reservada `const` se utiliza para declarar variables que **no pueden ser re-asignadas**, es decir, que su valor no puede cambiar en el futuro.

```js
const pi = 3.1416
```

### Qué es re-declarar y re-asignar una variable

**La re-declaración es volver a declarar una variable, y la re-asignación es volver a asignar un valor**. Entonces, expliquemos qué sucede con `var`, `let` y `const`.  

* Una variable declarada con `var` puede ser re-declarada y re-asignada
* Una variable declarada con `let` puede ser re-asignada, pero no re-declarada
* Una variable declarada con `const` no puede ser re-declarada, ni re-asignada. Su declaración y asignación debe ser en una línea, caso contrario habrá un error

En conclusión, si intentas re-declarar una variable declarada con `let` y `const` habrá un error de "variable ya declarada" (`SintaxError`). Si intentas re-asignar una variable declarada con `const` existirá un error de tipo (`TypeError`). En los demás casos, JavaScript lo aceptará como válidos, algo problemático con `var`, por eso se recomienda no utilizarlo.

A continuación se muestran ejemplos de re-declaración y re-asignación de variables.

```js
// Declarar y asignar con const en diferentes líneas
const pi  // SyntaxError: Missing initializer in const declaration.
pi = 3.14
```

```js
// Declaración de variables
var nameVar = 'soy var'
let nameLet = 'soy let'
const nameConst = 'soy const'
```

```js
// Re-declaración de variables
var nameVar = 'me re-declaré var' 
console.log(nameVar) // 'me re-declaré'

let nameLet = 'me re-declaré let' // SyntaxError: Identifier 'nameLet' has already been declared.

const nameConst = 'me re-declaré const' //SyntaxError: Identifier 'nameConst' has already been declared.
```

```js
// Re-asignación de variables
nameVar = 'otro var'
console.log(nameVar) // 'otro var'

nameLet = 'otro let'
console.log(nameVar) // otro let'

nameConst = 'otro const' //TypeError: Assignment to constant variable.
```

Ten en cuenta que los errores pararán la ejecución de tu programa. Es decir, si hay un error en tu código, el programa se detendrá y **no se ejecutará el resto del código**.

## Buenas prácticas con variables

A continuación, se presentan algunas buenas prácticas para declarar variables en JavaScript.

### Cómo utilizar `var`, `let` y `const`

Hasta ahora aprendiste brevemente a declarar variables con `var`,`let` y `const`. Sin embargo, en la **actualidad se recomienda** utilizar `let` y `const` para declarar variables. 

Las palabras reservadas `let` y `const` resuelven varios problemas de `var`, como la re-declaración y re-asignación de variables, el *hoisting*, y variables globales. 

Así que ten en cuenta que `let` y `const` son la **nueva forma de declarar** variables en JavaScript. Y `var` es la forma antigua. Los siguientes ejemplos únicamente se escribirán con `let` y `const`.


### Cómo nombrar variables

Al momento de escribir código, es importante seguir ciertas buenas prácticas para que el código sea más **legible y mantenible**. Esto ayuda a que otras personas puedan **entender tu código** y a que tú mismo puedas entenderlo en el futuro.

Algunas recomendaciones para nombrar variables son:

* **Utilizar nombres descriptivos**: el nombre de la variable debe indicar qué tipo de información almacena.
* **Evitar números al inicio y caracteres especiales**: no es recomendable utilizar números al inicio o caracteres especiales en el nombre de las variables.
* **Si el nombre de la variable es compuesto, se debe utilizar notación camelCase**: la primera palabra en minúscula y las siguientes palabras iniciarán en mayúscula.
* **Puedes utilizar abreviaciones si son comunes**: por ejemplo, `id` para identificador, `msg` para mensaje, `btn` para botón, entre otros.

```js
// ❌ No recomendado 
let n = 'Andres' 
let ndu = 'Andres'
let 123usuario = 'Andres'
let no@usu = 'Andres'
let nombredeusuarioprincipal = 'Andres'

// ✅ Recomendado 
let nombre = 'Andres'
let nombreDeUsuario = 'Andres'
let usuario123 = 'Andres'
let nombreUsuarioPrincipal = 'Andres'
let idUsuario = 1233455
```

## Aprende sobre tipos de datos en JavaScript
Ahora que conoces cómo declarar y asignar variables en JavaScript, es importante que aprendas sobre los **tipos de datos** que puedes almacenar en una variable.

Si quieres saber más sobre este tema, continúa con la clase de **[Tipos de datos en JavaScript](https://platzi.com/home/clases/10266-javascript/70444-tipos-de-datos-en-javascript/)**.

***Contribución creada por:** Andrés Guano (Associate).*
