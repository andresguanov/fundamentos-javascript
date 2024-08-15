**Los operadores lógicos comparan dos o más expresiones y devuelve un valor lógico (verdadero o falso).** Las expresiones son comparaciones entre valores, se utiliza en conjunto con los operadores de comparación.

### Qué es el operador disyunción lógico
**El operador de disyunción o *AND* (`&&`) devuelve verdadero, si y solo si ambas expresiones son verdadero.** Se lee de la siguiente manera: "La expresión 1 es verdadero **Y** la expresión 2 es verdadero, entonces es verdadero".

| **Expresión 1** | **Expresión 2** | **1 && 2** |
| --- | --- | --- |
| true | true | true |
| true | false | false |
| false | true | false |
| false | false | false |

Por ejemplo, si queremos saber si un número está entre 10 **y** 20. Es decir, un número que es mayor o igual que 10 **Y** menor o igual que 20.

```js
let a = 15
let b = 5

(a >= 10) && (a <= 20) // true
(b >= 10) && (b <= 20) // false
```

### Qué es el operador unión lógico
**El operador de unión u *OR* (`||`) devuelve verdadero, si y solo si, alguna expresión es verdadero.** Se lee de la siguiente manera: "La expresión 1 es verdadero **O** la expresión 2 es verdadero, entonces es verdadero".

| **Expresión 1** | **Expresión 2** | **1 \|\| 2** |
| --- | --- | --- |
| true | true | true |
| true | false | true |
| false | true | true |
| false | false | false |

Por ejemplo, si queremos saber si un número no está entre 10 **y** 20. Es decir, un número que es menor o igual que 10 **O** mayor o igual que 20.

```js
let a = 15
let b = 5

(a <= 10) || (a >= 20) // false
(b <= 10) || (b >= 20) // true
```

### Qué es el operador negación lógico
**El operador de negación o *NOT* (`!`) devuelve el valor lógico contrario a la expresión.** Se lee de la siguiente manera: "La expresión es verdadero, entonces es falso".

| **Expresión 1** |  **! 1** |
| --- | --- |
| true |  false |
| false |  true |

Por ejemplo, si queremos saber si un número no es menor que 0. Es decir, la negación de que un número es menor que 0.

```js
let a = 5

!(a < 0) // true
!false // true
```
También se puede escribir únicamente `a > 0`, sin embargo, es únicamente para entender el propósito del operador de negación.



## Aprende sobre los condicionales en JavaScript

Los condicionales son estructuras de control que permiten tomar decisiones en un programa. En JavaScript, los condicionales se implementan con la instrucción `if`, `else if` y `else`.

Si quieres saber más sobre este tema, continúa con la clase de **[Condicionales](https://platzi.com/clases/10266-javascript/70341-ejecucion-condicional-if/)**.

***Contribución creada por:** Andrés Guano (Associate).*
