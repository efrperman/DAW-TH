# Introducción a PHP

## Importante de cara al curso

En este curso de PHP, es esencial seguir algunas convenciones y buenas prácticas para asegurar la legibilidad y el mantenimiento del código:

- Los nombres de **variables**, **funciones**, **métodos** y **clases** deben estar en **inglés**.
- Los nombres de los **archivos** y **directorios** también deben estar en **inglés**.
- Cada archivo PHP debe incluir comentarios **PHPDoc** con, al menos, las etiquetas @**autor** y @**version**.
- Cada **clase** y **método** también debe incluir comentarios **PHPDoc**.
- En caso de tener **elementos complejos**, asegúrate de proporcionar **comentarios** adecuados.

## PHP: Un vistazo rápido

- Es un lenguaje de programación de **propósito general** que ha encontrado un uso extendido en el **desarrollo web**.
- Es un lenguaje **interpretado**.
- Su **sintaxis** es similar a la de lenguajes como **C** y **JAVA**.
- Para obtener información detallada sobre PHP, consulta la [documentación oficial](https://www.php.net/docs.php).


## Integración de PHP en HTML

Los `archivos.php` se denominan ***scripts*** y pueden estar compuestos por:

- Solo **HTML**. 
- Solo **PHP**.
- **PHP** que además genere **HTML**.
- Una **combinación** de todo lo anterior.

<br>

Para **evitar** el **almacenamiento en caché** de las páginas, puedes: 

- Agregar estas etiquetas meta al `<head>`:
  ``` html
    <meta http-equiv="Expires" content="0">
    <meta http-equiv="Last-Modified" content="0">
    <meta http-equiv="Cache-Control" content="no-cache, mustrevalidate">
    <meta http-equiv="Pragma" content="no-cache">
  ```

- Borrar la caché del navegador (`CTRL`+ `SHIFT`+ `SUPR` en Firefox).

<br>

Puedes **imprimir** contenido en PHP de estas tres formas:

- `echo expression`
- `print expression`
- `<?= $nameOfVariable ?>`, que es lo mismo que `<?php echo $nameOfVariable ?>`.

> No utilizamos paréntesis con `echo` y `print` puesto que **no** son **funciones**.

<br>

Por último, te encuenta que: 

- Las expresiones PHP **terminan** siempre con **`';'`**.
- Para **concatenar** cadenas, se utiliza el operador **`'.'`**.
- Se recomienda usar comillas simples **`''`** para declarar **cadenas**.
- Puedes utilizar la **secuencia** de **escape** **`'\'`** para anular un símbolo reservado.
- Debes de utilizar siempre **rutas absoulutas**.


## Comentarios

Con los comentarios podrás **documentar** y hacer más **comprensible** tu código. En PHP, tienes tres tipos:

- Comentarios en **una línea**:
``` php
// Este es un comentario en una línea.
```
<br>

- Comentarios **varias líneas**:
``` php
/*
 * Este es un comentario
 * en varias líneas.
*/
```

> Ten en cuenta que los comentarios PHP **no aparecerán** en el HTML final, mientras que los comentarios HTML (`<!-- ... -->`), **sí**.

<br>

- Comentarios **PHPDoc**:
``` php
<?php
/**
 * File Name: introduction.php
 *
 * Description: Brief introduction to PHP.
 *
 * @author Efraín Peris Manzano <efrperman@alu.edu.gva.es>
 * @version 1.0
 */
?>
```

Se recomienda agregar comentarios PHPDoc mientras programas tu código en:

- cada `archivo.php`
- includes
- clases e interfaces
- propiedades de las clases
- rasgos (traits)
- funciones y métodos
- constantes 
 
Para generar la documentación automáticamente, puedes utilizar [phpDocumentor](https://phpdoc.org/) (consultar las etiquetas disponibles [aquí](https://docs.phpdoc.org/guide/references/phpdoc/tags/index.html)). Primero, **incluye** el archivo ['phpDocumentor.phar'](https://github.com/phpDocumentor/phpDocumentor/releases) en el directorio del **proyecto**. Y luego, ejecuta el siguiente comando:

``` bash
    php 'phpDocumentor.phar' -d . -t 'docs/api'.  
```
> Esto creará dentro del proyecto, la ruta `docs/api` generando la documentación en HTML.


## Inclusión de ficheros externos

PHP te permite **reutilizar código** mediante la inclusión de archivos externos, para ello contamos con las siguientes instrucciones:

- `include`: Si no se encuentra el archivo, emite una advertencia y continúa la ejecución.
- `require`: Si no se encuentra el archivo, produce un error y detiene la ejecución.
- `include_once` y `require_once`: Aseguran que el código se agregue solo una vez.

<br>

Ejemplo de **inclusión** de un archivo haciendo uso de `require_once` y una `ruta absoluta`:

```php
<?php require_once __DIR__ . '/inc/footer.inc.php'; ?>