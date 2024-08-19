Las funciones flecha o *arrow functions* son una forma más corta de escribir funciones en JavaScript. Además, tienen un enlace léxico, lo que significa que **no tienen su propio `this`**. Se denominan función flecha por el conjunto de caracteres (`=>`) en su sintaxis, similar a una flecha hacia la derecha.


## Cómo declarar una función flecha

Para declarar una función flecha, se utiliza la siguiente sintaxis, similar a una función declarativa:

```js
//Función declarativa
function nombre (parámetros) {
  // Bloque de código
  return valorRetornado
}

//Función flecha
const nombre = (parámetros) => {
  // Bloque de código
  return valorRetornado
}
```

### Consideraciones al declarar una función flecha

Si la función flecha solo tiene un parámetro, puedes **omitir los paréntesis**.

```js
const nombre = parámetro => {
  return valorRetornado
}
```

Por otro lado, si la función flecha no contiene parámetros, deberás colocar paréntesis vacíos, **obligatoriamente**.

```js
const nombre = () => {
  return valorRetornado
}
```

Al igual que las funciones declarativas y expresivas, si no colocas un *return* explícito, la función retornará `undefined`.

### Qué es el retorno implícito

Las funciones flecha tienen un retorno implícito, es decir, se puede **omitir la palabra reservada `return`**, y el **código sea escrito en una sola línea**.

```js
//Función declarativa
function suma (a, b) {
  return a + b
}

//Función flecha
const suma = (a, b) => a + b
```

Si el retorno **requiere de más líneas** y aún deseas utilizarlo de manera implícita, deberás envolver la instrucción de retorno entre **paréntesis**.

```js
const suma = (a, b) => (
  a + b
)
```

## Cómo utilizar el enlace léxico

El enlace léxico es una característica de las funciones flecha que **permite acceder a las variables de un ámbito superior**. Esto significa que **no tienen su propio `this`**.

Es decir, si declaras una función flecha, el `this` de la función será el mismo que el objeto global. 

```js	
const saludar = () => {
  console.log(this)
}

saludar() // Window o Global Object
```

Sin embargo, si lo declaras como un método de un objeto, el `this` será `undefined`. Esto se refiere de que las funciones flecha no tienen su propio `this`.

```js
const cohete = {
  nombre: 'Falcon 9',
  despegar: () => {
    console.log(`¡${this.nombre} despegó!`)
  }
}
cohete.despegar() // ¡undefined despegó!
```


## Aprende sobre el contexto de ejecución o *scope*

El contexto de ejecución o *scope* es el alcance de las variables y funciones en un programa. Las funciones tienen acceso a las variables de su función padre, pero no al revés.

Si quieres saber más sobre este tema, continúa con la clase de **[Contexto de ejecución](https://platzi.com/clases/10266-javascript/70372-contextos-de-ejecucion-y-scope-chain/)**.

***Contribución creada por:** Andrés Guano (Associate).*
