# Name:NARRA RAMYA
# Register Number: 212223040128
## Ex 01 -Simple Web Server using Spring Boot

## AIM:
To develop a Simple Web Server using Spring Boot that can handle basic HTTP requests and return appropriate responses through RESTful endpoints.
## ALGORITHM:
Start a New Spring Boot Project:

Use Spring Initializr (https://start.spring.io/)

Select dependencies: Spring Web

Create the Main Application Class:

This class contains the main() method with @SpringBootApplication annotation to bootstrap the application.

Create a Controller Class:

Create a class annotated with @RestController.

Define one or more HTTP request handler methods using @GetMapping, @PostMapping, etc.

Write Endpoint Methods:

Inside the controller, define a simple method for handling GET requests (e.g., return “Hello World” when /hello is accessed).

Run the Application:

Run the application using your IDE or via the command line (mvn spring-boot:run or ./mvnw spring-boot:run).

Test the Endpoint:

Open a web browser or use Postman to visit:
http://localhost:8080/hello

You should see the output (e.g., "Hello World").

Stop the Server:

Stop the Spring Boot server once testing is complete.


## Program 

<img width="651" height="527" alt="image" src="https://github.com/user-attachments/assets/a98ac0a9-e7ac-4f4f-925f-beb551c71c8f" />

 ### Pom.xml
```
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>4.1.0</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>
	<groupId>com.example</groupId>
	<artifactId>ajw-exp-1</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name/>
	<description/>
 <properties>
	<java.version>21</java.version>
	</properties>
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-webmvc</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-webmvc-test</artifactId>
			<scope>test</scope>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>

</project>
```
### AjwExp1Application.java

```
package com.example.ajw.exp_1;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class AjwExp1Application {

	public static void main(String[] args) {
		SpringApplication.run(AjwExp1Application.class, args);
	}

}

```

### HelloController.java
```
package com.example.ajw.exp_1;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Spring Boot!";
    }
}
```


### application.properties:
```
spring.application.name=ajw-exp-1
server.port=8081
```

# Output:

<img width="1125" height="795" alt="image" src="https://github.com/user-attachments/assets/93e69a79-f63e-407f-8a21-9893d8d9da88" />



# Result:
Thus, the Simple Web Server was successfully developed using Spring Boot. The application was able to handle basic HTTP requests through RESTful endpoints and return appropriate responses for the requested URLs.


