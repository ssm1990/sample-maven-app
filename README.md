# Sample Maven App

A simple Java application built with Maven, featuring modern unit testing with JUnit 5.

## Features

- **Java 17**: Configured to use modern Java features.
- **JUnit 5**: Migrated from legacy JUnit 3 for robust unit testing.
- **Maven Shade Plugin**: Configured to create an "Uber-JAR" (fat JAR) containing all dependencies.
- **Security & Quality**: Includes plugins for OWASP Dependency Check, Checkstyle, and SpotBugs.

## Prerequisites

- **Java JDK 17** or higher.
- **Apache Maven 3.9.x** or higher.

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/ssm1990/sample-maven-app.git
cd sample-maven-app
```

### 2. Build the project
To compile the code and package it into a JAR file:
```bash
mvn clean package
```
This will generate an executable "Uber-JAR" in the `target/` directory:
- `enterprise-app-1.0.0.jar`: The fat JAR containing all dependencies and configured with a `Main-Class`.

> [!NOTE]
> The `maven-shade-plugin` is configured to replace the original artifact with the shaded one.

### 3. Run the application
You can run the application using the generated JAR:
```bash
java -jar target/enterprise-app-1.0.0.jar
```

### 4. Run Tests
To execute the unit tests:
```bash
mvn test
```

## License
This project is open-source and available under the MIT License.
