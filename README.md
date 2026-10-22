# Student Manager

A student registration web application built with Spring Boot, Spring Data JPA, Thymeleaf, and H2. It supports creating, viewing, editing, and deleting student records.

## Requirements

- Java 21
- No separate Maven installation is required; this project includes the Maven Wrapper.

## Run the application

From the project root in PowerShell:

```powershell
.\mvnw.cmd spring-boot:run
```

Open [http://localhost:8081](http://localhost:8081) in your browser.

To stop the application, press `Ctrl+C` in the terminal.

## Features

- Register students and view all registered students.
- Edit or delete student records.
- Validate student name, email, phone number, course, and age.
- Prevent duplicate email addresses.
- Persist data in a local H2 database.

Student age must be between 15 and 100. The available courses are Computer Science, Software Engineering, Data Science, Statistics, and Information Systems.

## Database console

The H2 web console is available at [http://localhost:8081/h2-console](http://localhost:8081/h2-console) while the application is running.

Use the following connection settings:

| Setting | Value |
| --- | --- |
| JDBC URL | `jdbc:h2:file:./data/studentdb` |
| User Name | `sa` |
| Password | Leave blank |

The database files are stored in the `data` directory relative to the project. These console credentials and settings are intended for local development; do not expose the console or use the default credentials in a production deployment.

## Tests

Run the test suite with:

```powershell
.\mvnw.cmd test
```

## Build

Package the application with:

```powershell
.\mvnw.cmd package
```

The executable JAR is created under `target`.
