
En programación, los *arrays* son esenciales para manejar colecciones de datos. Aprenderás a manejar **métodos mutables** para modificar esta estructura de datos tanto al principio como al final.

## Cómo utilizar el método `push`
El método `push` **agrega** uno o varios elementos al **final** del *array* original. El método recibe como argumento los valores a agregar. Retorna el número de elementos del *array* modificado.

```js
let array = [1,2,3]
let resultado = array.push(4,5)

console.log(array) // [ 1, 2, 3, 4, 5 ]
console.log(resultado) // 5
```

## Cómo utilizar el método `pop`
El método `pop` **extrae** el elemento del **final** del *array* original. Retorna el elemento extraído.

```js
let array = [1,2,3,4]
let ultimoElemento = array.pop()

console.log(array) // [ 1, 2, 3 ]
console.log(ultimoElemento) // 4
```

## Cómo utilizar el método `unshift`
El método `unshift` **agrega** uno o varios elementos al **inicio** del *array* original. El método recibe como argumento los valores a agregar. Retorna el número de elementos del *array* modificado.

```js
let array = [1,2,3]
let resultado = array.unshift("Hola", 0)

console.log(array) // [ 'Hola', 0, 1, 2, 3 ]
console.log(resultado) // 5
```

## Cómo utilizar el método `shift`
El método `shift` **extrae** el elemento del **inicio** del *array* original. Retorna el elemento extraído.

```js
let array = [1,2,3,4]
let primerElemento = array.shift()

console.log(array) // [ 2, 3, 4 ]
console.log(primerElemento) // 1
```

## Aprende sobre los métodos de iteración `map` y `forEach`

Los métodos `map` y `forEach` permiten recorrer los elementos de un array y ejecutar una función para cada uno.

Si quieres saber más sobre este tema, continúa con la clase de **[¿Por qué aprender desarrollo web?](https://platzi.com/clases/10266-javascript/70353-iteracion-con-map-y-foreach/)**.

***Contribución creada por:** Andrés Guano (Associate).*
