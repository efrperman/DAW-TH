# Tipos de Datos en JS

| Tipo       | Descripción                                                   | Ejemplo             |
| ---------- | ------------------------------------------------------------- | ------------------- |
| Number     | Número (entero o decimal)                                     | `42`, `3.14`        |
| String     | Cadena de caracteres delimitada por comillas simples o dobles | `'Hola'`, `"Mundo"` |
| Boolean    | Verdadero o falso                                             | `true`, `false`     |
| BigInt     | Número entero de precisión arbitraria                         | `123456789n`        |
| Symbol     | Valor único e inmutable                                       | `Symbol('foo')`     |
| Undefined  | Variable declarada pero no inicializada                       | `undefined`         |
| Null       | Valor nulo, denota la ausencia de valor                       | `null`              |

---
<br>

Para saber de **qué tipo** es el valor de una **variable** tenemos el operador **`typeof`**. Por ejemplo:

```javascript
typeof 3        // devuelve "number"
typeof 'Hola'   // devuelve "string"
```

---
<br>

## Number

- Cuando querramos incluir un decimal, usaremos el punto `'.'`.
- Utiliza `NaN` (Not a Number): el resultado de la operación no puede ser convertido a un número (por ejemplo, `'Hola' * 2`).
-  También existen los valores especiales `Infinity` y `-Infinity` (por ejemplo, `23 / 0` no produce un error, sino que devuelve `Infinity`).

### Operadores utilizados

| Tipo                       | Operadores                     |
|----------------------------|--------------------------------|
| Operadores aritméticos     | `+`, `-`, `*`, `/`, `%`        |
| Operadores unarios         | `++`, `--`                     |
| Operadores de asignación.  | `+=`, `-=`, `*=`, `/=`, `%=`   |
---

### Algunos métodos útiles para trabajar con números:

- `.toFixed(num)`: redondea el número a la cantidad de decimales indicada. Por ejemplo, `23.2376.toFixed(2)` devuelve `23.24`.
- `.toLocaleString()`: devuelve el número en formato local. Por ejemplo, `23.76.toLocaleString()` devuelve `"23,76"` (reemplaza el punto decimal por una coma).

### Casting

Podemos forzar la conversión de una cadena de texto a número utilizando la función `Number(valor)`. Por ejemplo, `Number("23.12")` devuelve `23.12`.

Otras funciones útiles son:

- `isNaN(valor)`: nos dice si el valor pasado es un número (devuelve `false`) o no (devuelve `true`).
- `isFinite(valor)`: devuelve `true` si el valor es finito (no es `Infinity` ni `-Infinity`).

- `parseInt(valor)`: convierte el valor pasado a un número entero. Siempre que comience por un número, la conversión se podrá hacer. Por ejemplo:
  - `parseInt(3.65)` devuelve `3`.
  - `parseInt('3.65')` devuelve `3`.
  - `parseInt('3 manzanas')` devuelve `3`.
  - `parseInt('tres')` devuelve `NaN`.

- `parseFloat(valor)`: similar a `parseInt`, pero conserva los decimales.















> Estos son los **valores** que puede tomar un '**boolean**':

| Verdadero                                                                | Falso                                 |
| ------------------------------------------------------------------------ | ------------------------------------- |
| `true` o `TRUE`                                                          | `false` o `FALSE`                     |
| Cualquier número entero o decimal, positivo o negativo distinto de cero. | `0`, `-0`, `0.0`, `-0.0`, `'0'`, `''` |
| Cualquier cadena que no sea cero o cadena vacía.                         | `null`                                |