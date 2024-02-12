# Introducion a Node JS

### ¿Qué es Node.js?
Node.js es un entorno de ejecución de JavaScript de código abierto y multiplataforma. Es una herramienta popular utilizada en una amplia variedad de proyectos.
---
### Repasar el uso de JavaScript necesario para usar Node.js:

* **Lexical Structure:**
Los scripts de ECMAScript se escanean de izquierda a derecha y se convierten en una secuencia de elementos de entrada que son segmentos. 
**Los comentarios** se utilizan para agregar consejos, notas, sugerencias o advertencias al código JavaScript, facilitando su lectura y comprensión.

*Forma 1:*
```js
    
//Este es un comentario JavaScript de una línea
 ```
 ---
*Forma 2:*
```js
    /* 
    Este es un comentario JavaScript 
    de
    varias
    líneas */ 
```
---
* **Expressions:** Las expresiones en JavaScript se dividen en dos categorías: Primarias y Expresiones del lado izquierdo:

1. *Ejemplos de expresiones primarias* incluyen palabras clave básicas y expresiones generales en JavaScript, como `class` y `function`.

1. *Ejemplos de expresiones del lado izquierdo* incluyen algunas como `new` y `super`.

---
* **Data Types:** JavaScript es un lenguaje débilmente tipado y dinámico.

*Ejemplos de tipos de datos* incluyen Cadena (`String`), Número (`Number`), Booleano (`Boolean`), `Null`, Objeto (`Object`), Arreglo (`Array`), y Función (`Function`).

* **Classes:** Las clases de JavaScript,fueron introducidas en ECMAScript 2015, mejorando la sintaxis de la herencia basada en prototipos.

*Ejemplo de declaración de clase:*
```js
        class Rectangulo {
          constructor(alto, ancho) {
            this.alto = alto;
            this.ancho = ancho;
          }
        }
```
---
* **Variables:** En JavaScript, las variables se utilizan para almacenar y manipular datos, y se pueden declarar usando `var`, `let` o `const`.

*Ejemplo:*
```js
        let nombre = "Juan";
        const edad = 25;
```
---
* **Functions:** Las funciones en JavaScript son bloques de código reutilizables que realizan tareas específicas.

*Ejemplo:*
```js
    function saludar(nombre) {
        return "¡Hola, " + nombre + "!";
    }
```
---
* **this Operator:** El operador `this` se refiere al objeto al que pertenece en el contexto actual.

* **Arrow Functions:** Las funciones de flecha son una forma concisa de escribir funciones en JavaScript, sin tener su propio valor `this`.

*Ejemplo:*
```js
        const sumar = (a, b) => a + b;
 ```
---
* **Loops:** Los bucles como `for`, `while`, y `do-while` se utilizan para ejecutar un bloque de código varias veces.

*Ejemplo:*
```js
    for (let i = 0; i < 5; i++) {
        console.log(i);
    }
```

* **Scopes:** El ámbito en JavaScript se refiere a la accesibilidad y visibilidad de las variables.La palabra clave `let` y `const` (introducida en ES6) afecta al ámbito de bloque.
---
* **Arrays:** Los arreglos en JavaScript son objetos que almacenan múltiples valores en una sola variable.

*Ejemplo:*
```js
let frutas = ["manzana", "banana", "naranja"];
```
---

* **Template Literals:** Los literales de plantilla permiten incrustar expresiones dentro de cadenas, facilitando la concatenación de variables y expresiones.

*Ejemplo:*
```js
    let nombre = "Juan";
    let mensaje = `Hola, ${nombre}!`;
```
---
* **Strict Mode:** El modo estricto (`"use strict";`) es una característica de JavaScript que ayuda a detectar y evitar errores comunes.
---
* **ECMAScript 2015 (ES6) y posteriores:** ES6 introdujo nuevas características como clases, funciones de flecha, `let` y `const`, desestructuración, módulos, etc., mejorando significativamente JavaScript.
---

## **Programación Asíncrona y Funciones de Retorno (Callbacks):**
La programación asíncrona en JavaScript permite ejecutar tareas sin bloquear la ejecución del programa.
      - 
*Ejemplo de callback:*
```js
    function operacionAsincrona(callback) {
        // Realizar operación asíncrona
          setTimeout(() => {
            callback();
          }, 1000);
    }

    operacionAsincrona(() => {
        console.log("Operación completada");
    });
 ```
---

* **Temporizadores (Timers):** Los temporizadores en JavaScript, como `setTimeout` y `setInterval`, permiten ejecutar funciones después de un cierto período de tiempo.

*Ejemplo:*
```js
    setTimeout(() => {
        console.log("¡Pasó un segundo!");
    }, 1000);
```
---

* **Promesas (Promises):** Las promesas son objetos que representan el resultado eventual (éxito o fallo) de una operación asíncrona.

*Ejemplo:*
```js
    const promesa = new Promise((resolve, reject) => {
        // Realizar operación asíncrona
        setTimeout(() => {
        resolve("Operación exitosa");
        // O reject("Operación fallida");
        }, 1000);
    });

    promesa.then((resultado) => {
        console.log(resultado);
        }).catch((error) => {
        console.error(error);
    });
```
---
* **Async y Await:** `async` y `await` simplifican la programación asíncrona.
 
*Ejemplo:*
```js
    async function operacionAsincrona() {
        try {
        let resultado = await promesa;
            console.log(resultado);
        } catch (error) {
            console.error(error);
        }
    }

    operacionAsincrona();
```
---

* **Cierres (Closures):**Los cierres son funciones que tienen acceso a las variables de su ámbito exterior,incluso después de que la función exterior haya terminado de ejecutarse.

*Ejemplo:*
```js
    function contador() {
        let count = 0;
        return function() {
        count++;
        console.log(count);
        };
    }

    let incrementar = contador();
    incrementar(); // 1
    incrementar(); // 2
```
---

* **El Bucle de Eventos (`Event Loop`):** El Event Loop es parte del modelo de concurrencia de JavaScript, que permite la ejecución eficiente de código asíncrono, manejando la cola de eventos y la pila de llamadas.

---
**Documentación:**

[Node.js Introduction](https://nodejs.org/en/learn/getting-started/introduction-to-nodejs)
