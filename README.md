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


## Instalación de dependencias

 1. npm init
 2. npm install express

## Configuración Inicial

const express = require('express');

const app = express();

const PORT = 3000;

app.use(express.json());

## Configuración del puerto

app.listen(PORT, function (err) {

    if (err) console.log(err);
    
        console.log("Server listening on PORT", PORT);
        
}); 


## Consideraciones

**Nota:** para los endpoint POST, PUT, DELETE, PATCH es importante adicionar la siguiente línea: 

app.use(express.json());


**EndPoint GET**

Realiza consulta general:

*app.js*  


const express = require('express');

const app = express();

const PORT = 3000;

app.use(express.json());

app.get('/api/consultar', function (req, res) {

    res.send("Consulta de Datos All")
    
    res.end();
    
    })



**EndPoint GET**


Realiza consulta Filtrada:


*app.js*  


app.get('/api/consultar/:id', function (req, res) {

    const dato = req.params.id;
    
    res.send("Vamos a consultar el Dato:" + dato);
    
    res.end();
    
})

    

**EndPoint POST**

*app.js* 


app.post('/api/agregar', function (req, res) {

    const datos = req.body;
    
    console.log(datos);
    
    res.send("Se van a agregar los datos: " + JSON.stringify(datos))
    
    res.end();
    
})


**EndPoint PUT**

*app.js* 

app.put('/api/modificar/:id', function (req,res) {

    const id = req.params.id;
    
    const dato_modificar = req.body
    
    res.send("El dato a buscar es: " + id + " los datos a modificar son : " + JSON.stringify(dato_modificar));
    
    res.end();
    
})


**EndPoint DELETE**

*app.js* 

app.delete('/api/eliminar/:id', function(req,res) {

    let id_buscar = req.params.id;
    
    res.json("El dato a borrar es: " + id_buscar);
    
})


## Ejecutar

node app.js










**Ing. Heiver Cuesta Dávila**
