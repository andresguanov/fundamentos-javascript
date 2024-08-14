Los operadores aritméticos sirven para **realizar operaciones matemáticas** desde las más básicas como la suma y resta, hasta las más complejas como la exponenciación.

## Qué son los tipos de datos numéricos

Los **tipos de datos numéricos son aquellos que representan números**. En JavaScript, los valores enteros y decimales son considerados como el mismo tipo de dato `'number`. Sin embargo, en otros lenguajes de programación, son considerados como tipos de datos diferentes.

Los decimales también son conocidos como **números de punto flotante** o **flotantes**. Tenlo en cuenta si lo lees en algún otro lugar.

```js
let numeroEntero = 10
let numeroDecimal = 3.145
```

## Cómo utilizar operadores aritméticos

Podríamos dividir los operadores aritméticos en dos grupos: los **operadores simples** y los **operadores complejos**.

### Cómo utilizar operadores simples

Los operadores simples son los más comunes y se utilizan para realizar operaciones básicas. Estos son:

- **Suma** `+`
- **Resta** `-`
- **Multiplicación** `*`
- **División** `/`

```js
let suma = 10 + 5
let resta = 10 - 5
let multiplicacion = 10 * 5
let division = 10 / 5

console.log(suma) // 15
console.log(resta) // 5
console.log(multiplicacion) // 50
console.log(division) // 2
```

### Cómo utilizar operadores complejos

Los operadores complejos son aquellos que no son considerados como operaciones aritméticas simples. Estos son:

- **Módulo** `%`
- **Exponenciación** `**`

```js
let modulo = 10 % 3
let exponenciacion = 10 ** 3

console.log(modulo) // 1
console.log(exponenciacion) // 1000
```

Tendré en cuenta que la **exponenciación** ya conoces cómo funciona. Sin embargo, te explicaré cómo funciona el **módulo**.

### Cómo funciona la operación módulo

La operación módulo es una operación que **devuelve el residuo de una división**. Por ejemplo, si dividimos 10 entre 3, el residuo es 1.

```js
let modulo = 10 % 3

console.log(modulo) // 1
```

Esto es de utilidad para **saber si un número es par o impar**, o si un número es **divisible entre otro número**. Ya que si el residuo es 0, significa que es divisible.

Por ejemplo, si queremos saber si `152466` es divisible para `4`. Podemos hacer la operación módulo y si el resultado es `0`, significa que es divisible.

```js
let numero = 152466
let divisor = 4

let modulo = numero % divisor

console.log(modulo) // 2
```

Como el resultado es `2`, significa que `152466` no es divisible para `4`.

## Cómo redondear un número decimal

Una de las formas para **redondear un número decimal** es utilizando el método `toFixed`. Este método recibe un parámetro que indica la cantidad de decimales que deseas mostrar.

```js
let numero = 3.14159265359
let numeroRedondeado = numero.toFixed(2)

console.log(numeroRedondeado) // 3.14
```

Ten en cuenta que el método `toFixed` **no redondea** el número, sino que **lo trunca**. Es decir, elimina los decimales que no necesitas. También, el resultado es un *string*.

```js
typeof numeroRedondeado // 'string'
```

## Cómo realizar operaciones avanzadas con el objeto Math

El objeto `Math` es un **objeto global que contiene propiedades y métodos para realizar operaciones matemáticas avanzadas**. Algunos de los métodos más comunes son:

- **`Math.sqrt`**: Devuelve la raíz cuadrada de un número.
- **`Math.abs`**: Devuelve el valor absoluto de un número.
- **`Math.random`**: Devuelve un número aleatorio entre 0 y 1.
- **`Math.floor`**: Redondea un número hacia abajo.
- **`Math.ceil`**: Redondea un número hacia arriba.
- **`Math.round`**: Redondea un número al entero más cercano.

```js
let raizCuadrada = Math.sqrt(16)
let valorAbsoluto = Math.abs(-10)
let numeroAleatorio = Math.random()
let numeroRedondeadoAbajo = Math.floor(3.9)
let numeroRedondeadoArriba = Math.ceil(3.1)
let numeroRedondeado = Math.round(3.5)

console.log(raizCuadrada) // 4
console.log(valorAbsoluto) // 10
console.log(numeroAleatorio) // 0.123456789
console.log(numeroRedondeadoAbajo) // 3
console.log(numeroRedondeadoArriba) // 4
console.log(numeroRedondeado) // 4
```

El objeto `Math` es muy útil para realizar **operaciones matemáticas avanzadas**. Si quieres saber más sobre este objeto, puedes consultar la documentación oficial de [MDN Web Docs sobre el objeto Math](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Math).

## Cuáles son los valores númericos especiales en JavaScript

Existen tres valores numéricos especiales en JavaScript:

- **`Infinity`**: Representa el infinito matemático. Se obtiene al dividir un número por cero.
- **`-Infinity`**: Representa el infinito negativo. Se obtiene al dividir un número negativo por cero.
- **`NaN`**: Representa un error de cálculo. Significa "Not a Number".

```js
let infinito = 1 / 0
let infinitoNegativo = -1 / 0
let noEsUnNumero = "Hola" / 2

console.log(infinito) // Infinity
console.log(infinitoNegativo) // -Infinity
console.log(noEsUnNumero) // NaN
```

También los puedes utilizar como valor.

```js
typeof Infinity   // 'number'
typeof -Infinity  // 'number'
typeof NaN        // 'number'
```

### Por qué NaN es un valor numérico

Aunque `NaN` signifique "Not a Number", **es un valor numérico**. Esto se debe a que **es un valor especial que representa un error de cálculo**. Por ejemplo, si intentamos dividir una cadena de texto por un número, obtendremos `NaN`.

Sí lo sé, es un poco ilógico, **pero así funciona JavaScript**. Tenlo en cuenta.


## Aprende sobre la conversión de tipos en JavaScript

La conversión de tipos es un tema muy importante en JavaScript. Existen dos tipos de conversión de tipos: **type casting** y **coerción**.

Si quieres saber más sobre este tema, continúa con la clase de **[Conversión de tipos](https://platzi.com/home/clases/10266-javascript/70367-conversion-de-tipos-type-casting-y-coercion/)**.

***Contribución creada por:** Andrés Guano (Associate).*
