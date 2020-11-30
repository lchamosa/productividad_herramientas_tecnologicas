# Sistema de Registro de Atletas en Silla de Ruedas

Descripción.

Esta propuesta es para la construcción en Java y MySQL de una aplicación web enfocada a apoyar a los entrenadores y atletas de la Asociación de Deportes sobre Silla de Ruedas IMSS Valle de México.

Problema Identificado.

Una gran necesidad que presenta esta asociación es la salvaguarda de información de los atletas. Hasta la fecha, los registros de los atletas, eventos, resultados, etc. se almacenan en medios impresos (como periódicos, documentos impresos) o medios digitales (como correos electrónicos, computadoras personales, unidades USB, discos duros externos). Aún más preocupante, estos medios no están concentrados en una sola persona o ubicación; cada persona interesada puede contar con una “pieza del rompecabezas”. 
Esta situación dificulta en extremo el mantener un registro confiable y actualizado del progreso y logros de los atletas de la Asociación. Es responsabilidad de la Asociación reportar continuamente este tipo de información a las autoridades competentes; también tiene como necesidad generar expedientes de los atletas para ser considerados en distintos eventos o reconocimientos, etc. 
Cada vez que es necesario armar este tipo de reportes, los miembros de la Asociación recolectan la información en los distintos medios disponibles; cayendo en situaciones como “sólo tengo estas fotos”, “no tenemos imagen del reconocimiento otorgado a un atleta”, “se perdió el correo con x información”, “perdí el respaldo de archivos que tenía en mi computadora”, “mi USB ya no funciona”.

Solución. 

Es por esto por lo que el objetivo del proyecto es crear un sistema/aplicación/página web para llevar un registro y control de los atletas de la Asociación de Deportes sobre Silla de Ruedas IMSS Valle de México”. Se pretende lograr la información de dichos atletas pueda ser consultada de manera rápida y amigable a través de una interfaz gráfica; por cualquier persona con intereses relacionados al deporte sobre silla de ruedas.

Arquitectura

La aplicación se ha diseñado para ser desplegada en un servidor Web para lo cual previamente se debe de contratar el “host” y el “dominio”, la arquitectura de despliegue corresponde a una aplicación simple web en donde tenemos dentro de un servidor web contratado el servidor de aplicaciones y el servidor de base de datos.  El servidor de aplicaciones debe soportar Java y el servidor de base de datos deberá contar con MySQL y el sistema web debe proveer de una página web responsiva de tal manera que pueda ser vista en una computadora, tableta o teléfono celular sin ningún problema, entiéndase por página responsiva como aquella página que se adapta al dispositivo en donde se está desplegando, reacomodando sus elementos de tal manera que sea fácil su uso y agradable visualmente. 

Para la arquitectura del código se ha diseñado una estructura de clases las cuales interactúan entre si mediante objetos complejos que son tomados de la capa de entidades, es decir si alguna clase tiene alguna relación con otra y utiliza sus datos, estos serán pasados a través de un objeto del tipo de la clase correspondiente en la capa de entidades que mapee los datos de la clase origen o en su defecto una lista de objetos cuando la relación sea de uno a muchos. Además, se tiene contemplado la implementación del patrón de diseño “singleton” en las clases que contendrán datos estáticos, como es el caso de Clasificación, Lesión, TipoLesion, Acción y Rol, esto con la finalidad de optimizar la memoria del servidor al generar sólo una instancia de las clases mencionadas para todos los usuarios firmados en el sistema. 
La estructura del código tambien contempla una construcción en cuatro capas, las cuales son la capa de datos, la de negocio y la de presentación, la última capa es la de entidades de negocio y se relaciona directamente con tres primeras capas mencionadas,  estas entidades de negocio son clases que estarán mapeando las tablas de la base de datos y servirán para pasar los datos entre las clases que forman la estructura del código fuente asi como entre las mismas capas.

Tabla de contenidos.

Enlace que redirecciona al sitio de ZUBE donde se está llevando la administración del proyecto con la metodología SCRUM por sprint, en este link se puede apreciar un tablero Kanban.
Workspace 1 | Kanban (zube.io)

Enlace que redirecciona al sitio de HEROKU donde se realizaran las publicaciones del sistema.
https://dashboard.heroku.com/apps/crasir/deploy/github

Requerimientos.

•	Para el desarrollo será necesario contar con la última version empresarial de NetBeans la cual permite construir soluciones web, esta version se debe instalar localmente. 
•	Se deberá instalar MySQL localmente y generar la base de datos.
•	El código fuente será administrado por medio de GIT.
•	La asociación deberá de proveer un dominio para poder subir a la web su aplicación web, para lo cual se les proporcionará la debida asesoría. 
•	La asociación deberá de proveer un host para poder publicar el sitio en la web, para lo cual se les proporcionará la asesoría correspondiente, este host debe soportar aplicaciones web      construidas con Java y contar con MySQL.
•	El servidor web deberá contar con Apache Tomcat y Java8

