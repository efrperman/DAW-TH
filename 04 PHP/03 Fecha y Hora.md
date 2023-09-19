# Fecha y Hora

> PHP **no** tiene un **tipo** de **datos concreto** para fechas y horas, sino que se utiliza la marca de tiempo **UNIX** (*segundos que han pasado desde las 00:00:00 del 1/1/1970*).


## Función `time()`

La función `time()` **devuelve** el **instante actual en** formato **UNIX**:

``` php
$start = time();
echo "Página generada en ". time()-$start ." segundos.";
```
---
<br>


## Cambiar la Zona Horaria

Es importante indicar la **zona horaria** cuando el servidor web se encuentra en una distinta a donde se visita la aplicación web.

``` php
date_default_timezone_set('Europe/Madrid');
```

---
<br>


## Función `mktime()`

Si se desea **generar** una **fecha específica** se usa la función `mktime()`:

``` php
// mktime(hora, minutos, segundos, mes, dia, año)
$cumpleanyos = mktime(0,0,0,5,18,1994);
```

---
<br>


## Función `date()`

Para **mostrar** detalles de una **fecha** en formato **UNIX** se usa la función `date()`.

``` php
echo date("l, d M Y", time());
echo date("l, d M Y");  // 'Wednesday, 18 May 1994'
```

En la [documentación](https://www.php.net/manual/es/function.date.php) se pueden consultar todas las opciones de formato.

---