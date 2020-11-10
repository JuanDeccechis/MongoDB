# Actividad 1

[HOME](./README.md)  

## Ejercicio 1
Instalar MongoDB en el ambiente local.  
Bajar el instalador: [MongoDB](https://www.mongodb.com/)  

## Ejercicio 2  
Conectarse a MongoDB vía CLI:  
El .exe queda en "C:\Program Files\MongoDB\Server\4.0\bin\mongo" por defecto.  

## Ejercicio 3  
Crear una nueva base de datos llamada futbolfifa:  
use futbolfifa //((crear si no existe) y switchear a la BD “futbolfifa”).  

## Ejercicio 4  
Crear una nueva coleccion llamada players:  
db.createCollection("players")  //(crea la colección “players” en la instancia de BD que esté usando).  

## Ejercicio 5  
Insertar 5 documentos en la coleccion players con los datos básicos (nombre, apellido, posicion, fecha de nacimiento, etc).  
db.players.insert({"nombre": "juan", "apellido": "deccechis", "edad": 26})  
db.players.insert({"nombre": "martin", "apellido": "perez", "edad": 25})  
db.players.insert({"nombre": "jose", "apellido": "gonzalez", "edad": 20})  
db.players.insert({"nombre": "matias", "apellido": "martinez", "edad": 25})  
db.players.insert({"nombre": "pedro", "apellido": "martinez", "edad": 22})  

## Ejercicio 6  
Listar todos los documentos de la coleccion players.  
db.players.find()  

## Ejercicio 7  
Crar otras colecciones con documentos (teams).  
db.createCollection("teams")  
db.teams.insert({"nombre": "equipoVacio"})
