El *closure* es una función que **recuerda el entorno en el que fue creada**. Esto significa que una función puede acceder a las variables de una función padre, incluso después de que esta haya sido ejecutada.

## Cómo declarar un *closure*

Para construir un closure necesitaremos los siguientes requisitos:

* Una función dentro de otra función.

```js
function padre() {
    
    function hijo(){
    }
}
```

* Una variable que se encuentre en la función con el *scope* superior, donde la función con *scope* inferior la utilice.

```js
function padre() {
    let numero = 5

    function hijo(){
        numero = numero + 1
        return numero
    }
}
```

* Invocar la función con un *scope* inferior en otro *scope* diferente al que fue escrita. Esto lo podemos hacer retornando la función y asignar la función de *scope* superior a una variable.

```js
function padre() {
    let numero = 5

    function hijo(){
        numero = numero + 1
        return numero
    }
    
    return hijo
}

const closure = padre()
```

De esta manera obtendremos una función (*scope* inferior) que tiene una referencia a la variable que se encontraba en un *scope* superior, que a su vez recordará el contexto en el que fue creada.


## Cómo funciona el ámbito léxico en los *closures*
El ámbito léxico se refiere al alcance de una variable, siguiendo la cadena de *scopes*. Es decir, una variable puede ser accedida desde un nivel inferior hasta uno superior, pero no al contrario.

En el siguiente ejemplo, crearemos una función `contador` que recibirá un parámetro `i` y retornará una función `aumentar` que incrementará el valor de `i`, según su ámbito léxico. Como resultado, obtendremos dos funciones que recordarán el valor de `i` en el contexto donde fueron creadas.

```js
function contador ( i ) {
  let acumulador = i
  function aumentar () {
    console.log(acumulador)
    acumulador = acumulador + 1
  }
  return aumentar
}

const closure = contador(1)
closure() // 1
closure() // 2
closure() // 3

const closure2 = contador(10);
closure2() // 10
closure2() // 11

closure() // 4
```

Podemos asignar la función `contador` a una variable (`closure` y `closure2`). Dependiendo del valor que tenga como parámetro, cada variable cambiará el valor inicial según el ámbito léxico que fue creada la variable `acumulador`, que está vinculada con la función `aumentar`.

## Aprende sobre experiencias al aprender desarrollo web

El desarrollo web es una de las áreas más demandadas en la actualidad en el ámbito del lenguaje JavaScript.

Si quieres saber más sobre este tema, continúa con la clase de **[¿Por qué aprender desarrollo web?](https://platzi.com/clases/10266-javascript/70349-preguntas-a-desarrolladores-senior-por-que-aprende/)**.

***Contribución creada por:** Andrés Guano (Associate).*
