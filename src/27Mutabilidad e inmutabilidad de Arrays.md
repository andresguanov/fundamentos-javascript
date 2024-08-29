La mutabilidad e inmutabilidad son conceptos importantes en la programación. Definen si un objeto **puede ser modificado o no**. De hecho, los *arrays* son mutables y los *strings* son inmutables, por definición.

## Qué es la referencia en memoria

En los lenguajes de programación, cada estructura está guardada en una **referencia en memoria** (en la memoria RAM). Por lo tanto, si cambiamos un elemento en un **tipo objeto**, también lo haremos en su referencia.

Por ejemplo, al asignar un *array* en otra variable, esa variable tendrá la **misma referencia en memoria que el original**, entonces, si se realiza un cambio en los elementos del original, también cambiará en la copia.

```js
const original = [1,2,3]
const copia = original
copia[0] = "Hola"

console.log(original) // [ 'Hola', 2, 3 ]
console.log(original === copia) // true
```

Esto también ocurre con objetos: 

```js
const original = {nombre: "Andres", edad: 20}
const copia = original
copia.nombre = "Platzi"

console.log(original) // { nombre: 'Platzi', edad: 20 }
console.log(original === copia) // true
```

## Qué es mutabilidad e inmutabilidad

La mutabilidad se refiere a la capacidad de un objeto para ser **modificado después de haber sido creado**. Esto significa que se pueden cambiar sus propiedades o estado sin necesidad de crear un nuevo objeto o valor.

Por ejemplo, los *arrays* son mutables por definición, por lo que se pueden modificar sus elementos sin errores.

```js	
let array = [1,2,3]
array[0] = "Hola"

console.log(array) // [ 'Hola', 2, 3 ]
```

La inmutabilidad se refiere a la propiedad de un objeto o valor que, una vez creado, **no puede ser modificado**. Esto significa que cualquier intento de cambiar su estado o contenido resultará en la creación de un nuevo objeto o valor en lugar de modificar el original.

Por ejemplo, los *strings* son inmutables, por lo que no se pueden modificar sus caracteres.

```js
let string = "Hola"
string[0] = "h" // TypeError: Cannot assign to read only property '0' of string 'Hola'
```

### Qué elegir entre mutabilidad e inmutabilidad

La mutabilidad es más flexible y una buena opción si se requiere **cambiar, actualizar o eliminar datos**; pero, puede ocasionar fallos o resultados erróneos en nuestra aplicación debido a las referencias en memoria. 

La inmutabilidad es más exigente, te permite generar **nuevas estructuras para manejarlas sin cambiar la origina**l; pero, puede provocar que ocupe más memoria de la necesaria.

Por lo que, ¿cuál es mejor? La respuesta es ninguna, cada uno te permite manejar estructuras de datos, por ende es necesario identificar cuál forma es la adecuada a aplicar en un algoritmo y no afectar a otras variables o a la aplicación.

### Cómo hacer inmutabilidad en *arrays*

Para hacer inmutabilidad en *arrays*, se puede utilizar métodos que no modifiquen el *array* original, sino que **devuelvan un nuevo *array* con los cambios realizados**. 

Estos nuevos *arrays* tendrán una referencia en memoria distinta del original. Algunos de estos métodos son: `map`, `filter`, `reduce`, `slice`, `concat`, entre otros.

También, se puede utilizar el operador de propagación `...` o funciones como `structuredClone()` para copiar un *array* y modificarlo sin afectar del original.

## Qué es el método `concat`

El método `concat` consiste en crear un nuevo *array* a partir de la unión de otros valores o *arrays* especificados como argumentos. Este método es **inmutable** porque no modifica el *array* original, sino que crea un nuevo *array* con los elementos concatenados.

Este método recibe uno o varios argumentos: 
* Valores cualesquiera y/o *arrays* para concatenar.

```js
let resultado = array.concat(otroArray)
let resultado = array.concat(valor1, valor2, ..., valorN)
```

### Ejemplo de uso del método `concat`

Para este ejemplo, se utilizarán tres *arrays* con números enteros. Crearemos un nuevo *array* a partir de la concatenación de los *arrays* originales y valores específicos.

```js
const numbers1 = [1,2,3,4]
const numbers2 = [5,6,7,8]
const numbers3 = [9,10,11,12]

// Concatenar valores
const result1 = numbers1.concat("hola", "mundo")
// Concatenar arrays
const result2 = numbers1.concat(numbers2)
// Concatenar valores y arrays
const result3 = numbers1.concat(numbers2, "hola")
// Concatenar varios arrays
const result4 = numbers1.concat(numbers2, numbers3)

result1 // [ 1, 2, 3, 4, 'hola', 'mundo' ]
result2 // [ 1, 2, 3, 4, 5, 6, 7, 8 ]
result3 // [ 1, 2, 3, 4, 5, 6, 7, 8, 'hola' ]
result4 // [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12 ]
```

Si revisas los *arrays*: `numbers1`, `numbers2` y `numbers3`, observarás que no han cambiado. Esto se debe a que el método `concat` es inmutable.

## Cómo identificar si una variable es un *array*

Como recordarás en la clase [Anatomía de un *Array*](https://platzi.com/clases/10266-javascript/70366-anatomia-de-una-variable/) se mencionó que los *arrays* son de tipo `'object'`. Por lo que no se puede identificar si una variable es un *array* con el operador `typeof`.

Para identificar si una **variable es un *array***, se debe utilizar el método `Array.isArray()`. Este método devuelve `true` si el argumento es un *array*.

```js
let numeros = [1,2,3,4]
console.log(typeof numeros) // 'object'

let esArray = Array.isArray(numeros)
console.log(esArray) // true
```

## Aprende sobre los métodos `push` y `pop`

Los métodos `push` y `pop` son dos métodos mutables que permiten **agregar y eliminar elementos** al final de un *array*, respectivamente.

Si quieres saber más sobre este tema, continúa con la clase de **[Métodos de modificación básica](https://platzi.com/home/clases/10266-javascript/70352-modificacion-basica-del-final-con-push-pop/)**.

***Contribución creada por:** Andrés Guano (Associate).*
