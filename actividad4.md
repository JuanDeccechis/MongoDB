# Actividad 4

[HOME](./README.md)  
## Ejercicio 1  
Utilizar la misma base de datos de peliculas e insertar varias peliculas (al menos 30) con distinto contenido.  

use netflix  
db.movies.insertMany([{"title": "peli01", "year": 2018, "rating": 3, "description": "lorem"}, {"title": "peli02", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli03", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli04", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli05", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli06", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli07", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli08", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli09", "year": 2018, "rating": 3.6, "description": "lorem"}, {"title": "peli10", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli11", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli12", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli13", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli14", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli15", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli16", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli17", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli18", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli19", "year": 2019, "rating": 5.0, "description": "ipsul"}, {"title": "peli20", "year": 2020, "rating": 1.0, "description": "lorem"}, {"title": "peli21", "year": 2020, "rating": 5.0, "description": "ipsul"}, {"title": "peli22", "year": 2020, "rating": 1.0, "description": "lorem"}, {"title": "peli23", "year": 2020, "rating": 5.0, "description": "ipsul"}, {"title": "peli24", "year": 2020, "rating": 1.0, "description": "lorem"}, {"title": "peli25", "year": 2020, "rating": 5.0, "description": "ipsul"}, {"title": "peli26", "year": 2020, "rating": 1.0, "description": "lorem"}, {"title": "peli27", "year": 2020, "rating": 5.0, "description": "ipsul"}, {"title": "peli28", "year": 2020, "rating": 1.0, "description": "lorem"}, {"title": "peli29", "year": 2020, "rating": 5.0, "description": "ipsul"}, {"title": "peli30", "year": 2020, "rating": 1.0, "description": "lorem"}, {"title": "peli31", "year": 2020, "rating": 5.0, "description": "ipsul"}])  
## Ejercicio 2  
Crear indice en field rating y luego hacer busquedas solo usando este campo.  

db.movies.createIndex({rating : 1 })  
db.movies.find({rating : 5.0 })

## Ejercicio 3  
Crear indice en title y description y despues hacer busquedas de texto en estos campos.  

db.movies.createIndex({title: 1 })  
db.movies.createIndex({description: 1 })  
db.movies.find({description : "ipsul" })  
db.movies.find({title : "peli30" })  
db.movies.find({title : "peli30" , description : "ipsul"})  

db.movies.createIndex({title : "text", description : "text" })  
db.movies.find({$text : {$search : "peli2"}}) //este ultimo no funciona  
