<!-- 
    @author:  Efraín Peris Manzano; 
    @version: 1.1 
-->

# SINTAXIS DE MARKDOWN

## 1. Encabezados

``` markdown
# h1
## h2
### h3
#### h4
##### h5
###### h6
```

# h1
## h2
### h3
#### h4
##### h5
###### h6
---
<br>

### 2. Negrita, Cursiva & Tachado

``` markdown
*cursiva*
**negrita**
***negrita & cursiva***
~tachado~
```

*cursiva*

**negrita**

***negrita & cursiva***

~~tachado~~

--- 
<br>

### 3. Citas

``` markdown
> Esto es una cita.
```

> Esto es una cita.

---
<br>

### 4. Listas

``` markdown
Lista Ordenada:

1. Item
2. Item
3. Item
```
1. Item
2. Item
3. Item

<br>

``` markdown
Lista Desordenada:

- Item
- Item
- Item
```
- Item
- Item
- Item

<br>

``` markdown
Lista Anidada:

1. Item
    1. Subitem
        - Subitem
        1. Subitem
    - Subitem
- Item
    1. Subitem
    2. Subitem
    - Subitem
```

1. Item
    1. Subitem
        - Subitem
        1. Subitem
    - Subitem
- Item
    1. Subitem
    2. Subitem
    - Subitem
---
<br>

## 5. Enlaces & Imágenes

``` markdown
Enlace:

[Esto es un enlace](https://github.com/efrperman)
```
[Esto es un enlace](https://github.com/efrperman)

<br>

``` markdown
Imágen:

![texto alternativo](https://miro.medium.com/v2/resize:fit:526/format:webp/1*KyfQrrAxJbBFVfm0eYi6TQ.png)
```

![texto alternativo](https://miro.medium.com/v2/resize:fit:526/format:webp/1*KyfQrrAxJbBFVfm0eYi6TQ.png)

---
<br>

## 6. Líneas y Bloques de Código

> Pincha [aquí](https://github.com/jincheng9/markdown_supported_languages) para ver la lista completa de lenguages soportados.

``` markdown
Línea única de código:

`<p>One line code</p>`
```

`<p>One line code</p>`

<br>

``` markdown
Bloque de código cercado:

``` nombreDelLenguaje
<main>
    <article>
        <h2><h2>
            <img src="/img/img.png" alt="img">
    </article>    
<main>
```                                          .
```

``` html
<main>
    <article>
        <h2>Bloque de código cercado<h2>
            <img src="/img/img.png" alt="img">
    </article>    
<main>
```

---
<br>

## 7. Saltos de Línea & Separadores
``` markdown
Salto de línea:

linea 1
linea 2
linea 3

linea a

linea b

linea c
```

linea 1
linea 2
linea 3

linea a

linea b

linea c

<br>

``` markdown
Separador:

---
```

---
<br>

## 8. Carácter de Escape & Comentarios
``` markdown
Carácter de Escape ('\'):

\# h1

\*cursiva*
```

\# h1

\*cursiva*

<br>

``` markdown
Comentario:

<!-- Esto es un comentario --> (no será visible)
```

<!-- Esto es un comentario -->

---
<br>

## 9. Tablas

``` markdown
| Sintaxis    | Descripción |
| ----------- | ----------- |
| Encabezado  | Título      |
| Párrafo     | Texto       |
```
| Sintaxis    | Descripción |
| ----------- | ----------- |
| Encabezado  | Título      |
| Párrafo     | Texto       |

---
<br>
<br>

> Los elementos de abajo ↓ no están siempre soportados, por lo que pueden **sustituirse** por sus equivalentes en HTML.

<br>

## 10. Superíndices & Subíndices

``` markdown
Superíndice:

X^2^
```
X<sup>2</sup>

<br>

``` markdown
Subíndice:

H~2~O
```
H<sub>2</sub>O

---
<br>

## 12. Notas a Pie de Página

``` markdown
Esta es una frase con una nota. [^1]
[^1]: Esta es la nota.
```

<p>Esta es una frase con una <a href="#nota">nota</a>.</p>
<ol><li id="nota">Esta es la nota.</li></ol>

---
<br>

## 13. Listas de Definición

``` markdown
término
: definición
```

<dl>
  <dt>término</dt>
  <dd>definición</dd>
</dl>

---
<br>

## 14. Listas de Tareas

``` markdown
- [x] Escribir la descripción
- [x] Actualizar la web
- [ ] Contactar al cliente
```

- [x] Escribir la descripción
- [x] Actualizar la web
- [ ] Contactar al cliente 

---
<br>

## 15. Emojis y Resaltado de Texto

> Pincha [aquí](https://github.com/caiyongji/emoji-list) para ver la lista completa de emojis.

``` markdown
Emoji:

 ¡Qué divertido! :joy: 
```

¡Qué divertido! 😂

<br>

``` markdown
Resaltado de Texto:

Quiero resaltar ==estas palabras==. 
```
Quiero resaltar ==estas palabras==. 

---
<br>