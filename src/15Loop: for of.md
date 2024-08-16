El ciclo `for ... of` es una variación del ciclo `for` que se utiliza para **recorrer los valores de un iterable**, como pueden ser *strings*, *arrays*, entre otros. 

## Cómo utilizar el ciclo `for ... of`

La estructura del ciclo `for ... of` es la siguiente:

```js
for ( let elemento of array){
  //Bloque de código
}
```

La variable `elemento` es la **referencia a cada uno** de los elementos del *array*. Este puede tener cualquier nombre, por eso se inicia con `let` o `const`, debido a que es una variable como el índice `i` en el bucle `for`. 

```js
let array = [5, 4, 3, 2, 1]

for (let elemento of array) {
  console.log(elemento) // 5 4 3 2 1
}
```

Por convención, se escribe la variable `elemento` en **singular** con respecto al nombre del `array`. Por ejemplo, si el nombre del *array* es `datos`, el nombre de la variable de cada elemento sería `dato`, y así sucesivamente. También se puede utilizar alguna abreviación o nombre que tenga sentido con el contexto, como `el` para `elements`.

```js
for (let dato of datos) { ... }
for (let name of names) { ... }
for (let number of numbers) { ... }
for (let el of elements) { ... }
```

### Limitaciones del ciclo `for ... of`

El ciclo `for ... of` **solo accede al valor** de cada uno de los elementos del iterable. Por consiguiente, si quieres cambiar un *array* original, no podrás hacerlo, porque necesitas su índice para acceder y cambiar su valor.

Por ejemplo, si quieres duplicar el valor de cada elemento en el *array*, necesitarás su índice.

```js
let numbers = [5, 4, 3, 2, 1]

// ❌ No cambia el array original
for (let number of numbers) {
  number = number * 2
}

console.log(numbers) // [5, 4, 3, 2, 1]

// ✅ Cambia el array original
for(let i=0; i < numbers.length; i++){
  numbers[i] = numbers[i] * 2
}

console.log(numbers) // [ 10, 8, 6, 4, 2 ]
```

Sin embargo, esto no es malo, **depende del problema que estés enfrentando.** Una forma de solucionar el anterior problema utilizando `for ... of`, es creando otro *array* vacío para llenarlo con los nuevos valores, de esta manera no cambiará el *array* original.

```js
let numbers = [5, 4, 3, 2, 1]
let duplicates = []

for (let number of numbers) {
  duplicates.push(number * 2)
}

console.log(duplicates) // [ 10, 8, 6, 4, 2 ]
```

El método `push()` agrega un nuevo elemento al final del *array* `duplicates`. Esto será explicado en la clase de **[Arrays](https://platzi.com/clases/10266-javascript/70350-introduccion-a-arrays/)**.


## Aprende sobre estructura de control repetitiva: `for ... in`

El ciclo `for ... in` es una variación del ciclo `for` que se utiliza para **recorrer las propiedades de un objeto**.

Si quieres saber más sobre este tema, continúa con la clase de **[Estructuras de repetición: `for ... in`](https://platzi.com/clases/10266-javascript/70346-loop-for-in/)**.

***Contribución creada por:** Andrés Guano (Associate).*
