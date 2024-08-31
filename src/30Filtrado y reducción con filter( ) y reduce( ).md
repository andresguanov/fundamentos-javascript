Los métodos `filter` y `reduce` permiten realizar operaciones más complejas con los elementos de un *array*. Estos métodos son inmutables, es decir, no modifican el *array* original, sino que crean uno nuevo con los elementos que cumplan con la condición especificada.

## Qué es el método `filter`

El método `filter` **es inmutable** y consiste en crear un nuevo *array* a partir de los elementos originales **filtrados mediante una función *(callback)*** que indica una **condición a cumplir**. Si la condición se cumple, retorna el elemento completo.

Este método recibe **dos argumentos**: 
* La función que itera y evalúa si cada elemento del *array* cumple con la condición especificada (obligatorio).
* Un objeto como **referencia del contexto** `this` en la función. Si se lo omite, será `undefined`. Recuerde que `this` en *arrow functions* es el objeto global.

```js
let otherArray = array.filter(function(), thisArg)
```

### Parámetros de la función como argumento en `filter`

La función, que recibe como argumento el método `filter`, utiliza **tres parámetros opcionales**:
* El **valor actual del elemento iterado**. Es decir, si es la primera iteración, será el primer elemento, y así sucesivamente.
* El **índice del elemento iterado**. Es decir, si es la primera iteración, será el índice `0`, y así sucesivamente.
* El ***array* que está iterando**.

```js
const other = array.filter(function(element, index, array))
```

### Cómo filtrar elementos de un *array*

Con el método `filter`, solo debemos establecer la función que indique una condición a cumplir para cada elemento, si cumple con la condición, entonces será incluido en el nuevo *array*.

Por ejemplo, creemos un *array* con palabras y filtremos aquellas que tengan más de 6 letras.

```js
const words = ["spray", "elites", "limit", "apple", "exuberant"]

const newWords = words.filter( function(word){
    if (word.length >=6){
      return true
    }else{
      return false
    }
})

// Utilizando Arrow Function con retorno implícito
const newWords = words.filter(word => word.length >= 6)

console.log(newWords) // [ 'elites', 'exuberant' ]
console.log(words) // [ 'spray', 'elites', 'limit', 'apple', 'exuberant' ]
```

Recuerda siempre retornar un **valor lógico** en la función `callback` del método.

### Cómo filtrar elementos a partir de la propiedad de un objeto

Con el método `filter` puedes filtrar los objetos de un *array* a partir de una condición referente a la **propiedad de cada elemento**. Teniendo en cuenta que el nuevo *array* contendrá el **objeto completo** que haya cumplido con la condición especificada.

Especifiquemos un objeto `orders` que contiene los pedidos de los clientes.

```js
const orders = [
  {
    customerName: "Nicolas",
    total: 60,
    delivered: true,
  },
  {
    customerName: "Zulema",
    total: 120,
    delivered: false,
  },
  {
    customerName: "Santiago",
    total: 180,
    delivered: true,
  },
  {
    customerName: "Valentina",
    total: 240,
    delivered: true,
  },
]
```

Ahora, filtremos los elementos del *array* `orders` cuyo total sea mayor a `150`.

```js
const newOrders = orders.filter(order => order.total > 150)

console.log(newOrders) 
/* [
  {
    customerName: 'Santiago',
    total: 180,
    delivered: true
  },
  {
    customerName: 'Valentina',
    total: 240,
    delivered: true
  }
]
*/

```


## Qué es el método `reduce

El método `reduce` **es inmutable** y consiste retornar **un solo valor** del *array* iterado a partir de una función *(callback)* que indica de qué manera se itera cada elemento para reducirlo.

Este método recibe **dos argumentos**: 
* La función que itera y reduce cada elemento del *array*. (obligatorio)
* El **valor inicial** que utilizará como argumento de la función. Si no se especifica, en la primera iteración el valor inicial será el primer elemento del *array* y no ejecuta la función.

```js
let reducedValue = array.reduce(function(), initialValue)
```

### Parámetros de la función como argumento en `reduce`

La función, que recibe como argumento el método `map`, utiliza **cuatro parámetros**:
* El **valor acumulado por la función** *(callback)*. En la primera iteración será igual al valor inicial del argumento del método. (obligatorio)
* El **valor actual del elemento iterado**. Es decir, si es la primera iteración, será el primer elemento, y así sucesivamente. (obligatorio)
* El **índice del elemento iterado**. Es decir, si es la primera iteración, será el índice `0`, y así sucesivamente.
* El ***array* que está iterando**.

```js
let reducedValue = array.reduce(
    function(acumulator, element, index, array), 
    initialValue
)
```

### Cómo reducir elementos de un *array*

Con el método `reduce`, solo debemos establecer la función que indique una **reducción** para cada elemento.

Por ejemplo, creemos un *array* con números y reduzcamos los elementos a partir de la suma de sus cuadrados.

```js
const numbers = [5,4,8,6,2]

const total = numbers.reduce((suma, number) => suma + number**2)

console.log(total) // 125
```

Observa que hay un error, el total está incorrecto. Si **no se especifica el valor inicial** del método, entonces tomará el primer elemento (`5`) sin ejecutar la función reductora. 

| **Iteración** | **Reducción** |
| --- | --- |
| 1 | `5` |
| 2 | `5 + 4**2 = 21` |
| 3 | `21 + 8**2 = 85` |
| 4 | `85 + 6**2 = 121` |
| 5 | `121 + 2**2 = 125` |

Por lo tanto, debes **especificar el valor inicial** para solucionar este problema.

```js
const numbers = [5,4,8,6,2]

const reducedValue = numbers.reduce((suma, number) => (
    suma + number**2
), 0) // <- Valor inicial

console.log(reducedValue) // 145
```

De esta manera se ejecutará la función reductora adecuadamente.

| **Iteración** | **Reducción** |
| --- | --- |
| 1 | `**0** + 5**2 = 25` |
| 2 | `25 + 4**2 = 41` |
| 3 | `21 + 8**2 = 105` |
| 4 | `85 + 6**2 = 141` |
| 5 | `121 + 2**2 = 145` |

## Aprende sobre los métodos de búsqueda con `find` y `findIndex`

Los métodos `find` y `findIndex` permiten realizar búsquedas en un *array* y retornar el **primer elemento** que cumpla con la condición especificada.

Si quieres saber más sobre este tema, continúa con la clase de **[¿Por qué aprender desarrollo web?](https://platzi.com/clases/10266-javascript/70355-busqueda-de-elementos-con-find-y-findindex/)**.

***Contribución creada por:** Andrés Guano (Associate).*
