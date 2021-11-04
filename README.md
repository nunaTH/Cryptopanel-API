# Cryptopanel-API
Development of a GraphQL interface in Java for an existing monolithic application

### The goals are:
* Other applications (web apps, native apps, monitoring, analysis tools) should be able to use the data.
* The close coupling between application and data is to be dissolved.
* The data structure should be documented openly

As part of the project, it should be made possible to query information about invoices and payments that are recorded in the CryptoPanel API via a web interface.

Access to the data must be controllable via rights management. Statistical information without personal data should be able to be queried without authentication. For example, it should be possible to query the portal's total turnover within a month for individual crypto currencies without a user account.

To query confidential data, authentication must be carried out using a username and password. A sophisticated rights management is not part of the project mandate but should be possible in the future.

The access to the data should take place through a server-side implementation of a GraphQL interface.

![image](https://user-images.githubusercontent.com/83286808/140423491-f2d5c27e-4c1a-4d27-96af-215e1c027611.png)

All the interface functions created as part of the project must be secured by unit tests

![image](https://user-images.githubusercontent.com/83286808/140423717-d5d67df2-0829-4b18-aa52-30eafd4f48bb.png)

The implementation of the GraphQL interface is done in Java with the help of the Spring Boot framework.
The interface is implemented with Java Version 11 from Oracle and will also be operated later.

![image](https://user-images.githubusercontent.com/83286808/140423893-d3ecf446-4f6b-4289-b5a7-a3c4a3ae6e8c.png)

The existing database of the CryptoPanel application is addressed with the JPA standards and Hibernate of the Spring Boot Framework. 

![image](https://user-images.githubusercontent.com/83286808/140423969-0f7cdf8c-a821-4950-9716-dc0e06b0d0ff.png)
![image](https://user-images.githubusercontent.com/83286808/140423991-a39b62a8-bb00-4931-9059-db9853f08157.png)

All the interface functions created as part of the project were written in Java in order to extend GraphQL and to be able to query the database via a web API. The data is accessed via a server-side implementation of a GraphQL interface. To query confidential data, authentication is carried out using a username and password.

![image](https://user-images.githubusercontent.com/83286808/140424149-9d320331-9a11-4989-b1c9-fbfcdfb6352a.png)
![image](https://user-images.githubusercontent.com/83286808/140424178-40d05827-4e0e-4d1e-a2dd-c58096292ee6.png)

### The application is made available in the following steps:
* Deployment is easy because the framework includes everything you need, for example an integrated web server.
* Using the Gradle build environment, it is very easy to create executable archives that are compatible with all modern cloud environments for Java or Docker.
* Simplest example:
  * **./gradlew bootJar** (Creates the archive)
  * **jar -xf cryptopanel-0.0.1-SNAPSHOT.jar** (unpacks the archive and makes it executable)
  * **java org.springframework.boot.loader.JarLauncher** (executes the application)
  * The last step can be edited in a Docker container or any hosting environment.

Choosing GraphQL ensures that even after future extensions of the underlying data model, efficient queries will be possible via the created interface.
* An authentication system for the existing web applications.
* A further development of existing functions and new functions.
* Unit test function for further developed and new functions.

These features can then be integrated into the CryptoPanel API application, as this is based on the GraphQL interface.

In the project, the choice of Spring and Spring-Boot was specified as the development framework. The framework offers very unusual mechanisms to handle standard tasks such as routing, database connections and the integration of dependencies (Dependency Injection, DI). However, the high degree of abstraction shows a good familiarization with the standards of the framework in many places, which leads to a steep learning curve at the beginning. This familiarization period was underestimated during project planning, which is reflected in the increased time required to implement the application.
---


