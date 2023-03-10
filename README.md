# Lab_5_AREP

El taller consiste en crear una aplicación web pequeña usando el micro-framework de Spark java (http://sparkjava.com/). Una vez tengamos esta aplicación procederemos a construir un container para docker para la aplicación y los desplegaremos y configuraremos en nuestra máquina local. Luego, cerremos un repositorio en DockerHub y subiremos la imagen al repositorio. Finalmente, crearemos una máquina virtual de en AWS, instalaremos Docker , y desplegaremos el contenedor que acabamos de crear.

## Conceptos Básicos


### Docker


"*Docker es un proyecto de código abierto que automatiza el despliegue de aplicaciones dentro de contenedores de software, proporcionando una capa adicional de abstracción y automatización de virtualización de aplicaciones en múltiples sistemas operativos.*"


### Spark


"*Spark es un framework de computación en clúster open-source. Fue desarrollada originariamente en la Universidad de California, en el AMPLab de Berkeley.*"


### MongoDB
"*MongoDB es un sistema de base de datos NoSQL, orientado a documentos y de código abierto. En lugar de guardar los datos en tablas, tal y como se hace en las bases de datos relacionales, MongoDB guarda estructuras de datos BSON (una especificación similar a JSON) con un esquema dinámico, haciendo que la integración de los datos en ciertas aplicaciones sea más fácil y rápida.*"


### Round Robin
"*Round-robin es un método para seleccionar todos los abstractos en un grupo de manera equitativa y en un orden racional, normalmente comenzando por el primer elemento de la lista hasta llegar al último y empezando de nuevo desde el primer elemento.*"


### AWS(EC2)
*"Amazon Elastic Compute Cloud es una parte central de la plataforma de cómputo en la nube de la empresa Amazon.com denominada Amazon Web Services. EC2 permite a los usuarios alquilar computadores virtuales en los cuales pueden ejecutar sus propias aplicaciones."*

## Arquitectura

![image](https://user-images.githubusercontent.com/90571387/224220769-71a51a73-a8cd-41d4-91d2-0e48baf53dac.png)

La solución de la arquitectura, está diseñada en dos partes, el frontend "LogService" y el backend "RoundRobinSpark"
## Generar Imágenes


Para poder generar las imágenes de Docker, se hace una copia del repo, después debemos compilar el backend y el balanceador, para poder hacer esto ingresamos a estas carpetas y utilizamos los comandos.
```
mvn clean install
mvn package
```
Despues de compilar el proyecto, utilizamos el siguiente comando para generar la imagenes y desplegar el proyecto.
```
docker-compose up -d
```

Aquí podemos ver el despliegue desde la consola de aws:

![Docker](https://media.discordapp.net/attachments/971608324137177088/1085781055048527902/image.png?width=718&height=410)


## Links
### AWS
```
http://ec2-54-172-15-68.compute-1.amazonaws.com/
```

## Despliegue AWS 

![Docker](https://media.discordapp.net/attachments/971608324137177088/1085780386094784592/image.png?width=1440&height=575)

![image](https://media.discordapp.net/attachments/971608324137177088/1085780630446546954/image.png?width=718&height=300)

## Muestra en Postman

![image](https://media.discordapp.net/attachments/971608324137177088/1085781583195275304/image.png?width=718&height=317)
