# Student Management API

A REST API for managing student records, built with Java, Spring Boot, Spring Data JPA, and Maven.

## Features

- Create, list, retrieve, update, and delete student records
- Persistence through Spring Data JPA
- Maven Wrapper for repeatable build and run commands

## Requirements

- Java version configured by the project (see `pom.xml`)
- A relational database configured in `src/main/resources/application.properties`

## Run locally

```bash
./mvnw clean install
./mvnw spring-boot:run
```

On Windows, use `mvnw.cmd` in place of `./mvnw`.

## API

The application exposes these endpoints:

| Method | Path | Purpose |
|---|---|---|
| `GET` | `/api/students` | List students |
| `GET` | `/api/students/{id}` | Retrieve one student |
| `POST` | `/api/students` | Create a student |
| `PUT` | `/api/students/{id}` | Update a student |
| `DELETE` | `/api/students/{id}` | Delete a student |

Use the `Student` model in `src/main/java/com/bluesky/student_api/model/Student.java` as the request and response shape. Configure the database connection before starting the application.

## Project structure

- `controller/` — HTTP endpoints
- `service/` — student operations
- `repository/` — Spring Data persistence
- `model/` — student entity
- `src/test/` — application test source

## Current scope

This repository provides the CRUD foundation. Validation, centralized error responses, pagination, and generated API documentation are not currently described as implemented features.