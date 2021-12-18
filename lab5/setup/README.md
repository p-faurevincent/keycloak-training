# Requirements and Setup

## Requirements

* [Java SDK](https://adoptopenjdk.net) Version 11 or 14
* A Java IDE like
  * [Eclipse](https://www.eclipse.org/downloads)
  * [Spring Toolsuite](https://spring.io/tools)
  * [IntelliJ](https://www.jetbrains.com/idea/download)
  * [Visual Studio Code](https://code.visualstudio.com)
* [Keycloak](https://keycloak.org)
* [Docker](https://docs.docker.com/engine/install) if you want to run Keycloak as docker container
* [Git](https://git-scm.com)
* [Postman](https://www.getpostman.com/downloads), [Httpie](https://httpie.org/#installation), or [Curl](https://curl.haxx.se/download.html) for REST calls

In case you select [Postman](https://www.getpostman.com/downloads), then the provided [Postman Collection](oidc_workshop.postman_collection.json) might be helpful.
Just import this [Postman Collection (Version 2.1 format)](oidc_workshop.postman_collection.json) into Postman.

### IntelliJ

IntelliJ does not require any specific additional plugins or configuration.

### Eclipse IDE

If you are an Eclipse user, then the usage of the Eclipse-based [Spring ToolSuite](https://spring.io/tools) is strongly recommended.
This eclipse variant already has all the required gradle and spring boot support pre-installed.

In case you want to stick to your plain Eclipse installation then you have to add the following features via the
eclipse marketplace: 

* BuildShip Gradle Integration (Version 3.x). This might be already pre-installed depending 
on your eclipse variant (e.g. Eclipse JavaEE) installed.
* Spring Tools 4 for Spring Boot (Spring Tool Suite 4).

### Visual Studio Code

To be able to work properly in Visual Studio Code with this Spring Boot Java Gradle project you need at least these extensions:

* Java Extension Pack
* vscode-gradle-language
* VS Code Spring Boot Application Development Extension Pack

## Import the source code
                       
You can import the whole project directory into your IDE as a __gradle project__:

* [IntelliJ](https://www.jetbrains.com/idea): Open menu item "New project from existing sources..." and then select 'Gradle' when prompted
* [Eclipse](https://www.eclipse.org/) or [Spring ToolSuite](https://spring.io/tools): Open menu item "Import/Gradle/Existing gradle project"
* [Visual Studio Code](https://code.visualstudio.com/): Just open the root directory in VS Code and wait until VS Code has configured the project

## Run the java applications

All spring boot based java projects can either be run using your Java IDE or using the command line
with changing into the corresponding project directory and issuing a `gradlew bootRun` command.

For other demo applications like the ones for Micronaut or Quarkus please consult written instructions there. 

## Setup Keycloak

Here we will use [Keycloak](https://keycloak.org) by RedHat/JBoss.

For this lab we are going to use a pre configured Realm for the all Java applications.

To do so, go to the web admin UI of Keycloak and in the top left > Add Realm > select and import this file [keycloak_realm_workshop.json](./keycloak_realm_workshop.json)

Now, if you see the realm _workshop_ on the left then Keycloak is ready to use it for this part of the keycloak labs.

![Keycloak Workshop](keycloak_workshop.png)

### Further Information

If you want to know more about setting up a Keycloak server for your own projects 
then please consult the [keycloak administration docs](https://www.keycloak.org/docs/latest/server_admin/index.html).