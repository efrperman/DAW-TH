# Operadores

Los **operadores** se se utilizan junto a variables creando así **expresiones**. Son similares a los de Java:

| Tipo de operación       | Operadores PHP                                                  |
| ----------------------- | --------------------------------------------------------------- |
| Asignación              | =,   +=,   -=,   *=,   /=,   %=                                 |
| Aritmética              | +,   -,   *,   /,   %,   **,   ++,   --                         |
| Comparación             | >,   <,   >=,   <=,   ==,   !=,   <>,   !==,   ===,   <=>,   ?? |
| Comparación booleana    | &&,   \|\|,   !,   and,   or,   xor                             |
| Sobre bits (integer)    | &,   \|,   ^(xor),   ~(not),   <<,   >>                         |
| Concatenación (strings) | .,   .=                                                         |


## Nave Espacial (`<=>`) y Fusión de Null (`??`)

> Funcionan a partir de PHP7.

``` php
$a <=> $b

// devuelve '-1' si '$a' es el menor.
// devuelve '0' si son iguales. 
// devuelve '1' si '&b' es el menor. 
```

``` php
$a ?? $b ?? $c  // se pueden usar tantas variables como se desee.

// devuelve el primer operando (desde la izquierda) que no sea 'null'.
```

---