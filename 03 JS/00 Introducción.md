# Introducción a JavaScript

Nuestras apps contendrán 3 elementos separados:

- HTML: `public/index.html`
- CSS: `styles/*.css`
- JS: `scripts/*.js`

Las características principales de JS son:

- Es un lenguaje **interpretado**.
- Está **débilmente tipado**.
- Es un lenguaje **orientado** a **objetos**, pero basado en **prototipos**.
- Se ejecuta en el **cliente** (con NodeJS puede en el Servidor).

Ejemplos de uso:

- Cambiar el contenido de una página.
- Cambiar los atributos de un elemento.
- Cambiar la apariencia de algo.
- Validar datos de formularios.
- ...

Por seguridad no podemos:

- Acceder al sistema de ficheros del cliente.
- Capturar datos de un servidor.
- Modificar las preferencias del navegador.
- Enviar e-mails o crear ventanas de forma invisible.
- ...


## Un poco de historia:

JS es una implementación de ECMAScript (el estándar que define sus características).

Nació en 1997 y desde 2012 todos los navegadores soportan al menos la versión ES5.1.

La versión que usaremos nosotros es la **ES6** o **ES2015**:
  - Introdujo mejoras importantes como: clases de objetos, let, for...of, Map, Set, Arrow functions, Promesas, spread, destructuring...
  - A partir de ella, van saliendo nuevas cada año, que introducen cambios pequeños.


## Soporte en los navegadores:

- Los navegadores tardan en adaptarse a las nuevas versiones, por lo que usar una muy moderna puede hacer que no funcionen algunos programas.
- En [Kangax](https://kangax.github.io/compat-table/es6/), podemos ver la compatibilidad de los navegadores con las versiones de JS.
- Con [CanIUse](https://caniuse.com/), podemos buscar la compatibilidad de un elemento concreto de JS, HTML o CSS.
- Los transpiladores (como Babeljs) nos permiten traducir nuestro código a otras versiones.

> En la página de [Babel](https://babeljs.io/) podemos teclear código en ES2015 y ver cómo quedaría una vez transpilado a ES5.

## Herramientas:

**La consola del navegador**

- La consola del navegador (`F12``): nos ayudará a depurar nuestro código.
- En ella vemos los errores, warnings y prints; podremos escribir instrucciones; probar código y depurarlo (poniendo puntos de interrupción, consultando el valor de nuestras variables...).
- Es fundamental dominar la consola: [aquí](https://es.javascript.info/debugging-chrome) tienes un recurso para ello.

**Editores y editores en línea**

- Podríamos escoger cualquiera, pero utilizaremos vscode con SonarLint y Live Server.
- Contamos con estas opciones en línea: [Codesandbox](https://codesandbox.io/), [Fiddle](https://jsfiddle.net/), [Plunker](https://plnkr.co/), [CodePen](https://codepen.io/pen/), etc.


## Incluir JS en una página web:

- **Posible:** Dentro de la etiqueta `<script>`, anidada o en `<head>` o en el `<body>` (para un mayor rendimiento, en el `<body>` o en el `<head>` con los atributos ‘async’ o ‘defer’).

- **Óptimo:** En un *.js aparte que enlazaremos: `<script src="code.js"></script>`.


## Mostrar información:

JS nos permite mostrar al usuario **ventanas modales** para mostrarle o pedirle información:

- `alert(msg)`: Muestra un mensaje y espera a que el usuario presione 'Aceptar'.

- `confirm(msg)`: Muestra un mensaje y los botones 'Aceptar' y 'Cancelar'.

- `prompt(msg)`: Muestra lo mismo que el 'confirm', más un campo de entrada.

---
<br>

### Git / GitHub

Para las entregas de las prácticas, utilizaremos un repositorio de Git que nos permitirá también realizar el control de versiones. Esto se puede gestionar desde la consola o desde VSCode.

### npm

NPM es el gestor de paquetes de Node.js y suele utilizarse en el front-end como gestor de dependencias de la aplicación.Se instalará automáticamente al instalar node.js.

Puedes **instalar** node.js **directamente** desde la terminal:
  
``` bash
sudo apt install nodejs
npm --v     // verifica la versión instalada
```

Obtener una **versión específica**:

 ``` bash
curl -sL https://deb.nodesource.com/setup_X.y | sudo -E bash - 
sudo apt-get install -y nodejs  // reemplaza X por la versión deseada
 ```
  
  O **descarga** el **paquete** desde [aquí](https://nodejs.org/es) y descomprímelo:
 
 ``` shell
dpkg -i nombreDelPaquete
 ```