# Library API - Spring Boot REST API

**Course:** IN3101 - Enterprise Application Development  
**Lab:** Lab Sheet 02 - Building a REST API with Spring Boot  
**Student Name:** Nadeesha Maduwantha Sugathadasa  
**Index Number:** 235108J  
**Institution:** University of Moratuwa, Faculty of Information Technology  

---

## 📌 Project Overview
A layered RESTful API built using Spring Boot and Spring Data JPA that performs CRUD operations on a `Book` resource and exposes API documentation using Swagger / OpenAPI.

### 🏛️ Architecture Layers
- **Model:** `Book` entity mapped to the database table with Jakarta validation constraints (`@NotBlank`, `@PositiveOrZero`).
- **Repository:** `BookRepository` extending `JpaRepository<Book, Long>`.
- **Service:** `BookService` encapsulating business logic.
- **Controller:** `BookController` mapping HTTP requests (`GET`, `POST`, `PUT`, `DELETE`) to service methods and returning JSON with OpenAPI annotations.

---

## 🚀 REST Endpoints

| Method | Endpoint | Description | Status Code |
|---|---|---|---|
| `GET` | `/api/books` | Retrieve all books | `200 OK` |
| `GET` | `/api/books/{id}` | Retrieve book by ID | `200 OK` / `404 Not Found` |
| `POST` | `/api/books` | Create a new book | `201 Created` / `400 Bad Request` |
| `PUT` | `/api/books/{id}` | Update an existing book | `200 OK` / `404 Not Found` |
| `DELETE` | `/api/books/{id}` | Delete a book by ID | `204 No Content` / `404 Not Found` |

---

## 📖 Swagger Documentation
Access the interactive OpenAPI Swagger UI at:
```
http://localhost:8080/swagger-ui.html
```
Raw OpenAPI description:
```
http://localhost:8080/v3/api-docs
```
