<!-- 
    @author:  Efraín Peris Manzano; 
    @version: 1.0 
-->

# MARKDOWN SYNTAX

## 1. Heading

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

### 2. Bold, Italic & Strikethrough

``` markdown
*italic*
**bold**
***bold & italic***
~strikethrough~
```

*italic*

**bold**

***bold & italic***

~~strikethrough~~

--- 
<br>

### 3. Blockquote

``` markdown
> This is a blockquote.
```

> This is a blockquote.

---
<br>

### 4. Lists

``` markdown
Ordered List:

1. Item
2. Item
3. Item
```
1. Item
2. Item
3. Item

<br>

``` markdown
Unordered List:

- Item
- Item
- Item
```
- Item
- Item
- Item

<br>

``` markdown
Nested List:

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

## 5. Link & Image

``` markdown
Link:

[This is a link](https://github.com/efrperman)
```
[This is a link](https://github.com/efrperman)

<br>

``` markdown
Image:

![alternative text](https://miro.medium.com/v2/resize:fit:526/format:webp/1*KyfQrrAxJbBFVfm0eYi6TQ.png)
```

![markdown logo](https://miro.medium.com/v2/resize:fit:526/format:webp/1*KyfQrrAxJbBFVfm0eYi6TQ.png)

---
<br>

## 6. Code

``` markdown
One line code:

`<p>One line code</p>`
```

`<p>One line code</p>`

<br>

``` markdown
Fenced code block:

``` nameOfThelanguage
<main>
    <article>
        <h2>Fenced Code Block<h2>
            <img src="/img/img.png" alt="img">
    </article>    
<main>
```                                          .
```

``` html
<main>
    <article>
        <h2>Fenced Code Block<h2>
            <img src="/img/img.png" alt="img">
    </article>    
<main>
```

---
<br>

## 7. Horizontal Rule & Comment

``` markdown
Horizontal Rule:

---
```

---
<br>

``` markdown
Comment:

<!-- This is a comment --> (it will not be shown)
```

<!-- This is a comment -->

---
<br>

## 8. Table

``` markdown
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

---
<br>
<br>

>The following elements ↓ are not always supported, so equivalent HTML elements may be used instead.

<br>

## 9. Superscript & Subscript

``` markdown
Superscript:

X^2^
```
X<sup>2</sup>

<br>

``` markdown
Subscript:

H~2~O
```
H<sub>2</sub>O

---
<br>

## 10. Footnote

``` markdown
Here's a sentence with a footnote. [^1]
[^1]: This is the footnote.
```

<p>Here's a sentence with a <a href="#footnote-1">footnote</a>.</p>
<ol><li id="footnote-1">This is the footnote.</li></ol>

---
<br>

## 11. Definition List

``` markdown
term
: definition
```

<dl>
  <dt>term</dt>
  <dd>definition</dd>
</dl>

---
<br>

## 12. Task List

``` markdown
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media 
```

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media 

---
<br>

## 13. Emoji

> Click [here](https://github.com/caiyongji/emoji-list) to see the complete list of emojis.

``` markdown
 That is so funny! :joy: 
```

That is so funny! 😂

---
<br>