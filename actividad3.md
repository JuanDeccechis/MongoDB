# Actividad 3

[HOME](./README.md)  

## Ejercicio 1  
Utilizar la misma base de datos de peliculas e insertar varias peliculas con distinto contenido.  

use netflix  
db.movies.insertMany([{"title": "clase3", "year": 2018, "rating": 3, "genre": "3comedia", "description": "3lorem", "actors": ["a31", "a33", "a333"], "country": "3uruguay", "income": 3000, "duration": 3}, {"title": "rocky3", "year": 2018, "rating": 3.6, "genre": "31accion", "description": "31lorem", "actors": ["31a", "31a", "31a"], "country": "3argentina", "income": 3000, "duration": 31}])  
## Ejercicio 2  
Listar toas las peliculas del año 2018.  

db.movies.find( {year : 2018 })  
## Ejercicio 3  
Listar las 10 primeras peliculas de Hollywood.  

db.movies.find( {country : "Hollywood" }).limit(10)  
## Ejercicio 4  
Listar las 5 peliculas mas taquilleras. (Mayor income)  

db.movies.find().limit(5).sort({income : -1 })  
## Ejercicio 5  
Listar el 2do conjunto de 5 peliculas mas taquilleras.  

db.movies.find().skip(5).limit(5).sort({income : -1 })  
## Ejercicio 6  
Repetir query 3 y 4 pero retornando solo el titulo y genre.  

db.movies.find( {country : "Hollywood" }, {title: 1, genre: 1, _id: 0}).limit(10)  
db.movies.find( {}, {title: 1, genre: 1, _id: 0}).limit(5).sort({income : -1 })  
## Ejercicio 7  
Mostrar los distintos paises que existen en la base de datos.  

db.movies.distinct("genre")  