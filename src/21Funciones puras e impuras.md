Las funciones puras son aquellas que **no modifican el estado de las variables** y **no tienen efectos secundarios**. Es decir, siempre que se les pase el mismo valor, devolverán el mismo resultado. Por otro lado, las funciones impuras son aquellas que no cumplen con estas características.

## Cómo identificar una función pura

Para identificar una función pura, se deben tener en cuenta las siguientes características:

* **Determinismo**: siempre que se le pase el mismo valor, devolverá el mismo
* **Transparencia referencial**: se puede reemplazar la función por su valor sin cambiar el resultado
* **No tiene efectos secundarios**

Las funciones puras son muy útiles en programación funcional porque nos permiten tener un **código más limpio, predecible y fácil de evaluar**.

Por ejemplo, la siguiente función es pura:

```js
function pura(a, b) {
  return a + b
}
```

Esta función recibe dos parámetros y devuelve la suma de ambos. Siempre que se le pase los mismos valores, devolverá el mismo resultado. Además, no modifica variables globales ni tiene efectos secundarios. Y finalmente, se puede reemplazar por su valor sin cambiar el resultado.

### Qué es determinismo

El determinismo se refiere a que siempre que se le pase el mismo valor, devolverá el **mismo resultado**. 

Un caso común en el que **no se cumple** con el determinismo es cuando se genera un número aleatorio. En este caso, no se puede garantizar que el resultado sea el mismo en todo momento.

### Qué es transparencia referencial

La transparencia referencial se refiere a que se puede **reemplazar la función por su valor sin cambiar el resultado**. Por ejemplo, si reemplazamos la función `pura` por su valor, obtendremos el mismo resultado:

```js
console.log(pura(2, 3)) // 5
console.log(2 + 3) // 5
```

### Qué son los efectos secundarios en JavaScript

Los efectos secundarios o *side effects* son cualquier **cambio que se haga fuera de la función**. En JavaScript, se pueden considerar efectos secundarios a las siguientes acciones:

* Modificar variables globales
* Modificar parámetros de entrada
* Solicitudes a servidores externos
* Imprimir en consola o en pantalla
* Manipulación del DOM (Document Object Model)
* Funciones que generan un resultado diferente por definición, como obtener la hora actual o un número aleatorio

## Cómo identificar una función impura

Una función impura es aquella que **no cumple con las características de una función pura**. 

Una función pura no es mejor que una impura, y viceversa. Todo depende del contexto en el que se esté trabajando.

### Cómo modificar una variable global

Una función impura es aquella que modifica una variable global. Esto parece simple de evitar, pero imagina modificar una variable global en un proyecto grande, esto puede causar problemas de mantenimiento.

```js
function impura() {
  a = a + 10
}

impura()
console.log(a) // 15
```

### Cómo modificar un parámetro de entrada

Una función impura es aquella que modifica un parámetro de entrada. Esto ocurre cuando se pasa un objeto o un array como parámetro y se modifica dentro de la función.

Esto sucede porque en JavaScript, los tipos de datos complejos comparten la misma **referencia en memoria**.

```js
const usuario = { nombre: 'Andrés' }

function impura(objeto) {
  objeto.nombre = 'Platzi'
}

impura(usuario)
console.log(usuario) // { nombre: 'Platzi' }
```

Como puedes observar, aunque `usuario` y `objeto` son variables diferentes, comparten la misma referencia en memoria. Esto quiere decir que si se modifica `objeto`, también se modificará `usuario`.

### Cómo hacer solicitudes a servidores externos

Una función impura es aquella que hace solicitudes a servidores externos. Esto se debe a que no se puede garantizar que la respuesta sea la misma en todo momento.

Las solicitudes a servidores es un tema de programación asíncrona, esto se discutirá en la clase de **[Promesas en JavaScript](https://platzi.com/clases/10266-javascript/70375-promesas-en-javascript//)**.

```js
function impura() {
  return fetch('https://api.com')
    .then(response => response.json())
}

impura() // Respuesta diferente en cada llamada
```

### Cómo imprimir en consola o en pantalla

Una función impura es aquella que imprime en consola o en pantalla. Esto se debe a que alteramos el objeto global `console`, por lo tanto estamos teniendo un efecto secundario.

```js
function impura() {
  console.log('Hola')
}

impura() // Hola
```

### Cómo manipular el DOM

Una función impura es aquella que manipula el DOM. Esto se debe a que alteramos el objeto global `document`, por lo tanto estamos teniendo un efecto secundario.

El DOM (Document Object Model) es una interfaz de programación que permite a los programadores manipular la estructura, estilo y contenido de un documento HTML para crear páginas web interactivas.

Este es un tema que aprenderás en el curso de **[Manipulación del DOM](https://platzi.com/cursos/document-object-model/)**.

```js
function impura() {
  document.querySelector("body").innerHTML = 'Hola'
}

impura() // Hola
```

Lo que hace esta función, es seleccionar el elemento `body` del documento HTML y cambiar su contenido por la palabra `Hola`. Si quieres probarlo, puedes copiar el código en la consola de tu navegador o usar esta [demostración de código](https://codi.link/%7C%7CZnVuY3Rpb24gaW1wdXJhKCkgew0KICBkb2N1bWVudC5xdWVyeVNlbGVjdG9yKCJib2R5IikuaW5uZXJIVE1MID0gJ0hvbGEnDQp9DQoNCmltcHVyYSgpIC8vIEhvbGE=).


### Qué son las funciones que generan un resultado diferente

Una función impura es aquella que obtiene la hora actual. Esto se debe a que no se puede garantizar que la hora sea la misma en todo momento.

```js
function impura() {
  return new Date()
}
```

El objeto global `Date` nos permite manejar fechas en JavaScript. Puedes consultar más información en MDN Web Docs sobre el objeto [Date](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Date).

También, una función impura es aquella que genera un número aleatorio. Esto se debe a que no se puede garantizar que el número sea el mismo en todo momento.

```js
function impura() {
  return Math.random()
}
```

## Aprende sobre las funciones flecha y enlace léxico

Las funciones flecha o *arrow functions* son una forma más corta de escribir funciones en JavaScript. Además, tienen un enlace léxico, lo que significa que **no tienen su propio `this`**.

Si quieres saber más sobre este tema, continúa con la clase de **[Funciones flecha y enlace léxico](https://platzi.com/home/clases/10266-javascript/70371-arrow-function-y-enlace-lexico/)**.

***Contribución creada por:** Andrés Guano (Associate).*
