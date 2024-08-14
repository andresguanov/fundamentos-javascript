Los tipos de datos en JavaScript son **la característica propia que tiene un valor**. En JavaScript existen los tipos de datos primitivos y los no primitivos o complejos.

## Qué son los tipos de datos primitivos
Los tipos de datos primitivos son los más básicos y simples que se pueden utilizar en JavaScript. Estos tipos de datos son **inmutables**, es decir, que no se pueden modificar. Estos son los siguientes: 

* **number**: indica un valor **numérico**, ya sea entero o flotante, flotante significa que tiene decimales
* **string**: indica una **cadena de caracteres**, el valor está envuelto en comillas dobles `"` o simples `'`
* **boolean** indica un valor **lógico binario**, es decir, los valores verdadero o `true` y falso o `false`
* **null**: indica un valor **nulo**, es decir un valor vacío
* **undefined**: indica un valor **no definido**, es decir, que no tiene valor asignado

Existen dos tipos primitivos más: `bigint` y `symbol`, pero es un tema que aprenderás más adelante.

## Qué son los tipos no primitivos o complejos
Los datos de tipo no primitivos o complejos son aquellos que **no almacenan directamente el valor**, sino que almacenan una referencia a la ubicación en la memoria donde se encuentra el valor. Estos son los siguientes:

* **function**: indica una representación de función, almacena un bloque de código que se puede ejecutar
* **object**: indica una representación de objetos, arreglos, entre otros.

En otras palabras, todo aquello que no sea un primitivo o una función, es un objeto.

## Cómo utilizar la palabra reservada `typeof`
La palabra reservada `typeof` permite **identificar el tipo de dato** de un valor en JavaScript. Este operador devuelve una cadena de texto o *string*.

Existe una excepción, al ejecutar `typeof null`, en la terminal mostrará `'object'`, esto es un error en JavaScript que **no se ha corregido por temas de compatibilidad**. Tenlo en cuenta.

Ingresa a la terminal y ejecuta cada línea del siguiente ejemplo y observa cuál es la respuesta.

```js
// Tipos de datos primitivos
typeof 5          // 'number'
typeof "hola"     // 'string'
typeof 'hola'     // 'string'
typeof true       // 'boolean'
typeof null       // 'object'
typeof undefined  // 'undefined'

// Tipos de datos complejos
typeof console.log      // 'function'
typeof {tipo: "objeto"} // 'object'
typeof [1,2,3,4]        // 'object'
typeof new Date()       // 'object'
```

### Ten precaución con el tipo de dato string
El tipo de dato `string` es una cadena de caracteres que se utiliza para almacenar texto. Este tipo de dato se puede declarar utilizando comillas simples `'` o dobles `"`. Por lo tanto no confundas el tipo de dato `string` con otros tipos de dato.

```js
typeof 'hola'       // 'string'
typeof '123'        // 'string'
typeof 'true'       // 'string'
typeof 'null'       // 'string'
typeof 'undefined'  // 'string'
typeof '[1,2,3]'    // 'string'
```

En definitiva, no confundas el tipo de dato `string` con otros tipos de datos, **recuerda que es una cadena de caracteres**. Esto en especial es importante cuando trabajas con datos que provienen de una API o de una base de datos.


## Qué es el tipo de dato Big Int
El nuevo dato primitivo `bigint` permite **manejar números enteros muy grandes**.

Existen dos formas de crear un `bigint`: 
* el número entero seguido de `n`
* mediante la función `BigInt`

```js
const number1 = 45n
const number2 = BigInt(45)

typeof 45n // 'bigint'
typeof number1 // 'bigint'
```

### Qué problema resuelve el tipo de dato Big Int

**JavaScript tiene límites numéricos**, un máximo `Number.MAX_SAFE_INTEGER` y un mínimo `Number.MIN_SAFE_INTEGER`. Puedes ver estos límites ejecutando el siguiente código:

```js
const max = Number.MAX_SAFE_INTEGER
const min = Number.MIN_SAFE_INTEGER

console.log(max)  // 9007199254740991
console.log(min) // -9007199254740991
```

Después de estos límites máximo y mínimo, **los cálculos muestran resultados erróneos**. Los `bigint` ayudan a manejar operaciones de enteros fuera de los límites mencionados.

```js
const increment = 2
const number = Number.MAX_SAFE_INTEGER + increment
const bigInt = BigInt(Number.MAX_SAFE_INTEGER) + BigInt(increment)

console.log(number) // 9007199254740992
console.log(bigInt) // 9007199254740993n
```

Como puedes observar en el código anterior, se añade la misma cantidad a ambos tipos de datos, sin embargo, el tipo numérico da un **resultado diferente al esperado**.

## Qué es tipo de dato Symbol
El tipo de dato `symbol` es un **valor único e inmutable** que se utiliza como clave de una propiedad de un objeto.

```js
const symbol = Symbol('Andres')
const symbol2 = Symbol('Andres')
typeof symbol // 'symbol'
typeof symbol2 // 'symbol'

console.log(symbol === symbol2) // false
```

En el código anterior, `symbol` y `symbol2` son dos valores diferentes, aunque tengan el mismo nombre.

## Aprende sobre el tipo de dato String

El tipo de dato `string` es una **cadena de caracteres** que se utiliza para almacenar texto. Este tipo de dato se puede declarar utilizando comillas simples `'` o dobles `"`.

Si quieres saber más sobre este tema, continúa con la clase de **[tipo de dato String](https://platzi.com/home/clases/10266-javascript/70445-creacion-de-strings/)**.

***Contribución creada por:** Andrés Guano (Associate).*
