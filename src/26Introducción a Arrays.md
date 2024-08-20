
Los *arrays* son estructuras de datos que nos permiten **almacenar varios elementos** localizados por índices y separados por comas en una sola variable. Estos elementos pueden ser de cualquier tipo, como números, cadenas de texto, objetos, funciones, entre otros.

## Qué son los índices

Los índices son números enteros que se utilizan para acceder a los elementos de un *array*. Estos números comienzan desde `0` y se incrementan en `1` por cada elemento que contiene un *array*.

Un *array* se inicia mediante la sintaxis de corchetes `[]`, sus elementos están separados por comas y su tipo de dato es `'object'`.

```js
let array1 = [] // Array vacío
let array2 = [1,2,3,4] // Array con elementos
let array3 = [1] // Array con un solo elemento
let array4 = [1, "Platzi", true, {name: "Andres"}]
```

## Qué es el atributo `length`

El atributo `length` es una característica de los *arrays* que nos permite conocer la **cantidad de elementos** que contiene un *array*. Este atributo es de tipo `number` y se puede acceder a él mediante la siguiente sintaxis:

```js
array.length
```

Por ejemplo, si se tiene un *array* con 4 elementos, el atributo `length` devolverá `4`.

```js
let array = [1,2,3,4]

console.log(array.length) // 4
```

## Cómo acceder a los elementos de un *array*

Para acceder a los elementos de un *array* se utiliza la sintaxis de corchetes `[]` seguido del índice del elemento que se desea obtener.

```js
array[índice]
```

Entonces, para acceder a un elemento del *array*, únicamente podrás utilizar los índices desde el `0` hasta `array.length - 1`, teóricamente. Si se accede a un índice que no existe, devolverá `undefined`.

```js
let nombres = ["Andres", "Ramiro", "Silvia"]

nombres[0] // "Andres"
nombres[1] // "Ramiro"
nombres[2] // "Silvia"
nombres[3] // undefined
```


## Cómo crear un *array* con la función `Array`

La función `Array` nos permite crear un *array* con la cantidad de elementos que se desee. 


### Crear un *array* con elementos específicos con `Array`

Para crear un *array* con **elementos específicos**, se debe pasar como argumento los elementos que se desean almacenar en el *array*.

```js
let array = Array(1,2,3,4)

console.log(array) // [1,2,3,4]
```

### Crear un *array* con una cantidad específica de elementos con `Array`

Para crear un array con una **cantidad específica de elementos**, se debe pasar como argumento un número entero que represente dicha cantidad. Esto creará un array con los elementos especificados, pero sin **valores asignados**.

```js
let array = Array(5)

console.log(array) // [undefined, undefined, undefined, undefined, undefined]
console.log(array.length) // 5
```

Por otro lado, no podrás crear un *array* con un solo elemento, ya que la función `Array` interpretará el argumento como la cantidad de elementos que contendrá el *array*.

### Crear un *array* vacío con `Array`

Para crear un *array* vacío, no se debe pasar ningún argumento a la función `Array`.

```js
let array = Array()

console.log(array) // []
```

## Aprende sobre la mutabilidad e inmutabilidad 

La mutabilidad e inmutabilidad son conceptos importantes en la programación. Definen si un objeto puede ser modificado o no. De hecho, los *arrays* son mutables.

Si quieres saber más sobre este tema, continúa con la clase de **[Mutabilidad e inmutabilidad](https://platzi.com/clases/10266-javascript/70351-mutabilidad-e-inmutabiliad-de-arrays/)**.

***Contribución creada por:** Andrés Guano (Associate).*
