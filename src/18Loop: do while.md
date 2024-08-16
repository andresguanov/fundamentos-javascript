El ciclo `do while` es una estructura de control repetitiva que se utiliza para **ejecutar un bloque de código al menos una vez, y luego repetirlo mientras una condición sea verdadera**.

## Cómo utilizar el ciclo `do while`

El funcionamiento del ciclo `do while` es similar al ciclo `while`, con la diferencia de que el bloque de código se ejecuta al menos una vez, y luego se repite mientras la condición sea verdadera.

La estructura del ciclo `do while` es la siguiente:

```js
do {
  // Bloque de código (se ejecuta al menos una vez)
  // Cambiar la condición para salir del bucle
} while (condición)
```

En este caso, el bloque de código se **ejecuta al menos una vez**, y luego se repite mientras la condición sea verdadera. Si la condición es falsa, el ciclo termina.

### Practiquemos con el ciclo `do while`

En este ejemplo, vamos a generar los números del 1 al 10 con un ciclo `do while`.

```js
let numero = 1 // Inicializamos la variable

do {
  console.log(numero) // Bloque de código
  numero++ // Cambiar la condición del bucle
} while (numero <= 10) // Condición
```

En este caso, la variable `numero` se inicializa en 1, y luego se imprime en la consola. Luego, la variable se incrementa en uno y se repite el ciclo mientras `numero` sea menor o igual a 10.

¿Qué pasaría si `numero` se inicializa en 11? 

```js
let numero = 11 // Inicializamos la variable

do {
  console.log(numero) // Bloque de código
  numero++ // Cambiar la condición del bucle
} while (numero <= 10) // Condición
```

## Aprende sobre la estructura de una función

Las funciones son bloques de código que se pueden reutilizar en diferentes partes de un programa. 

Si quieres saber más sobre este tema, continúa con la clase de **[Anatomía de una función](https://platzi.com/home/clases/10266-javascript/70368-anatomia-de-una-funcion/)**.

***Contribución creada por:** Andrés Guano (Associate).*
