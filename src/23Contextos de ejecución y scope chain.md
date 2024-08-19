El ***scope*** es cada uno de los **entornos de ejecución donde las variables tienen alcance dentro del código de JavaScript**. En otras palabras, determina qué valor tendrá la variable dependiendo dónde se encuentre en el código.

## Cómo funciona el scope

Imagina que pierdes algo importante (llaves, dinero, celular), comienzas a buscar este objeto por los lugares **más cercanos** en que te encuentras; si no lo encuentras, buscas en los lugares **más lejanos y así sucesivamente** hasta encontrarlo. Las llaves son las variables y tú eres JavaScript.

Si haces referencia a una variable, el motor de JavaScript buscará su declaración en el **entorno** más cercano, y seguirá buscando en entornos más lejanos hasta llegar a la línea de código que la **variable esté declarada**, pero no en viceversa. A este proceso se lo denomina **cadena de scope** *(scope chaining)*.

##  Cuáles son los tipos de *scope*

Existen dos tipos de *scope:* 

* Global
* Local

El *scope* local se divide en:

* Scope de función
* Scope de bloque

### Representación de los tipos de scope

El código que manejaremos será el siguiente: 

```js
var saludo = "Hola"

function scopes(){
  if (true){
    console.log(saludo)
  }
}

scopes()
```

En la imagen siguiente, el entorno más cercano para la variable `saludo` cuando es invocada se encuentra en el siguiente orden:

1. Scope de bloque
2. Scope de función
3. Scope global

Este es un ejemplo del recorrido que sigue JavaScript hasta encontrar la variable referenciada.

![Representación de los tipos de scope](https://static.platzi.com/media/articlases/Images/scope_closure01.PNG)

### Qué es un bloque en JavaScript

Un bloque es toda porción de código que está encerrada entre llaves `{}`. Estos pueden ser los bloques: 

* función: `function() { /* Bloque */ }`
* if: `if() { /* Bloque */ }`
* else if: `else if() { /* Bloque */ }`
* else: `else { /* Bloque */ }`
* while: `while() { /* Bloque */ }`
* for: `for() { /* Bloque */ }`
* switch: `switch() { /* Bloque */ }`

## Qué es el scope global

El *scope* global es el entorno donde las variables globales pueden ser **accedidas desde cualquier lugar** de nuestro programa.

En el siguiente ejemplo, mira el código y piensa qué mostrará en consola. Una vez tengas las respuestas, ejecútalo en la terminal. ¿Qué sucedió?

```js
var nombre = "JavaScript"

function saludar(){
    console.log("Hola " + nombre)
}

saludar()
```

Con este ejemplo podemos concluir que, la función `saludar` tiene acceso a la variable `nombre`. Porque la variable `nombre` está en un **scope global**.

Entonces, una variable global puede ser accedida en cualquier lugar, porque el *scope* global es el último entorno en el que JavaScript busca una variable. 

## Qué es el *scope* local

El *scope* local es el entorno donde las variables locales solo se pueden acceder desde una **función o bloque** del programa.

Observa el siguiente código y piensa cuál será el resultado.

```js
function saludo() {
  let nombre = "Andres"
  console.log(nombre)
}

saludo()
console.log(nombre)
```

Primeramente, al invocarse la función `saludo` imprimirá `"Andres"` en la terminal, pero inmediatamente después, existirá un **error de referencia**.

```js
saludo() // "Andres"
console.log(nombre) // ReferenceError: nombre is not defined
```

Esto sucede porque la variable `nombre` tiene un *scope* local, por lo que solo puede acceder dentro del bloque.

En el *scope* global, la variable `nombre` no existe. Por esto, el scope global **no tiene acceso** a las variables locales del scope local. Esto se repite por cada nivel de scope.

## Aprende sobre el concepto *closure*

El *closure* es una función que **recuerda el entorno en el que fue creada**. Esto significa que una función puede acceder a las variables de una función padre, incluso después de que esta haya sido ejecutada.

Si quieres saber más sobre este tema, continúa con la clase de **[Qué es *Closure*](https://platzi.com/clases/10266-javascript/70373-que-es-closure/)**.

***Contribución creada por:** Andrés Guano (Associate).*
