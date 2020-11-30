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

[Documento de Arquitectura](https://github.com/lchamosa/productividad_herramientas_tecnologicas/blob/main/2-Dise%C3%B1o/PHT_Dise%C3%B1oArquitectura.pdf)

[Documento de Base de Datos](https://github.com/lchamosa/productividad_herramientas_tecnologicas/blob/main/2-Dise%C3%B1o/PHT_Dise%C3%B1oBaseDatos.pdf)

# Tabla de contenidos.

Enlace que redirecciona al sitio de ZUBE donde se está llevando la administración del proyecto con la metodología SCRUM por sprint, en este link se puede apreciar un tablero Kanban.
https://zube.io/certificado-java/control-y-registro-de-atletas-en-silla-de-ruedas/w/workspace-1/kanban

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

# Referencia para usuario final

[Referencia de funcionalidad del sistema](https://github.com/lchamosa/productividad_herramientas_tecnologicas/blob/main/2-Dise%C3%B1o/PHT_Prototipo.pdf)

# Contribucion

[Documentacion de GitHub](https://github.com/lchamosa/productividad_herramientas_tecnologicas/blob/main/5-Documentacion/PHT_ContribucionGIT.pdf)

# Roadmap

Esta aplicación es solo una versión inicial del sistema que se esta proponiendo, en el tetramestre empresarial se incluirán los módulos siguientes que por si solos, sobre todo los módulos 2,3, y 4 tienen mucha funcionalidad implícita.

1.	Administración de entrenadores.
2.	Administración de eventos.
3.	Administración de pruebas.
4.	Registro del plan de entrenamiento de atletas.


 
