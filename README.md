# Sistema de Registro de Atletas en Silla de Ruedas

## Descripción.

Esta propuesta es para la construcción en Java y MySQL de una aplicación web enfocada a apoyar a los entrenadores y atletas de la Asociación de Deportes sobre Silla de Ruedas IMSS Valle de México.

## Problema Identificado.

Una gran necesidad que presenta esta asociación es la salvaguarda de información de los atletas. Hasta la fecha, los registros de los atletas, eventos, resultados, etc. se almacenan en medios impresos (como periódicos, documentos impresos) o medios digitales (como correos electrónicos, computadoras personales, unidades USB, discos duros externos). Aún más preocupante, estos medios no están concentrados en una sola persona o ubicación; cada persona interesada puede contar con una “pieza del rompecabezas”. 
Esta situación dificulta en extremo el mantener un registro confiable y actualizado del progreso y logros de los atletas de la Asociación. Es responsabilidad de la Asociación reportar continuamente este tipo de información a las autoridades competentes; también tiene como necesidad generar expedientes de los atletas para ser considerados en distintos eventos o reconocimientos, etc. 
Cada vez que es necesario armar este tipo de reportes, los miembros de la Asociación recolectan la información en los distintos medios disponibles; cayendo en situaciones como “sólo tengo estas fotos”, “no tenemos imagen del reconocimiento otorgado a un atleta”, “se perdió el correo con x información”, “perdí el respaldo de archivos que tenía en mi computadora”, “mi USB ya no funciona”.

## Solución. 

Es por esto por lo que el objetivo del proyecto es crear un sistema/aplicación/página web para llevar un registro y control de los atletas de la Asociación de Deportes sobre Silla de Ruedas IMSS Valle de México”. Se pretende lograr la información de dichos atletas pueda ser consultada de manera rápida y amigable a través de una interfaz gráfica; por cualquier persona con intereses relacionados al deporte sobre silla de ruedas.

## Arquitectura

La aplicación se ha diseñado para ser desplegada en un servidor Web para lo cual previamente se debe de contratar el “host” y el “dominio”, la arquitectura de despliegue corresponde a una aplicación simple web en donde tenemos dentro de un servidor web contratado el servidor de aplicaciones y el servidor de base de datos.  El servidor de aplicaciones debe soportar Java y el servidor de base de datos deberá contar con MySQL y el sistema web debe proveer de una página web responsiva de tal manera que pueda ser vista en una computadora, tableta o teléfono celular sin ningún problema, entiéndase por página responsiva como aquella página que se adapta al dispositivo en donde se está desplegando, reacomodando sus elementos de tal manera que sea fácil su uso y agradable visualmente. 

Para la arquitectura del código se ha diseñado una estructura de clases las cuales interactúan entre si mediante objetos complejos que son tomados de la capa de entidades, es decir si alguna clase tiene alguna relación con otra y utiliza sus datos, estos serán pasados a través de un objeto del tipo de la clase correspondiente en la capa de entidades que mapee los datos de la clase origen o en su defecto una lista de objetos cuando la relación sea de uno a muchos. Además, se tiene contemplado la implementación del patrón de diseño “singleton” en las clases que contendrán datos estáticos, como es el caso de Clasificación, Lesión, TipoLesion, Acción y Rol, esto con la finalidad de optimizar la memoria del servidor al generar sólo una instancia de las clases mencionadas para todos los usuarios firmados en el sistema. 
La estructura del código tambien contempla una construcción en cuatro capas, las cuales son la capa de datos, la de negocio y la de presentación, la última capa es la de entidades de negocio y se relaciona directamente con tres primeras capas mencionadas,  estas entidades de negocio son clases que estarán mapeando las tablas de la base de datos y servirán para pasar los datos entre las clases que forman la estructura del código fuente asi como entre las mismas capas.

# Tabla de contenidos.

Enlace que redirecciona al sitio de ZUBE donde se está llevando la administración del proyecto con la metodología SCRUM por sprint, en este link se puede apreciar un tablero Kanban.
Workspace 1 | Kanban (zube.io)

Enlace que redirecciona al sitio de HEROKU donde se realizaran las publicaciones del sistema.
https://dashboard.heroku.com/apps/crasir/deploy/github

# Requerimientos.

- Para el desarrollo será necesario contar con la última version empresarial de NetBeans la cual permite construir soluciones web, esta version se debe instalar localmente. 
- Se deberá instalar MySQL localmente y generar la base de datos.
- El código fuente será administrado por medio de GIT.
- La asociación deberá de proveer un dominio para poder subir a la web su aplicación web, para lo cual se les proporcionará la debida asesoría. 
- La asociación deberá de proveer un host para poder publicar el sitio en la web, para lo cual se les proporcionará la asesoría correspondiente, este host debe soportar aplicaciones web      construidas con Java y contar con MySQL.
- El servidor web deberá contar con Apache Tomcat y Java8

