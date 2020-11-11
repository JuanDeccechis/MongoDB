# Actividad 2

[HOME](./README.md)  

## Ejercicio 1  
Crear una nueva base de datos de un sistema de straming de video que permita almancenar movies (netflix).  
use netflix  
db.createCollection("movies")

## Ejercicio 2  
Para cada movie, se deberia guardar informacion como titulo (String), year (Number), rating (Number, entre 1.0 y 5.0), genre (String), description (String), actors (Array< String>), country (String), income (Number), duration (Number).  
db.movies.insert({"title": "asd", "year": 2020, "rating": 3.0, "genre": "drama", "description": "lorem", "actors": ["a1", "a2", "a3"], "country": "argentina", "income": 100, "duration": 2})  

## Ejercicio 3  
Agregar peliculas usando insert(), insertOne(), insertMany().  
db.movies.insert({"title": "asd", "year": 2020, "rating": 3.0, "genre": "drama", "description": "lorem", "actors": ["a1", "a2", "a3"], "country": "argentina", "income": 100, "duration": 2}) //el del ejercicio anterior  
db.movies.insertOne({"title": "asd2", "year": 20202, "rating": 3.02, "genre": "drama2", "description": "lorem2", "actors": ["a1", "a22", "a3"], "country": "argentina2", "income": 1002, "duration": 22})  
db.movies.insertMany([{"title": "asd3", "year": 20203, "rating": 4.3, "genre": "drama3", "description": "lorem3", "actors": ["a1", "a23", "a33"], "country": "argentina3", "income": 1003, "duration": 23}, {"title": "asd4", "year": 20204, "rating": 4.6, "genre": "drama4", "description": "lorem4", "actors": ["a14", "a24", "a34"], "country": "argentina4", "income": 1004, "duration": 24}])  

## Ejercicio 4  
Actualizar películas agregando el field highlighted=true a aquellas con rating > 4.5  
db.movies.updateMany( {rating : {$gt: 4.5 } }, { $set: { highlighted: true }})  

## Ejercicio 5  
Actualizar peliculas cambiando genre "drama" por "bored".  
db.movies.updateMany( {genre : "drama" }, { $set: { genre: "bored" }})  

## Ejercicio 6  
Borrar todas las peliculas que tengan mas de 30 años  
db.movies.deleteMany( {year : {$lt: 1990 } })  

## Ejercicio 7  
Buscar todas las peliculas argentinas.  
db.movies.find( {country : "argentina" })  

## Ejercicio 8  
Buscar todas las peliculas de accion con un buen rating (> 4.0) que hayan salido los ultimos 2 años.  
db.movies.find( {genre: "accion", rating : {$gt: 4.5 }, year : {$gt: 2018 } })  