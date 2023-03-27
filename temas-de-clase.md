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


