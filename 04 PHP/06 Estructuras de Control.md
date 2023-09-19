# Estructuras de Control

PHP dispone de sentencias que permiten alterar el flujo de ejecución similares a las de JAVA: **if**, **switch**, **while**, **do-while**, **for**.

## If / If else

``` php
if($num == 0) {
    echo "El número es cero.";
}
```

``` php
if ($a < $b) {
    echo "a es menor que b";
} else if ($a > $b) {
    echo "a es mayor que b";
} else {
    echo "a es igual a b";
}
```

---
<br>


## Operador Ternario

Es una **manera abreviada** de la estructura 'if else'.

``` php
$precio = 199.5;
$descuento = 15;

$precioFinal = ($descuento > 0) ? $precio-$precio*$descuento/100 : $precio;
```

---
<br>


## Switch

``` php
switch ($a) {
    case 0:
    case 1: echo 'a vale de 0-1';
        break;
    default: echo "a no vale de 0-1";
}
```

---
<br>


## While / Do-while

``` php
$a = 1;

while ($a < 8) {
    $a += 3;
}

echo $a;
```

``` php
$a = 5;

do {
    $a -= 3;
} while ($a > 10);

echo $a;
```

---
<br>


## For

``` php
for ($a=0; $a<10; $a++) {
    echo $a;
    echo "<br>";
}
```

---