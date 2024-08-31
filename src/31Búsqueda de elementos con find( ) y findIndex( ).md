Los métodos `find` y `findIndex` permiten realizar búsquedas en un *array* y retornar el **primer elemento** que cumpla con la condición especificada.


## Qué es el método `find` y `findIndex`

El método `find` consiste en retornar un elemento, **si cumple con una condición**, caso contrario retornará `undefined`. El método `findIndex` retornará el índice del elemento encontrado, caso contrario retornará `-1`. 

Estos métodos reciben **dos argumentos**: 
* La función que itera y evalúa cada elemento del *array* hasta encuentre uno que cumpla con la condición especificada (obligatorio).
* Un objeto al que puede hacer referencia el contexto `this` en la función. Si se lo omite, será `undefined`. Recuerde que `this` en *arrow functions* es el objeto global.

```js
array.find(function(), thisArg);
array.findIndex(function(), thisArg)
```

### Parámetros de la función como argumento en `find` y `findIndex`

La función, que recibe como argumento los métodos `find` y `findIndex`, utiliza **tres parámetros**:
* El **valor actual del elemento iterado**. Es decir, si es la primera iteración, será el primer elemento, y así sucesivamente.
* El **índice del elemento iterado**. Es decir, si es la primera iteración, será el índice `0`, y así sucesivamente.
* El **array que está iterando**.

```js
array.find(function(element, index, array));
array.findIndex(function(element, index, array))
```

### Cómo buscar elementos en un *array*

Con los métodos `find` y `findIndex`, se debe establecer la función que indique la condición a cumplir para buscar un **elemento en específico**.

```js
const numbers = [1, 30, 41, 29, 50, 60]

const elemento = numbers.find(item => item >= 40)
const index = numbers.findIndex(item => item >= 40)

console.log(elemento) // 41
console.log(index) // 2
```

El primer elemento que cumple con la condición es `41`, que se encuentra en el índice `2` del array `numbers`.

Recuerda que si los métodos `find` y `findIndex` si no encuentran el elemento que cumpla con la condición, devolverán `undefined` y `-1`, respectivamente.

```js
const numbers = ["a", "b", "c"]

const elemento = numbers.find(item => item >= 40)
const indice = numbers.findIndex(item => item >= 40)

console.log(elemento) // undefined
console.log(indice) // -1
```

## Aprende a crear copias con `slice`

El método `slice` permite **crear una copia** de un *array* a partir de un rango de índices especificado. Este método es **inmutable**.

Si quieres saber más sobre este tema, continúa con la clase de **[Crear copias con slice](https://platzi.com/clases/10266-javascript/70356-crear-copias-con-slice/)**.

***Contribución creada por:** Andrés Guano (Associate).*
