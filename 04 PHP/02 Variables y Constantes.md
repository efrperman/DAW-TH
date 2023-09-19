# Variables y Constantes

## Nombres de Variables

- Los nombres de variables deben comenzar con **`$`** seguido de una letra o el símbolo **`_`**.
- **No** se recomienda usar caracteres **no ingleses** y **símbolos**.
- Los nombres de variables son **case sensitive**, lo que significa que `$nombre` es diferente de `$Nombre`.

Ejemplos válidos: 

``` php
$i;
$edad;
$nombreCalle, 
$cantidad_pelotas;
$_piso;
$_3tipos;
$primerApellido; $apellido2;
```
---
<br>

## Tipado Débil

PHP es un lenguaje de programación **débilmente tipado**, lo que implica:

- No es necesario **declarar** las **variables** previamente; simplemente se les asigna un valor para comenzar a usarlas.
- En cualquier momento se puede **cambiar** el **tipo** de **dato** que almacena una variable.

---
<br>

## Asignación de Valores a Variables

Se utiliza el operador **`=`** para asignar valores a las variables:

``` php
$season = 5;
$name = "Morty";
$male = true;
```
---
<br>


## Eliminación de Variables

Puedes **eliminar variables** (no solo su contenido) utilizando la función `unset`:

``` php
unset($season);
unset($name, $male);
```
---
<br>


## Casting

Si en una operación intervienen variables de **distinto tipo**, PHP intentará convertirlas a un tipo común (**casting**).

``` php
$cantidad = 3;
$precio = 1.6;
$total = $cantidad * $precio;

$total = $cantidad * (int)$precio; // casting forzado

echo "El precio final es ". $precio ." €";
```

---
<br>


## Constantes

Los **nombres** de las constantes irán siempre en **mayúscula**.

Podemos crearlas de dos maneras:

``` php
define("PI", 3.141592);

const PI = 3.141592; //a partir de PHP 5.3
```

---