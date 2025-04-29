
# Hello World Spring Boot Application

## Description
This is a minimal Spring Boot application that demonstrates the basics of creating a web app with Spring Boot. The app responds with simple messages including a JSON-formatted greeting.

## Requirements
- Java 17+
- Maven 3.6+ or Gradle 7.0+

## Project Structure
```
src/
├── main/
│   ├── java/
│   │   └── com/example/helloworld/
│   │       ├── HelloWorldApplication.java
│   │       └── HelloController.java
│   └── resources/
│       ├── application.properties
│       └── banner.txt
├── test/
│   └── java/
│       └── com/example/helloworld/
│           └── HelloWorldApplicationTests.java
```

## Running the Application

### Using Maven
```
mvn spring-boot:run
```

### Using Gradle
```
./gradlew bootRun
```

### Running Packaged JAR
```
mvn package
java -jar target/hello-world-0.0.1-SNAPSHOT.jar
```

## Endpoints

- `GET /` → "Hello, World!"
- `GET /greeting` → "Welcome to Spring Boot!"
- `GET /api/greeting` → JSON response
  - Example: `GET /api/greeting?name=Student` returns `{ "id": 1, "content": "Hello, Student!" }`

## Change Port
In `src/main/resources/application.properties`:
```
server.port=8081
```

## Custom Banner
Add ASCII art to `banner.txt` to personalize the Spring Boot startup message.

## Annotations Used

- `@SpringBootApplication`: Combines `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan`
- `@RestController`: Marks the class as a REST controller
- `@GetMapping`: Maps HTTP GET requests to handler methods
- `@RequestParam`: Binds HTTP query parameters to method arguments

## JSON Conversion
Spring Boot uses Jackson (included by default) to automatically convert Java objects returned from controller methods into JSON format.

## Benefits of Spring Boot
- Quick setup with Spring Initializr
- Embedded server (no need to deploy to external servlet containers)
- Production-ready features (metrics, health checks, etc.)
- Reduced boilerplate via auto-configuration

## Author
Generated during Spring Boot lab for hands-on learning.
