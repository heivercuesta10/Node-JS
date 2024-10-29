# Guia de NodeJS Backend

## Introducción

Ahora con JavaScript puedes crear aplicaciones que corren del lado del servidor gracias a Node.js.


## ¿Qué es Node.js?

Se trata de un entorno de código abierto (open source) multiplataforma que ejecuta el código JavaScript fuera de un navegador. Este entorno de ejecución de JavaScript se orienta a eventos asíncronos (los eventos no dependen de que otros se hayan ejecutado previamente) y permite construir aplicaciones en red escalables, es decir, tiene la capacidad de realizar muchas conexiones de manera simultánea sin que tenga que leer el código línea a línea, ni abrir múltiples procesos.

## ¿Cómo funciona Node.js?

Hasta la aparición de Node.js, JavaScript era un lenguaje que para los desarrolladores funcionaba íntegramente en el front-end, lo que significaba que para codear un back-end, había que utilizar otro lenguaje. ¿Qué solución trae Node.js? Que ahora, todo el stack, se puede codear con un único lenguaje.


## Ventajas de Node.js

Ahora analizaremos algunas de las principales ventajas y desventajas de Node.js, para que puedas evaluar si es la solución adecuada para tus proyectos

1. Rendimiento y escalabilidad
2. Facilidad de aprendizaje
3. Ecosistema de paquetes y comunidad

## Desventajas de Node.js

1. Programación asíncrona y manejo de errores
2. Falta de soporte para la programación multihilo
3. Madurez relativa y cambios en la API


## Referentes estadisticos de NodeJS

Tecnologías de desarrollo stackoverflow:  (https://survey.stackoverflow.co/2023/#most-popular-technologies-webframe)


## Ejemplo de Programación utilizando Framework Express


**EndPoint POST**

*app.js*  

const express = require('express');

const app = express();

const PORT = 3000;


app.use(express.json());


app.post('/', function (req, res) {

         console.log(req.body.name)
    
         console.log(req.body)

         const datos = req.body
    
         res.send(req.body)
    
         res.end();
    
})


app.listen(PORT, function (err) {

    if (err) console.log(err);
    
    console.log("Server listening on PORT", PORT);
    
});


**Nota:** para los endpoint POST, PUT, DELETE, PATCH es importante adicionar la siguiente línea: 

app.use(express.json());


**Ing. Heiver Cuesta Dávila**
