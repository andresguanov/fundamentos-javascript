Los métodos `map` y `forEach` permiten **iterar** los elementos de un array y ejecutar una función para cada uno. 

## Qué es el método `forEach`

El método `forEach` de los *arrays* consiste **en ejecutar una función (*callback*) para cada uno de los elementos iterados**. Este método no retorna ningún valor.

Este método recibe **dos argumentos**:

* La **función que itera** cada elemento del *array* (obligatorio).
* Un objeto como **referencia del contexto** `this` en la función. Si se lo omite, será `undefined`. Recuerde que `this` en *arrow functions* es el objeto global.

```js
array.forEach(function(), thisArg)
```

### Parámetros de la función como argumento en `forEach`

La función, que recibe como argumento el método `forEach`, utiliza tres parámetros opcionales:

* El **valor actual del elemento iterado**. Es decir, si es la primera iteración, será el primer elemento, y así sucesivamente.
* El **índice del elemento iterado**. Es decir, si es la primera iteración, será el índice 0, y así sucesivamente.
* El **array que está iterando**.

```js
array.forEach(function(element, index, array))
```

Estos parámetros son opcionales, pero es recomendable utilizarlos para tener un **mejor control de los elementos** que se están iterando. También puedes definir sus nombres como desees.


### Cómo utilizar el método `forEach`

El método `forEach` es útil para recorrer un *array* y ejecutar una función para cada uno de sus elementos. Se puede utilizar con **cualquier tipo de función**.

Puedes utilizar una función anónima o una función *arrow* como argumento del método `forEach`.

```js
const array = [1,2,3,4,5]

// Función anónima
array.forEach(function(element, index, array){
    console.log(`En el índice ${index} está el elemento ${element}`)
})
// Arrow function
array.forEach((element, index, array) => {
    console.log(`En el índice ${index} está el elemento ${element}`)
})
```

O puedes definir una función por separado y pasarla como argumento del método `forEach`. Ten en cuenta que la función debe recibir los mismos parámetros definidos.

```js
function logElements(element, index, array){
    console.log(`En el índice ${index} está el elemento ${element}`)
}

array.forEach(logElements)
```


## Diferencia entre la estructura `for` y el método `forEach`

Los métodos de *arrays* nos permiten realizar algoritmos con una **menor cantidad de líneas de código** que una estructura `for`, con un resultado igual o parecido.

```js
const letras = ['a','b','c']

// Utilizando la estructura repetitiva for
for(let index = 0; index < letras.length; index++){
    const element = letras[index]
    console.log('for', element)
}

// Utilizando el método forEach
letters.forEach(item => console.log('forEach',item))
```


## Qué es el método `map`

El método `map` **es inmutable** y consiste en crear un nuevo *array* a partir de los elementos originales **transformados mediante una función *(callback)***.

Este método recibe **dos argumentos**: 
* La función que itera y transforma cada elemento del *array* (obligatorio).
* Un objeto como **referencia del contexto** `this` en la función. Si se lo omite, será `undefined`. Recuerde que `this` en *arrow functions* es el objeto global.


```js
let otherArray = array.map(function(), thisArg)
```

### Parámetros de la función como argumento en `map`

La función, que recibe como argumento el método `map`, utiliza **tres parámetros opcionales**:
* El **valor actual del elemento iterado**. Es decir, si es la primera iteración, será el primer elemento, y así sucesivamente.
* El **índice del elemento iterado**. Es decir, si es la primera iteración, será el índice `0`, y así sucesivamente.
* El ***array* que está iterando**.

```js
const otherArray = array.map( function(element, index, array) )
```

Estos parámetros son opcionales, pero es recomendable utilizarlos para tener un **mejor control de los elementos** que se están iterando. También puedes definir sus nombres como desees.

Esta función siempre debe retornar un valor, ya que este valor será el nuevo elemento del *array* que se está creando.


### Cómo utilizar el método `map`

El método `map` es útil para **transformar** los elementos de un *array* y crear un nuevo *array* con los elementos transformados.

Crearemos una función que altere cada elemento del array original y retorne ese valor por cada iteración. Recuerda siempre retornar un valor en la función `callback` del método, caso contrario cada elemento del nuevo *array* será `undefined`.

```js
function double(number){
    // Bloque de código extra que necesites
    return number * 2
}
```

Entonces, cada elemento del *array* original será transformado por esta función. También puedes utilizar cualquier tipo de función.

```js
const numbers = [1,2,3,4,5]

const newNumbers = numbers.map( function (number){
    return number * 2
})

// Utilizando Arrow functions con retorno implícito
const newNumbers = numbers.map(number => number * 2)

console.log(newNumbers) // [ 2, 4, 6, 8, 10 ]
```

Si observas, el método `map` **retorna un nuevo *array*** con los elementos transformados. Es decir, no altera el original, por lo tanto es **inmutable**.

```js
console.log(numbers) // [ 1, 2, 3, 4, 5 ]
```

## Aprende sobre los métodos de `filter` y `reduce`

Los métodos `filter` y `reduce` permiten realizar operaciones más complejas con los elementos de un *array*.

Si quieres saber más sobre este tema, continúa con la clase de **[¿Por qué aprender desarrollo web?](https://platzi.com/home/clases/10266-javascript/70354-filtrado-y-reduccion-con-filter-y-reduce/)**.

***Contribución creada por:** Andrés Guano (Associate).*
