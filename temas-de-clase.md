# JavaScript fundamentos

### Declaraciones de variables

#### La etiqueta <script>
  - Puerta de entrada al código JavaScript en nuestros proyectos.
  - Vive en el <head> en el <body> de nuestros documentos HTML*.
 
 ```js
 <script>
    console.log("Hola Mundo!!!")
 </script>
```
  - A través de <script> podemos cargar JavaScript externo.
  - Para ello, utilizamos el atributo src y una URL al recurso, ya sea relativo o absoluto.
 ```js
  <script src="..."></script>
  ```
  - Muchas veces encontraremos <scrtipt> en <footer> en lugar de <header>, para asegurarnos de que el DOM está listo antes de acceder a él.    
  
  
 #### Elevado (hoisting)
 - JavaScript es un lenguaje con tipos dinámicos, es decir, podemos asignar y reasignar diferentes tipos a una misma variable (de ahí el nombre: variable).
  
- Para hacerlo tenemos que utilizar dos fases diferentes: declaración e inicialización.
```js
var favorito // Declaracióm
favorito = 66 // Inicialización
favorito = "Juan" // Reasignación
```
    - Cuando creamos declaramos una variable, JavaScript le asigna el tipo _undefined_.
  - Si intentamos referenciar una variable antes de ser declarada, ¿qué crees que ocurrirá?.
  
  ```js
  console.log(nombre) // 🤔
  var nombre = "Juan"
  ```
    - La respuesta es undefined porque JavaScript, al interpretar tu código alza al inicio del programa la declaración de variables (no la inicialización) y las funciones declaradas.
  
   - Esto explica el por qué, por ejemplo, puedes invocar una función antes de declararla.
  
```js
saludar() // "Hola 👋"
function saludar() {
  console.log("Hola 👋")
}
```
### Ámbito y let
 - Hasta ahora hemos creado variables con var. Estas tienen ámbito de función: pueden ser accedidas desde la función donde fueron declaradas (y funciones interiores).
```js
 var nombre = "Juan"
 function saludar() {
    console.log("Hola " + nombre)
}
saludar() // "Hola Juan"
```
 - Sin embargo, si declaramos variables con let (ES2105), tenemos ámbito de bloque, es decir, solo pueden ser accedidas desde el bloque en el que se declararon, o bloques interiores.

 ```js
{
    let nombre = "Juan"
}
console.log(nombre) // nombre is not defined 
```
  - Este ámbito de bloque tiene sus ventajas. Por ejemplo al utilizarlo con estructuras de control y de flujo.
 ```js
  for (let i = 0; i <= 100; i++) {
    console.log(i)
}
console.log(i) // i is not defined
 ```
