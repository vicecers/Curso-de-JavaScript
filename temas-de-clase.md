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
  
  
  
