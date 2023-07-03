# API Course
[![Sppring boot ](https://img.shields.io/badge/JAVA-<Stable>-<COLOR>.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)

Curso
# ¿Qué son los microservicios? 📋

Los microservicios son tanto un estilo de arquitectura como un modo de programar software. Con los microservicios, las aplicaciones se dividen en sus elementos más pequeños e
independientes entre sí. A diferencia del enfoque tradicional y monolítico de las aplicaciones, en el que todo se compila en una sola pieza, los microservicios son elementos
independientes que funcionan en conjunto para llevar a cabo las mismas tareas. Cada uno de esos elementos o procesos es un microservicio. Este enfoque de desarrollo de software
valora el nivel de detalle, la sencillez y la capacidad para compartir un proceso similar en varias aplicaciones. Es un elemento fundamental de la optimización del desarrollo de
aplicaciones hacia un modelo nativo de la nube.
¿Pero cuáles son las ventajas de utilizar una infraestructura de microservicios? En pocas palabras, el objetivo es distribuir sistemas de software de calidad con mayor rapidez,
lo cual es posible gracias a los microservicios, pero también se deben considerar otros aspectos. Dividir las aplicaciones en microservicios no es suficiente; es necesario
administrarlos, coordinarlos y gestionar los datos que crean y modifican.

# Objetivo de Maps-Service 📭
* Ofrece un API única abstrayendo del proveedor de acceso de la informacion
* Obtencion de información de Geo-posicionamiento de usuario
* Obtener Mapas de localizacion a partir de coordenadas GPS
## Diagrama de la solución  📊️
* El HLA (High Level Architecture) de la solución se detalla a continuación:

  ![HLA-solution.png](HLA-solution.png)
* Diagrama model-Spring:
  ![maps-spring-model.png](maps-spring-model.png)
* Diagrama de clases de la solución:
  ![maps-service.png](maps-service.png)
# Changelog
* Java 17
# Stack Tecnológico 🛠️
* Java 17 JDK
* Apache Maven 3.5.x en adelante
* Spring boot - Framework de java
* Junit - Tests y Test de integración.
# Entorno de Desarrollo 🚀
Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas.
* [Git]()
* Java 17 JDK
* [Spring boot](https://spring.io/projects/spring-boot) - Framework de java 2.7.1
* Intellij-Eclipse-vscode
* Maven 3.8.1
* [Lombok](https://projectlombok.org/) - librería que a través de anotaciones reduce el código que escribimos.
* [Junit](https://junit.org/junit5/) - Tests y Test de integración.
  Este entorno necesita permisos de acceso a la red de Riu.
* [gitignore](https://www.toptal.com/developers/gitignore) - Creación de archivo .gitignore

#### Instalar Lombok en el IDE
Esto depende del IDE(1) que utilices, seguir indicaciones de la web de Project Lombok

* Lombok para evitar código 'boilerplate'

## Ejecutar el proyecto

Procede a compilar la solución con el bash:

```
mvn clean compile
```

## Generate git.properties file

Información del repositorio Git en una aplicación basada en Spring Boot construida con Maven.
Para ello utilizaremos maven-git-commit-id-plugin - una práctica herramienta creada únicamente para este propósito.
Para generar el archivo `git.properties` es necesario compilar el proyecto con el comando maven

```shell
mvn clean compile
```
#### Despliegue en Openshift
* Los despliegues de imagenes SNAPSHOT, se realizan desde el branch develop
* Los despliegues de imagenes RELEASE, se realizan desde el banch master despues de creat un tag de versión.

## URLs del Proyecto  💻

* [Desarrollo](pendiente)
* [Integración](pendiente)



## Documentación adicional 📖

Wiki del proyecto [Documento]()



## Versionado 📌

Usamos [SemVer](http://semver.org/) para el versionado.

## Conventional Commits 🔧
Para nuestros mensajes de commit utilizamos [Commits Convencionales](https://www.conventionalcommits.org/)


## Problemas comunes 😣

---

* Maven no puede bajar las dependencias

  Verificar configuración de proxy: Ir a C:\Users\\{tuUsuario}\\.m2

* No puede iniciar la app en entorno local por problemas de permisos al escribir el archivo de log

  Definir una nueva variable de entorno con la ruta adecuada, ejemplo: export LOG_PATH=/tmp

* Error de certificado al intentar acceder a la url de personas

  Agregar el certificado provisto por la url definida en application.properties.

  Descargar el certificado de la página indicada en application.properties y luego agregar el certificado.
  Ejemplo:
    * En Linux, puede correr el siguiente comando por consola:
      sudo keytool -importcert -cacerts -file /mypath/apidesa.gscorp.ad.pem -alias ApiDesaCert

    * En Windows, puede correr el siguiente comando en la consola de windows (como administrador):
      your_java_home\jdk_x.xx\jre\bin\keytool -importcert -file "C:\mypath\apidesa.gscorp.ad.pem" -alias CertArtifactory -trustcacerts -keystore "C:\Program Files\Java\jdk-11.0.5\lib\security\cacerts"
* Comandos git
```
git remote show --> Muestra la(s) url del repositorio remoto
```

## Autor ✒

* **Jaime Peredo** - *Líder técnico* - [jperedo](https://gitlab/jperedo)
