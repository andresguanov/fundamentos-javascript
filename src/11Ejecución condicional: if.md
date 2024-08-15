Los condicionales son **estructuras de control que te permiten evaluar** diferentes expresiones y realizar determinadas acciones.

## Cómo utilizar un condicional
**Un condicional evalúa una expresión o condición si es verdadera.** Por ejemplo, si mi edad es mayor o igual que 18, puedo conducir.

```js
if (edad >= 18){
  console.log("Puedes conducir")
}
```

La palabra reservada `else` sirve para evaluar un bloque cuando la expresión del `if` es falsa, pero no es obligatorio colocarlo. En el ejemplo anterior, cuando la edad menor que 18, entonces no puedes conducir.

```js
if (edad >= 18){
  console.log("Puedes conducir")
} else {
  console.log("No puedes conducir")
}
```

En otras palabras, si (`if`) una acción (`expresión`) es verdadera (`true`) realizo una acción (`bloques de código`), caso contrario (`else`) realizo otra acción.

## Cómo anidar condicionales
Has aprendido a utilizar un condicional, pero ¿y si tenemos varias condiciones? **Entonces utilizamos las palabras reservadas `else if` junto a la condición a ejecutar**, puedes utilizar varias condiciones que necesites. Sin embargo, JavaScript evalúa la primera condición, luego a la segunda, y así sucesivamente. Esto es importante para ordenar las condiciones correctamente  y no sobreescribirlas.

```js
if (condicion1){
   // Bloque 1
} else if (condicion2){
    // Bloque 2
} else if (condicion3){
   // Bloque 3
} else {
    // Bloque else
}
```

Por ejemplo, un cliente solicita un descuento según el número de artículos que ha comprado, la tienda ofrece 3 descuentos: 10% si ha comprado más de 5 artículos, 15% si son más de 10 artículos, y todo por encima de 15 artículos recibe un 20% de descuento.

```js
let precio = 10 

if (articulos >= 5 && articulos < 10){
   precio = precio * (1 - 0.10)

} else if (articulos >= 10 && articulos < 15){
    precio = precio * (1 - 0.15)

} else {
    precio = precio * (1 - 0.20)
}

console.log(precio)
```

## Qué es el operador ternario

**El operador ternario es una forma de simplificar un condicional.** Esto sirve para evaluar una condición de manera rápida. 

La estructura es la siguiente y se lee como: "Evalúa la condición (`?`), si es verdadera ejecuta el "Bloque verdadero", caso contrario (`:`), ejecuta el "Bloque falso".

```
condicion ? Bloque verdadero : Bloque falso
```

Por ejemplo, guardemos en una variable un mensaje si un número es par o impar.

```js
let numero = 5
let esPar = numero % 2 === 0 ? "Es par" : "No es par"

console.log(esPar) // No es par
```

En este caso, la condición es `numero % 2 === 0`, si es verdadera se ejecuta `"Es par"`, caso contrario `"No es par"`.


## Aprende a programar: Adivina el número

Ahora estás listo para crear un juego de adivinar el número. Donde aplicarás todo lo aprendido hasta ahora.

Si quieres saber más sobre este ejercicio, continúa con la clase de **[Ejercicio: Adivina el número](https://platzi.com/home/clases/10266-javascript/70342-ejercicio-adivina-el-numero/)**.

***Contribución creada por:** Andrés Guano (Associate).*
