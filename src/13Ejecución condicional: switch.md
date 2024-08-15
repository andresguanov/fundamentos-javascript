La estructura `switch` es otra forma de evaluar condiciones. A diferencia de `if`, `switch` evalúa **una expresión y dependiendo del resultado**, ejecuta un bloque de código.

## Cómo utilizar la estructura de control `switch`

Utilizamos la palabra reservada `switch`, seguido de la variable o expresión a evaluar, pero sin ningún operador de comparación.

```js
switch (expresion) {}
```

Después colocamos cada caso con la palabra reservada `case` y el valor que deberá ser igual a la expresión. Seguido colocamos el bloque de código a ejecutar y al final la palabra reservada `break` para que no vuelva a evaluar otra condición si ya se cumplió.

```js
switch (expresion) {
    case valor1: {
        // Bloque 1
        break
    }
    case valor2: {
        // Bloque 1
        break
    }     
}
```

La expresión será evaluada por cada caso, como si fuera `if (expresion === valor1)`, con una comparación estricta (valor y tipo de dato).

Finalmente, colocamos la condición por defecto con la palabra reservada `default` que se ejecutará si ninguno de los casos fue el correcto. Esto es semejante al bloque `else`. 

```js
switch (expresion) {
  case valor1: {
    // Bloque 1
    break
  }
  case valor2: {
   // Bloque 2
    break
  }
  default: {
    // Bloque por defecto
  }
}
```

### Ejemplo utilizando `switch`
Por ejemplo, creemos un semáforo.

```js
switch (color) {
  case "verde": {
    console.log("¡Sigue!")
    break
  }
  case "amarillo": {
    console.log("¡Detente!")
    break
  }
  case "rojo": {
    console.log("¡No puedes avanzar!")
    break
  }
  default: {
    console.log("¡No reconozco ese color! :(")
  }
}
```

Dependiendo de una variable `color`, se ejecutará un bloque de código según sea el caso. Pruébalo en tu editor de código.

## Cuándo deberías utilizar `switch`

Deberías utilizar `switch` cuando tengas **una gran cantidad de casos**, que con el condicional `if` produciría más cantidad de código ilegible. El problema con `switch` es que no es muy utilizado y se puede resolver con la estructura `if`. Sin embargo, conocer esta estructura te puede permitir escribir código más legible y mantenible en ciertos casos.


## Aprende sobre estructuras de control repetitivas

Las estructuras de control repetitivas, también llamados ciclos o bucles, son fundamentales para la programación. Permiten ejecutar un bloque de código múltiples veces, según una condición.

Si quieres saber más sobre este tema, continúa con la clase de **[Estructuras de repetición](https://platzi.com/home/clases/10266-javascript/70344-loop-for/)**.

***Contribución creada por:** Andrés Guano (Associate).*
