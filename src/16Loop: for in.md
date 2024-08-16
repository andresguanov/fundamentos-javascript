El ciclo `for ... in` es una variación del ciclo `for` que se utiliza para **recorrer las propiedades de un enumerable**, como los objetos.

## Qué es un objeto

Un objeto es una **colección de entradas**, y cada entrada es una **asociación entre un nombre (o propiedad) y un valor**. Por ejemplo, un objeto `persona` puede tener las propiedades `nombre`, `edad`, `género`, `nacionalidad`, etc.

Un objeto se define con llaves `{}` y sus entradas se separan por comas `,`. Cada entrada se define con una propiedad seguido de dos puntos `:` y su valor.

```js
let usuario = {
  // Propiedad: Valor
  nombre: 'Andrés',
  edad: 25,
  genero: 'masculino',
}
```

Ten en cuenta este concepto hasta explicarlo en la clase de **[Objetos](https://platzi.com/clases/10266-javascript/70358-anatomia-de-un-objeto/)**.

## Qué es un enumerable 

Un enumerable es una propiedad de un objeto que puede ser **enumerada**. Es decir, que puede ser recorrida por un ciclo `for ... in`. Por defecto, todas las propiedades de un objeto son enumerables, excepto las propiedades que se crean con el método `Object.defineProperty()`.

## Cómo utilizar el ciclo `for ... in`

La estructura del ciclo `for ... in` es la siguiente:

```js
for (let propiedad in objeto){
  //Bloque de código
}
```

La variable `propiedad` es la **referencia** a cada una de las propiedades del objeto. Este puede **tener cualquier nombre**, por eso se inicia con `let` o `const`, debido a que es una variable como el índice `i` en el bucle `for`. 

```js
for (let propiedad in usuario) {
  console.log(propiedad) // nombre edad genero
}
```

Esto puede ser de ayuda para acceder a los valores de las propiedades del objeto.

```js
for (let propiedad in usuario) {
  console.log(usuario[propiedad]) // Andrés 25 masculino
}
```

### Limitaciones del ciclo `for ... in`

Si intentas recorrer un objeto con la estructura `for propiedad of objeto`, existirá un error, porque un **objeto no es un iterable**.

```js
for (let propiedad of usuario) {
  console.log(propiedad) // ❌ TypeError: usuario is not iterable
}
```

Por otro lado, si intentas recorrer un iterable con la estructura `for propiedad in iterable`, no obtendrás los valores de los elementos, sino los **índices de cada uno**.

Esto se debe a que los iterables son objetos en JavaScript , como te lo mencioné en la clase de [Tipos de Datos](https://platzi.com/clases/10266-javascript/70444-tipos-de-datos-en-javascript/), y sus índices son las propiedades enumerables.

```js
let numeros = ["Python", "JavaScript", "Java", "C++"]

for (let propiedad in numeros) {
  console.log(propiedad) // 0 1 2 3
}
```

## Aprende sobre estructura de control repetitiva: `while`

El ciclo `while` es una estructura de control repetitiva que se utiliza para **ejecutar un bloque de código mientras una condición sea verdadera**.

Si quieres saber más sobre este tema, continúa con la clase de **[Estructuras de repetición: `while`](https://platzi.com/clases/10266-javascript/70347-loop-while/)**.

***Contribución creada por:** Andrés Guano (Associate).*
