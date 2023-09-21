# Mapas

## Características
- En PHP, contamos con **mapas** que pueden funcionar como: *arrays*, *listas*, *tablas hash*, *diccionarios*, *pilas*, *colas…*
  
- **No** tienen un **tamaño establecido** pudiéndose añadir y eliminar elementos en cualquier momento.

- Permiten almacenar **pares clave** (índices) y **datos** de **distinto tipo**.

## Tipos

- **Numérico**: todos los índices son **'integers'**.
- **Asociativo**: todos los índices son **'Strings'**.
- **Mixto**: tiene índices de **ambos** tipos.

--- 
<br>

## Definición

> Si no lo indicamos en la definición, se asignará a la **clave** un valor **númerico** comenzando en **'0'**.

``` php
$chars = ['Ricky', 'Morty'];    // en una línea

$chars[] = 'Ricky';             // o en varias
$chars[] = 'Morty';

// en ambos casos 'Rick' es el elemento 0 y 'Morty el 1'
```


``` php
$teachers = ['name' => 'Jacinto',  // en una línea
             'age' => 45,
             'gender' => 'male'
];

$teachers['name'] = 'Jacinto';     // o en varias
$teachers['age'] = 45;
$teachers['gender'] = 'male';
```

<br>

> **¡Ojo!** Siempre que indiquemos una **clave**, PHP intentará **castearla** a **integer**:

``` php
$array = [1 => 'a',     // el índice 1 vale 'a' 
        '1' => 'b',     // ahora vale 'b'
        1.5 => 'c',     // ahora vale 'c'
        true => 'd'     // ahora vale 'd'
];
```

<br>

> Los **arrays mixtos** suelen tener sus datos **duplicados**, a fin de que se pueda acceder a ellos tanto con la clave 'integer' como con la 'string':

``` php
$chars = [0 => 'Rick Sánchez',         // en una línea
          'name' => 'Rick Sánchez',
          1 => 70,
          'age' => 70
];

$chars[0] = 'Rick Sánchez';             // o en varias
$chars['name'] = 'Rick Sánchez';
$chars[1] = 70;                         // las claves numéricas no haría falta añadirlas 
$chars['age'] = 70;
```

<br>

> Debido a que en PHP un elemento de un mapa puede ser de cualquier tipo, para crear **matrices** o **mapas multidimensionales**, deberemos de **incluir** todo entre corchetes **'[]'**:

``` php
$nums = [[1,2,3], [4,5,6], [7,8,9]];

$films = [
        ['title' => 'Matrix', 'year' => 1999],
        ['title' => 'El Hobbit', 'year' => 2018],
        ['title' => 'Men in Black', 'year' => 2022]
];
```

---
<br>

## Modificación

``` php
$chars = ['Ricky', 'Morty'];    // suponiendo haberlo declarado así anteriormente...
$chars[1] = ['Rocky'];          // cambiaría 'Morty' por 'Rocky' 
```

---
<br>

## Adición

``` php
$chars = ['Ricky', 'Rocky'];    // suponiendo haberlo declarado así anteriormente...
$chars[] = 'Luke';              // 'Luke' se asignaría en el próximo índice (el 3)
```


> Se debe tener **cuidado** con esta práctica si se indica una **clave mayor** que la **última posición** del array:

``` php
$chars[6] = 'Leia';             // las claves 4 y 5 no existirían
$chars[] = 'Yoda';              // 'Yoda' se asignarían en el próximo índice (el 7)
```

---
<br>


## Eliminación

> Si la variable ya contenía algun dato, deberá de **eliminarse** primero para poder crearse un mapa:

``` php
$show = 'Futurama';
uset($show);                    // elimina la variable

$show[] = 'Braking Bad';
$show[] = 'Better call Saul';
```

``` php
unset($show[1]);                 // elimina el elemento '1' del mapa
$show = array_values($show);     // volvemos a crear los índices para evitar problemas al recorrerlo
```

> Esta última función **`array_values()`** es solo para evitar los problemas al recorrer **mapas numéricos**.

---
<br>


## Recorrer un Mapa

### Bucle `for` + Función `count()`

> Para recorrer **mapas numéricos**.

``` php
for ($i = 0; $i < count($chars); $i++) {
        echo '<li>'. $chars[$i] .'</li>';
}
```

<br>

### Bucle `foreach`

> Para recorrer **mapas numéricos** y **asociativos**.

``` php
foreach ($chars as $key => $value) {
        echo $key. ' - ' .$value . '<br>';
}
```

---