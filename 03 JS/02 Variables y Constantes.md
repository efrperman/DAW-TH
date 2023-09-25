# Variables y Constantes

JavaScript es un lenguaje **débilmente tipado**:

``` javascript
let miVariable;          // Declaro miVariable y como no se asignó un valor, valdrá undefined
miVariable = 'Hola';     // Ahora su valor es 'Hola', por tanto contiene una cadena de texto
miVariable = 34;         // Pero ahora contiene un número
miVariable = [3, 45, 2]; // Y ahora un array
miVariable = undefined;  // Para volver a valer el valor especial undefined
```

## Declaración

**No** neceseitamos **declarar** una **variable** antes de usarla, aunque es recomendable para evitar errores que nos costará depurar. Podemos hacer que se produzca un **error** si no declaramos una variable incluyendo al principio de nuestro código la instrucción `use strict`.

Las variables se declaran con `let` (lo recomendado desde ES2015), aunque también pueden declararse con `var` (con let la variable sólo existe en el bloque en que se declara, mientras que con var la variable existe en toda la función en que se declara):

``` js
if (edad < 18) {
  let textoLet = 'Eres mayor de edad';
  var textoVar = 'Eres mayor de edad';
} else {
  let textoLet = 'Eres menor de edad';
  var textoVar = 'Eres menor de edad';
}
console.log(textoLet);  // mostrará undefined porque fuera del if no existe la variable
console.log(textoVar);  // mostrará la cadena
```

Cualquier variable que no se declara dentro de una función (o si se usa sin declarar) es global. Debemos siempre intentar **NO** usar **variables globales**.

Se recomienda que los nombres de las variables sigan la sintaxis **camelCase** (ej.: miPrimeraVariable).

## Casting 

Como las variables pueden contener cualquier tipo de valor, en las operaciones, JavaScript realiza automáticamente las conversiones necesarias:

- `'4' / 2` devuelve 2 (convierte '4' en 4 y realiza la operación).
- `'23' - null` devuelve 0 (hace 23 - 0).
- `'23' - undefined` devuelve NaN (no puede convertir undefined a nada, así que no puede hacer la operación).
- `'23' * true` devuelve 23 (23 * 1).
- `'23' * 'Hello'` devuelve NaN (no puede convertir 'Hello').
- `23 + 'Hello'` devuelve '23Hello' (+ es el operador de concatenación, así que convierte 23 a '23' y los concatena).
- `23 + '23'` devuelve '2323' (OJO, convierte 23 a '23', no al revés).

> Es importante destacar que en JavaScript, todo son objetos, por lo que todo tiene métodos y propiedades. 

## Constantes

Desde ES2015 también podemos declarar **constantes** con `const`. Se les debe dar un valor al declararlas y si intentamos modificarlo posteriorment se produce un error:

``` js
const PI = 3.14159265359;
```