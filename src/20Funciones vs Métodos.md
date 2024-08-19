Las funciones también son consideradas **ciudadanos de primera clase**. Esto significa que las funciones pueden ser almacenadas en variables, pasadas como argumentos a otras funciones y retornadas por otras funciones.

## Qué son las funciones declarativas y expresivas

Las **funciones declarativas** son aquellas que aprendimos en la anterior clase [Anatomía de una función](https://platzi.com/clases/10266-javascript/70368-anatomia-de-una-funcion/). **Consisten en almacenar un bloque de código en memoria**. 

Por otro lado, las **funciones expresivas o anónimas** consisten en **guardar la función en una variable**. Tienen la misma declaración e invocación que las funciones declarativas. 

Cabe mencionar que las funciones expresivas no pueden ser invocadas antes de su declaración y su nombre depende de la variable donde se almacena.

```js
// Declaración
let suma = function (a, b) {
  return a + b
}
// Invocación
suma(2, 2) //4
```

## Qué son los métodos

Los métodos son funciones que se **encuentran dentro de un objeto** almacenado en una propiedad. La manera de declararlas es similar a las funciones expresivas, se **asignan a una propiedad de un objeto**.

```js
const cohete = {
  nombre: 'Falcon 9',
  despegar: function () {
    console.log('3, 2, 1, ¡Despegue!')
  }
}
```

Para invocar un método, se debe hacer referencia al objeto y a la propiedad que contiene la función.

```js
cohete.despegar() // 3, 2, 1, ¡Despegue!
```

### Cuál es la diferencia entre métodos y atributos

Los métodos y atributos son propiedades de un objeto. La diferencia radica en que los **atributos son valores** y los **métodos son funciones**.

En el ejemplo de `cohete`, `nombre` es un atributo y `despegar` es un método. Estos son conceptos básicos de la programación orientada a objetos (POO). Hay una sección específica para este tema.


## Qué son los callbacks

Los **callbacks** son funciones que se pasan como argumentos a otras funciones. Se utilizan para **ejecutar código después de que otra función sea invocada**.

```js
function sumar (a, b, callback) {
  const resultado = a + b
  callback(resultado)
}

function imprimirResultado (resultado) {
  console.log(resultado)
}

sumar(2, 2, imprimirResultado) // 4
```

Los *callbacks* son útiles para extender funcionalidades sin modificar el código original. Por ejemplo, puedo utilizar otra función y utilizar el resultado de la función `sumar`.

```js
function multiplicarPorDos (resultado) {
  console.log(resultado * 2)
}

sumar(2, 2, multiplicarPorDos) // 8
```

Y así sucesivamente, puedo reutilizar funciones y extender la funcionalidad del código. Los *callbacks* son una herramienta poderosa para la programación funcional. Ten esto en cuenta cuando iniciemos con los [métodos de manipulación de *arrays*](https://platzi.com/clases/10266-javascript/70350-introduccion-a-arrays/).


## Qué son las *nested functions*

Las *nested functions* son funciones anidadas dentro de otras funciones. Estas funciones tienen acceso a las variables de la función padre y pueden ser invocadas dentro de la función padre.

```js
function principal () {
  function padre () {
    function hijo () {
      console.log('Hola desde la función c')
    }
    hijo()
  }
  padre()
}
principal() // Hola desde la función c
```

Las *nested functions* son útiles para modularizar el código y mantener la lógica de la función padre separada. Además, las funciones anidadas pueden acceder a las variables de la función padre, pero no al revés. A esto se le conoce como el **contexto de ejecución**.

## Qué es el contexto de ejecución

El **contexto de ejecución** es el alcance de las variables y funciones en un programa. Las funciones tienen acceso a las variables de su función padre, pero no al revés. 

```js
function padre () {
  const x = 1
  function hijo () {
    console.log(x)
  }
  hijo()
}
padre() // 1
```

En este ejemplo, la función `hijo` tiene acceso a la variable `x` de la función `padre`. Sin embargo, si intento acceder a una variable de la función `hijo` desde la función `padre`, obtendré un error.

```js
function padre () {
  function hijo () {
    const x = 1
  }
  console.log(x)
}
padre() // ReferenceError: x is not defined
```

Este tema es más amplio y complejo, y se explicará con más detalle en la clase [Contextos de ejecución](https://platzi.com/clases/10266-javascript/70372-contextos-de-ejecucion-y-scope-chain/), pero estos son los conceptos básicos que necesitas saber para entender cómo funcionan las funciones en JavaScript.

## Qué es el objeto global

El objeto global es aquel que contiene todas las variables y funciones de JavaScript. Dependiendo el entorno donde se ejecute el código, este objeto puede cambiar. 

En el navegador, el objeto global es `window`. En Node.js, el objeto global es `global`. También es `globalThis` sin importar el entorno.

## Qué es `this` en JavaScript

La palabra clave `this` en JavaScript se refiere al **objeto que invoca una función**. El valor de `this` depende del contexto de ejecución en el que se encuentra la función.

En funciones, `this` se refiere al objeto global. 

```js
function a () {
  console.log(this)
}
a() // Window
```

En objetos, `this` se refiere al objeto que contiene la función.

```js
const cohete = {
  nombre: 'Falcon 9',
  despegar: function () {
    console.log(`¡${this.nombre} despegó!`)
  }
}
cohete.despegar() // ¡Falcon 9 despegó!
```

### Cómo cambiar el valor de `this`

El valor de `this` puede ser cambiado utilizando los métodos `call`, `apply` y `bind`. Estos métodos permiten cambiar el contexto de ejecución de una función.

El método `call` permite invocar una función con un objeto específico como contexto de ejecución.

```js
function imprimir () {
  console.log(this)
}
a() // Window

const usuario = { name: 'Andrés' }
imprimir.call(usuario) // { name: 'Andrés' }
```

En este ejemplo, la función `imprimir` imprime `this`, pero este es el objeto global. Al utilizar `call`, cambiamos `this` por el objeto `usuario`.

Recomiendo utilizar estos métodos con precaución, ya que pueden ser **confusos y difíciles de mantener**.

## Qué son las *higher-order functions*

Las *higher-order functions* son funciones que:
* reciben otras funciones como argumentos
* retornan una función

Estas funciones son una parte fundamental de la programación funcional.

Como ya sabes que las funciones son ciudadanos de primera clase, puedes pasarlas como argumentos a otras funciones. Esto también es llamado *callback*. Por otro lado, puedes retornar una función desde otra función.

```js
function a () {
  function b () {
    console.log('Hola desde la función b')
  }
  return b
}
```

### Cómo invocar una *high order function*

Para invocar una *high order function*, puedes hacerla de dos maneras:

* Almacenar la función en una variable y luego invocarla con el nombre de esa variable.

```js
const resultadoB = a()
resultadoB() // Hola desde la función b
```

* Invocar la función directamente.

```js
a()() // Hola desde la función b
```

Si la invocas una vez (`a()`) obtendrás la función `b`. Si la invocas dos veces (`a()()`) obtendrás el resultado de la función `b`.

## Aprende sobre las funciones puras e impuras

Las funciones puras son aquellas que **no modifican el estado de las variables** y **no tienen efectos secundarios**.

Si quieres saber más sobre este tema, continúa con la clase de **[Funciones puras e impuras](https://platzi.com/clases/10266-javascript/70370-funciones-puras-e-impuras/)**.

***Contribución creada por:** Andrés Guano (Associate).*
