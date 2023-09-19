# Ámbito de las Variables

Existen **tres ámbitos** posibles para una variable en PHP: **local** al **script**, **local** a una **función** y **global**.

## Local al Script

Si la variable se crea en el **script**, incluso dentro de una estructura de control, dicha variable se podrá utilizar en cualquier parte del script, salvo dentro de las funciones.

``` php
$i = 100;
$temp = 0;

while ($i!=0) {
$temp += $i--;
$suma = $temp;
}

echo 'variable temp: '. $temp;
echo '<br>';
echo 'La suma de los 100 primeros números: '. $suma;
```

``` php
$nombre = 'Álex';

saludo();

function saludo() {
    echo '¡Hola soy '. $nombre .'!';    // error
}
```

---
<br>


## Local a una función

Si la variable se crea dentro de una **función**, esa variable solo se podrá usar en esa función.

``` php
saludo();

echo $nombre;   // error

function saludo() {
    $nombre = 'Alex';
    echo '¡Hola soy '. $nombre .'!';
}
```

---
<br>


## Global

Si la variable se crea en el **script** fuera de una función, esa variable se podrá usar en las funciones del script si se usa la **palabra reservada** `global``.

``` php
$nombre = 'Álex';

saludo();

function saludo() {
    global $nombre;
    echo '¡Hola soy '. $nombre .'!';
}
```

> Se debe **evitar** siempre el uso de **variables globales**.

---