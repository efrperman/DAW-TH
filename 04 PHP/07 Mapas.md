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


``` php
$chars = ['Ricky', 'Morty'];
```

> Si no lo indicamos en la definición, se asignará a la **clave** un valor **númerico** comenzando en **'0'**.

## Modificación

``` php
$chars[1] = ['Rocky']; // cambiamos 'Morty' por 'Rocky' 
```


## Adición

``` php
$chars[] = 'Luke';  // se le asigna la clave siguiente: 3
```

Se debe tener cuidado con esta práctica si se indica una clave mayor que la última posición del array:

``` php
$chars[6] = 'Leia';  // las claves 4 y 5 no existen
$chars[] = 'Yoda';   // se le asigna la clave siguiente: 7
```

## Eliminación

> Si la variable ya contenía algun dato, deberá eliminarse primero para poder crear un mapa en ella.

``` php
$show = 'Futurama';
uset($show);

$show[] = 'Braking Bad';
$show[] = 'Better call Saul';
```

---
<br>


<!-- ## Claves de tipo String

### Declaración
``` php
$teachers = ['name' => 'Jacinto', 
             'age' => 45,
             'gender' => 'male'
];
```

``` php
$teachers['name'] = 'Jacinto';
$teachers['age'] = 45;
$teachers['gender'] = 'male';
```

### Casting

> ¡Ciudado! Al indicar una clave, PHP intentará castearla a integer.

``` php
$array = [1 => 'a', 
        '1' => 'b',
        1.5 => 'c',
        true => 'd'
];
``` -->

<!-- Páginas 55-61 -->