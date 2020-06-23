# Buhocenter - Dockerizado ![npm](https://img.shields.io/badge/node-v8.12.0-green) ![npm](https://img.shields.io/badge/vue-2.6.11-red) ![npm](https://img.shields.io/badge/version-1.0-blue) ![npm](https://img.shields.io/badge/postgresql-v.11or12-blue) ![npm](https://img.shields.io/badge/docker-blue)

![Logo-completo](https://user-images.githubusercontent.com/44983658/82739421-64d46c00-9d0d-11ea-87ea-c8c1d27f2a21.png)
## Actividad 3 - integrantes
 ## Angel sucasas
 ## Gabriel Ortega

## Find everything, buy anything

Buhocenter es un nuevo comercio electrónico que permite el pago con criptomonedas. Miles de productos al alcance de un clic, encuentra el producto de tu necesidad en nuestros catálogos, ¿te sientes perdido? No te preocupes, con nuestras categorías podrás encontrar lo que necesites, desde productos de tecnología, hasta productos del hogar.

## Correr el contenedor

Primero debe colocarse dentro de la carpeta raiz del proyecto, la cual seria "practica-3",deberia ver algo asi:

![image](https://user-images.githubusercontent.com/44983658/85345059-6ab19e80-b4bf-11ea-9a66-1872504584d5.png)

 en esa ruta , abra la terminal y ejecute el siguiente comando:
 
 ```bash
$ docker-compose up -d --force-recreate
```
 esto puede tardar un poco (en nuestro caso tardaba aproximadamente 50 min o 1 hora), en caso de una conexion lenta , docker le mostrara este mensaje:
 
 si el comando anterior no le hace el build , tendra que ejecutar el siguiente comando:
 
  ```bash
$  docker-compose up --build
```

 ![image](https://user-images.githubusercontent.com/44983658/85345045-61c0cd00-b4bf-11ea-847e-62e64d8bdbac.png)
 
una vez listo, ya podra ver buhocenter [aca](http://localhost:8081/home) en el puerto 8081

## Inserts a la BD

 aun faltan los inserts,ejecutaremos el siguiente comando:
 
   ```bash
$  docker cp ./inserts.sql buhocenter-postgres:/docker-entrypoint-initdb.d/dump.sql
```

y luego :

   ```bash
$  docker exec -u postgres buhocenter-postgres psql buhocenter postgres -f docker-entrypoint-initdb.d/dump.sql
```
y deberiamos ver algo como esto, donde se ve que ya se estan ejecutando los inserts:

![image](https://user-images.githubusercontent.com/44983658/85357463-5d0c1100-b4df-11ea-944c-9aa050f70604.png)

y listo, ya tendremos los inserts en la BD y podremos disfrutar de buhocenter [aca](http://localhost:8081/home) !

(en http://localhost:8081/home )

---------------------------
## MIT © 
[Ángel Sucasas](mailto:aasucasas.17@est.ucab.edu.ve)
[Gabriel Ortega](mailto:geortega.17@est.ucab.edu.ve)

------------------------

