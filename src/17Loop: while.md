El ciclo `while` es una estructura de control repetitiva que se utiliza para **ejecutar un bloque de código mientras una condición sea verdadera**.

## Cómo utilizar el ciclo `while`

Para el ciclo `while` **no conocemos la cantidad de veces que la estructura repetirá una o varias instrucciones.** Aunque también se puede acoplar para que realice un determinado número de repeticiones. 

Por ejemplo, si queremos que un usuario ingrese un valor mayor a 0, no sabremos cuántas veces se equivocará. También, si queremos que un programa se ejecute hasta que el usuario ingrese una opción para detener el programa.

La estructura del ciclo `while` es la siguiente:

```js
while (condición) {
  // Bloque de código
  // Cambiar la condición para salir del bucle
}
```

En este caso la condición es una expresión lógica a evaluar, si es verdadera repite el bloque de código, si es falsa el ciclo termina. Debido a esto, **necesitas cambiar la variable de la condición, para que no exista un bucle infinito**.


### Practiquemos con el ciclo `while`

Se requiere generar los números del 1 al 10, con un bucle `while`.

La estructura es la siguiente:
```js
let numero = 1 // Inicializamos la variable

while ( numero <= 10 ){ // Condición
  console.log(numero) // Bloque de código
  numero++  // Cambiar la condición del bucle
}
```

Esto se leería como: "Mientras (`while`) la variable `numero` sea menor o igual que 10 (`numero <= 10`) ejecuta una o varias instrucciones (`console.log`); finalmente, aumenta la variable en uno (`numero++`) para que no exista un bucle infinito".

Controlar la variable numero es importante, porque si no se incrementa, la condición siempre será verdadera y el bucle se ejecutará infinitamente.

## Aprende sobre estructura de control repetitiva: `do while`

El ciclo `do while` es una estructura de control repetitiva que se utiliza para **ejecutar un bloque de código al menos una vez, y luego repetirlo mientras una condición sea verdadera**.

Si quieres saber más sobre este tema, continúa con la clase de **[Estructuras de repetición: `do while`](https://platzi.com/clases/10266-javascript/70348-loop-do-while/)**.

***Contribución creada por:** Andrés Guano (Associate).*
