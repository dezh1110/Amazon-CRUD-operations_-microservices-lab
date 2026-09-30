# Amazon Product CRUD - Spring Boot

Simple Amazon-like Product CRUD application for IntelliJ IDEA.

## Requirements

- Java 17 or later
- IntelliJ IDEA
- Maven (IntelliJ can download/use the Maven wrapper configuration)

## Run

1. Open the `amazon-crud` folder in IntelliJ IDEA.
2. Wait for Maven dependencies to download.
3. Open:
   `src/main/java/com/example/amazoncrud/AmazonCrudApplication.java`
4. Run `AmazonCrudApplication`.

Server:
`http://localhost:8080`

## Postman APIs

### 1. CREATE
POST `http://localhost:8080/products`

Body -> raw -> JSON:

{
    "name": "iPhone 16",
    "category": "Electronics",
    "price": 79999,
    "quantity": 10
}

### 2. READ ALL
GET `http://localhost:8080/products`

### 3. READ BY ID
GET `http://localhost:8080/products/1`

### 4. READ BY CATEGORY
GET `http://localhost:8080/products/category/Electronics`

### 5. UPDATE
PUT `http://localhost:8080/products/1`

Body -> raw -> JSON:

{
    "name": "iPhone 16",
    "category": "Electronics",
    "price": 74999,
    "quantity": 20
}

### 6. DELETE
DELETE `http://localhost:8080/products/1`

## Project flow

Postman
   |
Controller
   |
Service
   |
Repository
   |
H2 Database

The project uses H2 so you can run it immediately without installing MySQL.
