Los operadores de comparación, como su nombre lo indica, son utilizados para **comparar valores**. Estos operadores devuelven un valor lógico dependiendo si la comparación es verdadera o falsa.


## Qué son los operadores de igualdad

Los operadores de igualdad son utilizados para **comparar dos valores** y devuelven verdadero (`true`) si son iguales y falso (`false`) si no lo son. En JavaScript existe dos tipos de operadores de igualdad:


* **Igualdad por valor (`==`):** compara dos variables solamente por su valor. Por ejemplo: `"3"` de tipo *string* y `3` de tipo número son iguales.
* **Igualdad por valor y tipo de dato (`===`):** compara dos variables por su valor y tipo de dato. Por ejemplo: `"3"` de tipo *string* y `3` de tipo número no son iguales.

```js
//Igualdad por valor
"3" == 3 // true
3 == 3   // true

// Igualdad por valor y tipo de dato
"3" === 3 // false
3 === 3   // true
```

**Utiliza la comparación por valor y tipo de dato para evitar errores.** Los operadores de igualdad son diferentes al operador de asignación (`=`).

## Qué son los operadores de desigualdad

Los operadores de desigualdad son utilizados para comparar dos valores y devuelven verdadero (`true`) si son diferentes.

Igualmente que los operadores de igualdad, existen dos tipos:
* Desigualdad por valor (`!=`)
* Desigualdad por valor y tipo de dato (`!==`)

```js
//Desigualdad por valor
"3" != 3 // false
3 != 3   // false

// Desigualdad por valor y tipo de dato
"3" !== 3 // true
3 !== 3 // false
```

## Qué son los operadores de mayor o menor

Los operadores de mayor o menor evalúan si un número es mayor o menor que otro. Existen cuatro tipos de operadores de comparación:

* **Menor que (`<`):** devuelve verdadero si el valor de la izquierda es menor que el de la derecha.
* **Mayor que (`>`):** devuelve verdadero si el valor de la izquierda es mayor que el de la derecha.
* **Mayor o igual a que (`>=`):** devuelve verdadero si el valor de la izquierda es mayor o igual al de la derecha.
* **Menor o igual a que (`<=`):** devuelve verdadero si el valor de la izquierda es menor o igual al de la derecha.


```js
// Menor que
3 < 5 // true

// Mayor que
3 > 5 // false

// Mayor o igual a que
3 >= 3 // true
3 >= 5 // false

// Menor o igual a que
3 <= 3 // true
3 <= 5 // true
```

## Aprende sobre los operadores lógicos en JavaScript

Los operadores lógicos son utilizados para combinar dos o más expresiones lógicas y devuelven un valor verdadero o falso.

Si quieres saber más sobre este tema, continúa con la clase de **[Operadores lógicos](https://platzi.com/home/clases/10266-javascript/70340-operadores-logicos/)**.

***Contribución creada por:** Andrés Guano (Associate).*
