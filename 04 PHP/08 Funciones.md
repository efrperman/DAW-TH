# Funciones

## Predefinidas
PHP dispone de infinidad de **funciones predefinidas** (referencia funciones). Es importante consultar la [documentación](https://www.php.net/manual/es/funcref.php) para ver cómo funciona una función y cómo
se realiza la llamada a la función.

### Para Variables [🛈](https://www.php.net/manual/es/ref.var.php)

| Función    | Definición                                              |
|------------|---------------------------------------------------------|
| **empty**      | Comprueba si la variable está vacía (valor no vacío distinto de cero). |
| **isset**      | Comprueba si una (o más variables) existe y no es null. |
| **unset**      | Destruye una (o más variables).                         |
| **is_int**     | Comprueba si una variable es integer.                   |
| **is_float**   | Comprueba si una variable es float.                     |
| **is_string**  | Comprueba si una variable es string.                    |
| **is_array**   | Comprueba si una variable es un array.                  |
| **is_object**  | Comprueba si una variable es un objeto.                 |
| **is_null**    | Comprueba si una variable es null.                      |

### Matemáticas [🛈](https://www.php.net/manual/es/ref.math.php)

| Función    | Definición                                              |
|------------|---------------------------------------------------------|
| **pow**        | Calcula la potencia (un número elevado a otro).         |
| **sqrt**       | Calcula la raíz cuadrada de un número.                  |
| **round**      | Redondea un decimal dependiendo del dígito: 0 a 4 si hacia abajo, 5 a 9 hacia arriba. |
| **ceil**       | Redondea un decimal hacia arriba.                       |
| **floor**      | Redondea un decimal hacia abajo.                        |
| **decbin**     | Convierte un número decimal a binario en forma de string. |
| **bindec**     | Convierte un número binario en forma de string a decimal. |
| **max**        | Encuentra el valor más alto entre las variables indicadas (también con array de integer). |
| **min**        | Encuentra el valor más bajo entre las variables indicadas (también con array de integer). |
| **sin**, **cos**, **tan**... | Funciones trigonométricas.                             |
| **rand**       | Genera un número aleatorio.                             |
| **mt_rand**    | Genera un número aleatorio de una mejor manera que la anterior. |

### Para Strings [🛈](https://www.php.net/manual/es/ref.strings.php)

| Función        | Definición                                                                 |
|----------------|----------------------------------------------------------------------------|
| **strlen**         | Obtiene la longitud de una cadena.                                         |
| **substr**         | Devuelve una parte de una cadena.                                          |
| **str_replace**    | Sustituye parte de una cadena por otra cadena indicada.                     |
| **strtolower**     | Transforma una cadena a minúsculas.                                        |
| **strtoupper**     | Transforma una cadena a mayúsculas.                                        |
| **trim**           | Elimina espacios al principio y al final.                                  |
| **explode**        | Divide un string en varios strings almacenándolos en un array.             |
| **implode**        | Une elementos de un array en un string.                                    |
| **strip_tags**     | Elimina etiquetas HTML.                                                    |
| **strcmp**         | Comparación segura de dos cadenas.                                         |
| **strcasecmp**     | Comparación segura de dos cadenas convirtiéndolas primero a minúsculas.    |

### Para Mapas [🛈](https://www.php.net/manual/es/ref.array.php)

| Función            | Definición                                                                         |
|--------------------|------------------------------------------------------------------------------------|
| **count**              | Cuenta los elementos de un array.                                                 |
| **array_values**       | Devuelve un array con los valores del mismo.                                      |
| **array_keys**         | Devuelve un array con las claves del mismo.                                       |
| **array_key_exists**   | Comprueba si una clave existe en un array.                                        |
| **array_flip**         | Intercambia las claves y los valores de un array. Los valores pasarán a ser las claves y viceversa. |
| **array_pop**          | Extrae el último elemento de un array.                                            |
| **array_push**         | Añade uno o más elementos al final de un array.                                   |
| **array_shift**        | Extrae el primer elemento del array. Si es numérico recalcula las claves para que empiecen en cero. |
| **array_unshift**      | Añade uno o más elementos al inicio de un array.                                  |
| **array_reverse**      | Devuelve un array con los elementos en orden inverso al array indicado.          |
| **array_merge**        | Combina dos o más arrays.                                                         |
| **in_array**           | Comprueba si un valor existe en un array.                                         |
| **sort**               | Ordena un array.                                                                  |

--- 
<br>

## Propias

Para definir funciones propias se utiliza la palabra reservada **function**:

``` php
function greeting () {
    echo 'Hola ¿Qué tal va?';
}
```
Para usar una función, esta debe estar definida en el mismo script desde donde se realiza la llamada, ya sea **directamente** o a través de **include** o **require**:

``` php
greeting();
```

A la hora de definir y usar funciones propias existen una serie de
características que difieren de otros lenguajes de programación.


### Paso de argumentos por valor

Al definir una función se pueden indicar los argumentos que necesitará.
Lo más habitual es realizar el paso por valor, lo cual significa que se realizará una copia
de la variable para usarla dentro de la función:

``` php
function addition($number1, $number2) {
    echo $number1 . '+' . $number2 . '=' . $number1+$number2;
}

addition(14, 27);
```

### Paso de argumentos por referencia

Al pasar parámetros por referencia no se crea una copia de la variable y si se modifica
dentro de la función los cambios se mantendrán fuera de esta:

``` php
$number = 6;

function increment(&$number, $quantity) {
    $number += quantity;
}

echo 'Número antes de la llamada: ' . $number . '<br>'
increment($number, 25);
echo 'Número después de la llamada: ' . $number . '<br>'
```

### Argumentos con valor por defecto/opcionales

Se puede indicar un **valor por defecto** a los argumentos, estos argumentos además
serán **opcionales**. Los argumentos con valor por defecto deben ser los últimos:

``` php
function finalPrice($price, $vat=21, $discount=0) {
    echo 'Precio sin IVA: ' . $price . '€<br>';
    if ($discount != 0) {
        echo 'Descuento (' . $discount . '%): ' . $price*$discount/100 . '€<br>';
        $price -= $price*$discount/100;
    }
    echo 'IVA ('. $vat . '%): ' . $price*$vat/100 . '€<br>';
    echo 'Precio Final: ' . $precio + $price*$vat/100 . '€<br>';
}

finalPrice(150);
finalPrice(150, 10);
finalPrice(150, 10, 50);
```

### Argumentos con nombre

Desde **PHP 8** se pueden realizar llamadas a funciones con el **nombre del argumento**:

``` php
function finalPrice($price, $vat=21, $discount=0) {
}

finalPrice(price:150, discount:15);
finalPrice(93, discount:7, vat:10);
finalPrice(discount:15, price:199, vat:21);
```

Si se usan argumentos con y sin nombre en la misma llamada, los argumentos con
nombre deben ser los últimos.

### Cantidad de argumentos

Aunque en la definición de la función se indiquen unos argumentos PHP al realizar la
llamada a la función **se pueden indicar más argumentos** de los definidos, **nunca menos**:

``` php
function test() {
}

test();
test(1, 2, 3, 4);

function addition($number1, $number2) {
}

addition(); // error
addition(14, 27);
addition(14, 27, 52);
```

Aunque se indiquen más argumentos, si en la definición de la función no se realiza
ninguna acción con ellos no habrá ningún error:

``` php
function addition($number1, $number2) {
    echo $number1 . '+' . $number2 . '=' . $number1+$number2;
}

addition(14, 27);
addition(14, 27, 52, 8, 14);
```

Existen dos maneras de acceder a los argumentos no indicados en la definición:

``` php
// Mediante las funciones: `func_num_args` y `func_get_arg`:

function addition() {
    $addition = 0;
    for ($i = 0; $i < func_num_args(); $i++>) {
        $addition += func_get_args($i);
    }
    echo 'La suma de los números es: ' . $addition;
}

addition(14, 27);
addition(14, 27, 52, 8, 14);
```

``` php
// Creando un `array` (PHP > 5.6).

function addition(... $numbers) {
    $addition = 0;
    foreach ($numbers as $number) {
        $addition += $number;
    }
    echo 'La suma de los números es: ' . $addition;
}

addition(14, 27);
addition(14, 27, 52, 8, 14);
```
Mediante la notación de tres puntos `…` se pueden definir parámetros concretos primero
y al final dejar la opción de añadir más parámetros en la llamada:

``` php
function operation ($operation, ...$number) {
}

echo operation('suma', 1, 6, 15, 5);
```

Los tres puntos `…` también permiten separar un array en diferentes variables cuando se
pasa el array como argumento a una función.

``` php
function addition(...$numbers) {
}

$numbers = [1, 2, 3, 4, 5];
addition(...$numbers);
```

### Devolver valores

Mediante **return** una función puede devolver un dato al finalizar su llamada:

``` php
function addition(...$numbers) {
    $result = 0;
    foreach ($numbers as $number) {
        $result += $number;
    }
    return $result;
}
```

### Indicar el tipo de dato

Desde PHP 7 se permite indicar el tipo de dato de los argumentos y del valor devuelto.
Si se definen las funciones así PHP se vuelve más estricto.

``` php
function finalPrice(int $price, float $vat=21, int $discount=0: float) {
    $price -= $price*$discount/100;
    $price += $price*$vat/100;
    return $price;    
}
```
--- 
<br>

Cabe **recordar** que cuando PHP usa una variable siempre va a intentar hacer
un **casting** con ella para evitar posibles problemas:

``` php
$number = 6;

function increment($number, $quantity) {
    return $number+$quantity;
}

echo increment('3', 4);
```