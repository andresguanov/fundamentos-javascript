Un bucle *(loop)* o ciclo repetitivo es una estructura de control que te **permite realizar una o varias instrucciones mientras una condición sea verdadera**.

Existen dos tipos de ciclos repetitivos: 
* For (para)
* While (mientras)

## Qué es un ciclo *for*

Para el ciclo `for` **conocemos la cantidad de veces** que la estructura repetirá una o varias instrucciones.

Por ejemplo, si queremos 10 números, sabemos que el ciclo se repetirá 10 veces.


## Cómo utilizar el ciclo *for*

Para utilizar el ciclo `for`, debes seguir una estructura específica. La palabra reservada `for`, la condición y el bloque de código que se repetirá.

```js
for (condición) {
  // Bloque de código
}
```

La condición del bloque `for` consta de 3 partes:

1. Inicialización de la variable de control.
2. Condición de continuación del bucle, si esta condición es `false`, el bucle termina.
3. Los pasos que se deben realizar en cada iteración. Puede ser un incremento o decremento, o cualquier otra operación que modifique la variable de control.

```js
for (let inicio; condición; pasos) {
  // Bloque de código a repetir
}
```

### Practiquemos el uso del bucle *for*

Por ejemplo, generemos los números del 1 al 10:
* **Inicio del ciclo:** inicializamos una variable con el valor de 1, generalmente se utiliza `i` (índice) como variable para el bucle, pero no es obligatorio. En este caso utilizaremos `let num = 1`
* **Condición de control:** La condición será mientras sea menor o igual que 10 `num <= 10`
* **Pasos:** Debemos aumentar la variable en una unidad, por lo tanto, podemos utilizar `num = num +1`.

La estructura es la siguiente:
```js
for (let num = 1; num <= 10; num = num + 1) {
  console.log(num)
}
```

Esto se leería como: "Para (`for`) la variable `num` que inicia en 1 (`num = 1`) mientras sea menor o igual que 10 (`num <= 10`) en pasos de 1 (`num++`) ejecuta `console.log`".

Mira la siguiente tabla que muestra cómo cambia la variable `num` en cada ciclo.

| **# Ciclo** | **num** | `num <= 10` | `num = num + 1` |
| --- | --- | --- | --- |
| 1.º | 1 | true | 2 |
| 2.º | 2 | true | 3 |
| ... | ... | ... | ... |
| 10.º | 10 | true | 11 |
| 11.º | 11 | false | Termina el bucle |

## Qué es iterar, iterable e iteraciones

**Iterar** es el proceso de repetir una o varias instrucciones. Un objeto **iterable** es aquel que puede ser recorrido o iterado, como un *string* o un *array*. **Iteraciones** son las veces que se repite el ciclo.

En algunos ejemplos, observarás la letra `i` como variable de control. Esta variable es comúnmente utilizada en los ciclos para hacer referencia a la palabra *índice* o *index*. También se utilizan otras letras como `j`, `k` o `l`


## Qué son los operadores de incremento y decremento

El operador de incremento (`++`) y decremento (`--`) consiste en **aumentar o disminuir una sola unidad** a una variable, respectivamente, de forma más corta.

Estos operadores se pueden utilizar antes y después de una variable.

```js
// Después de la variable
variable++
variable--

// Antes de la variable
++variable
--variable
```

Sin embargo, si se utiliza antes o después, el comportamiento es diferente: 

* Si está **después**, retorna el valor actual y luego aumenta o disminuye el valor de la variable
* Si está **antes**, el valor de la variable aumenta o disminuye y luego devuelve el valor actualizado

Observa los siguientes ejemplos con su respectivo resultado:

```js
let a = 3
let b = 3

console.log(a++) //3
console.log(++b) //4

console.log(a) //4
console.log(b) //4
```

Es decir, `a++` retorna `3` y luego aumenta a `4`, mientras que `++b` aumenta a `4` y retorna `4`. Aunque en ciclos `for` no hay diferencia, es importante tener en cuenta este detalle.

### Operadores de incremento y decremento en ciclos *for*

En el ciclo `for`, puedes utilizar los operadores de incremento y decremento para modificar la variable de control.

```js
for (let i = 0; i < 10; i++)
```

## Qué son los operadores de asignación combinada
En la clase de [Anatomía de una variable](https://platzi.com/clases/10266-javascript/70366-anatomia-de-una-variable/) aprendiste lo que es un operador de asignación (`=`). 

### Operadores de asignación combinada

En ciertos casos, **re-asignarás la misma variable más otro valor.** Estas variables pueden utilizarse como acumuladores o contadores.

```js
let contador = 1
contador = contador + 1 // contador = 1 + 1

console.log(contador) // 2
```

Una forma para evitar repetir la reasignación de la variable, es **combinarlas** con los operadores aritméticos antes del operador de asignación.

```js
let contador = 1
contador += 1

console.log(contador) // 2
```

### Tabla de operadores de asignación combinada

| **Tipo** | **Operador** | **Forma larga** |
| --- | --- | --- |
| Asignación de suma | `a += b` | `a = a + b` |
| Asignación de resta | `a -= b` | `a = a - b` |
| Asignación de multiplicación | `a *= b` | `a = a * b` |
| Asignación de división | `a /= b` | `a = a / b` |

### Cómo utilizar los operadores de asignación combinada en ciclos *for*

En los ciclos `for`, puedes utilizar los operadores de asignación combinada para modificar la variable de control.

```js
for (let i = 0; i < 10; i += 6) { // Los pasos son cada 6
  console.log(i)
}
```

## Qué es un array o arreglo

Un *array* es una estructura de datos que permite almacenar una serie de datos localizados por índices, separados por comas entre corchetes (`[]`). Existe una sección en el curso que explica [la estructura de datos de Arrays](https://platzi.com/clases/1814-basico-javascript/26303-arrays/). 

```js
// Ejemplos de arrays
let nombres = ["Andres", "Diego", "Platzi", "Ramiro", "Silvia"]
let numeros = [1, 2, 3, 4, 5]
```

### Cómo recorrer *arrays* con el ciclo *for*
En el anterior ejemplo aprendiste a generar números del 1 al 10, utilizaremos la misma lógica para recorrer un *array*. 

¿Qué debemos utilizar para acceder a los elementos de un *array*? Exactamente, sus índices (variable `i`). Debemos generar los índices desde `0` hasta `length` (que no debe estar incluido). Con esto, utilizamos la misma variable `i` para acceder a cada elemento con la sintaxis de corchetes `array[i]`.

La estructura sería la siguiente:

```js
let nombres = ["Andres", "Diego", "Platzi", "Ramiro", "Silvia"]

for(let i = 0; i < nombres.length; i++){
  console.log( nombres[i] )
}
```

## Aprende sobre estructura de control repetitiva: `for ... of`

El ciclo `for ... of` es una variación del ciclo `for` que se utiliza para **recorrer los valores de los elementos de un iterable**.

Si quieres saber más sobre este tema, continúa con la clase de **[Estructuras de repetición: `for ... of`](https://platzi.com/clases/10266-javascript/70345-loop-for-of/)**.

***Contribución creada por:** Andrés Guano (Associate).*
