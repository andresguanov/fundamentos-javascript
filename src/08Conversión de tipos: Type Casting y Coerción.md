La conversión de tipos consiste en transformar de un tipo de dato a otro de una variable. Existen dos tipos de conversión de tipos: **type casting** y **coerción**.

## Qué son los lenguajes compilados e interpretados

Los lenguajes de programación se pueden clasificar en dos tipos: **compilados** e **interpretados**.

### Qué son los lenguajes compilados
Los lenguajes compilados son aquellos que **necesitan de un compilador** para transformar el código fuente en código máquina. Este código máquina es el que se ejecuta en la computadora.

Algunos ejemplos de lenguajes compilados son C, C++, Rust, Swift y Go.

En este tipo de lenguajes, **el chequeo de tipos es estático**, lo que significa que el compilador verifica que los tipos de datos sean correctos antes de ejecutar el programa.

### Qué son los lenguajes interpretados
Los lenguajes interpretados son aquellos que no necesitan de un compilador para transformar el código fuente en código máquina. En su lugar, utilizan un **intérprete que lee el código fuente y lo ejecuta**.

Algunos ejemplos de lenguajes interpretados son JavaScript, Python, Ruby y PHP.

En este tipo de lenguajes, **el chequeo de tipos es dinámico**, lo que significa que el intérprete verifica los tipos de datos cuando se ejecuta el programa.

## Qué es JavaScript

JavaScript es un lenguaje de programación interpretado. Es un lenguaje de **tipado débil y dinámico**, lo que significa que **no es necesario declarar el tipo de dato de una variable** y que **los tipos de datos pueden cambiar en tiempo de ejecución**.

Esto es importante porque en JavaScript, al ser un lenguaje débil y dinámicamente tipado, **es necesario tener cuidado con la conversión de tipos**. Ya que el compilador tratará de interpretar el código de la mejor manera posible, pero puede arrojar **resultados inesperados**.

## Cómo funciona la conversión de tipos en JavaScript

**La conversión de tipos consiste en transformar de un tipo de dato a otro de una variable.** Existen dos tipos de conversión de tipos: 

* Conversión implícita o *type coercion*
* Conversión explícita o *type casting* 

## Qué es la conversión implícita o *type coercion*

La conversión implícita consiste en la transformación de tipos mediante la **ayuda de JavaScript.** Esto ocurre en operaciones de diferentes tipos, ya que es un lenguaje débil y dinámicamente tipado.

Al momento de ejecutar el código, si el motor de JavaScript encuentra alguna incoherencia (una suma de un número con un *string*), **el motor lo interpreta a su manera y arroja un valor que puede ser erróneo**. 

Algunos de los ejemplos de coerción implícita son los siguientes:

```js
4 + "7"   // 47
4 * "7"   // 28
2 + true  // 3
false - 3 // -3
```

Ten en cuenta que **la coerción implícita puede ser peligrosa**, ya que puede arrojar resultados inesperados. Por eso es importante tener cuidado con la conversión de tipos en JavaScript.

## Qué es la conversión explícita o *type casting*

La conversión explícita es la transformación de tipos de datos sobre la que **controlamos el resultado.** Para realizar estas transformaciones se utiliza las funciones `Number()`, `String()` y `Boolean()`, para convertir a tipo número, *string* y booleano, respectivamente.

```js
Number("47") // 47
String(51)   // "51"
Boolean(1)   // true
```

Puedes utilizar la palabra reservada `typeof` para comprobar el tipo de dato transformado.

```js
typeof Number("47") // 'number'
typeof String(51)   // 'string'
typeof Boolean(1)   // 'boolean'
```

Ten en cuenta que **la conversión explícita es más segura que la conversión implícita**, ya que controlamos el resultado de la transformación. También que debe existir lógica en conversión, si deseas convertir `"Hola"` a número, no será posible.


## Aprende sobre los operadores de comparación en JavaScript

Los operadores de comparación en JavaScript son importantes para realizar comparaciones entre valores y variables.

Si quieres saber más sobre este tema, continúa con la clase de **[Operadores de comparación](https://platzi.com/clases/10266-javascript/70339-operadores-de-comparacion/)**.

***Contribución creada por:** Andrés Guano (Associate).*