# Instalacion

## ¿Cómo instalar el ambiente de desarrollo?

Se deben de seguir los siguientes pasos:

1. Instalar MySQL
- Ir al sitio de MySQL https://dev.mysql.com/downloads/
- Descargar “MySQL Installer for Windows”
- Una vez descargado, dar doble clic al archivo instalador y Windows nos preguntara si deseamos ejecutarlo como administrador a lo que le indicamos que sí.
- Esperamos a que se instale la base de datos y finalmente ejecutar el script de creacion de base de datos.

2. Instalar el conector de MySQL
   Este conector nos va a servir para conectar nuestro código de Java con la base de datos MySQL, para lo que debemos hacer lo siguiente:

- Ir al sitio de MySQL https://dev.mysql.com/downloads/connector/j/
- Nos aseguramos de que el sistema operativo recomendado sea el que tenemos instalado en nuestro equipo, después damos clic en el botón “Go to Download Page”
- Seleccionamos el paquete con la version mas reciente y de preferencia a 64 bits (si es que esta disponible) y damos clic en el botón “Download” para descargar el instalador.
- Una vez descargado, dar doble clic al archivo instalador y Windows nos preguntara si deseamos ejecutarlo como administrador a lo que le indicamos que sí.
- Esperamos a que se termine de instalar el paquete.
- Instalar el IDE de NetBeans 8.2
- Ir al sitio de NetBeans https://netbeans.org/downloads/8.2/rc/start.html?platform=windows&lang=en&option=all y automáticamente se descarga la version del IDE con la version completa que   soporta HTML5 y JavaScript ademas de otras utilerías necesarias,  si la instalación no inicia automáticamente dar clic en el texto “download it here”.
- Una vez descargado, dar doble clic al archivo instalador y Windows nos preguntara si deseamos ejecutarlo como administrador a lo que le indicamos que sí.
- Esperamos a que se termine de instalar el paquete.

## ¿Cómo ejecutar pruebas manualmente?
Para la ejecución de pruebas manuales se realizarán de dos maneras y están contempladas en el plan de trabajo, estas pruebas se estarán realizando cada cierre de sprint y al final del desarrollo del sistema.

**Pruebas de integración.**

Para las pruebas de integración se deben definir previamente los casos de prueba, para cada modulo se construirá una matriz con distintos escenarios y los resultados esperados, estas matrices de prueba se construyen en conjunto con el usuario para que tengamos certeza de que el desarrollo que se esta realizando está funcionando correctamente. Teniendo los casos de prueba definidos, las pruebas de integración se realizan por el equipo de desarrollo (deseable por QA) en este caso siguiendo los casos de prueba, para tal efecto se instalará una versión del sistema completo funcionando en un ambiente de pruebas, dependiendo de los resultados se procede a corregir errores o a la siguiente etapa que son las pruebas de usuario.

**Pruebas de liberación o de usuario.**

Este tipo de prueba las debe de realizar el cliente en un ambiente real pero controlado, el usuario debe de ejecutar el sistema siguiendo su operación normal y de esta manera identificar si el producto esta correcto o hay que hacer algunos ajustes.


## ¿Cómo implementar la solución en producción en un ambiente local o en la nube como Heroku?

Se investigo al respecto y es muy fácil la implementación en Heroku, simplemente hay que hacer los siguientes pasos. 

1. Dirigirse al sitio web de Heroku.  
2. El sitio nos pedirá que nos registremos o que iniciemos sesión, si ya estamos registrados damos clic en “log in” 
   Una vez que dimos clic en “log in” vemos esta pantalla y precedemos a firmarnos con nuestras credenciales.
3. Ya que estemos firmados, veremos el **Deployment method**
4. Y procedemos a conectarnos a nuestro repositorio GitHub presionando el icono que dice **GitHub** y eligiendo nuestro repositorio (al presionar el icono de GitHub se nos pedirá que nos firmemos en    nuestra cuenta de GitHub y seleccionemos el repositorio).
5. Ya que nos hemos conectado podremos ver la sopción para hacer un “deploy” manual, en esta sección podemos elegir que Branch queremos publicar.
6. Seleccionamos el Branch y presionamos “Deploy Branch” entonces Heroku realiza una revisión y compilación del código encontrado, si no hay errores en el codigo entonces se publica en una URL temporal.



 
