---
layout: two-cols
layoutClass: gap-4
---

# Creación de proyecto: academy_backend
Abra la Paleta de Comandos (`Ctrl+Shift+P`)

Escriba y selecciona: Spring Initialzr: Create a Maven Project

Complete los siguientes campos:

* Spring Boot version: **4.1.1**
* Language: **Java**
* Group id: **edu.academy**
* Artifact id: **coursesmng**
* Package: <br>**edu.academy.coursesmng**
* Package type: **jar**
* Java version: **25**

::right::

## Dependencias

* Spring Data JPA
* Spring Web
* Spring Boot Dev Tools
* MySQL Driver 

---
layout: default
transition: fade-out
---
# Configuración del datasource del proyecto

Abra del arhivo application.properties

```properties
spring.application.name=coursemng

spring.datasource.url=jdbc:mysql://163.178.107.2:3306/academy_db
spring.datasource.username=laboratorios
spring.datasource.password=TUy&)&nfC7QqQau.%278UQ24/=%

# Turn off the Spring Boot banner
spring.main.banner-mode=off

# Reduce logging level. Set logging level to warn
logging.level.root=warn

# Show JPA/Hibernate logging messages
logging.level.org.hibernate.SQL=trace
logging.level.org.hibernate.orm.jdbc.bind=trace

#context path
server.servlet.context-path=/coursemng
server.port = 8084

```