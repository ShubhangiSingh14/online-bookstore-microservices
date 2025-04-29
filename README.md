# Online Bookstore Microservices

This is a Spring Boot-based **Online Bookstore** project using a **Microservices architecture**, where each service is independently deployable and connected via **Eureka Discovery Server**.

## Modules

- **book-service**: Manages book catalog (title, author, price)
- **order-service**: Handles customer orders (book ID, quantity, total price)
- **discovery-server**: Eureka Service Registry where services register themselves

## Tech Stack

- Java 21
- Spring Boot 3
- Spring Data JPA
- Spring Eureka Discovery Server
- MySQL 8
- REST APIs
- Postman (for API testing)
- Git, GitHub

## Prerequisites

- Java 21
- Maven
- MySQL Server running (with `bookdb` and `orderdb` created)
- Spring Tool Suite / Eclipse IDE
- Git installed

## How to Run

1. **Start MySQL Server**
   - Ensure `bookdb` and `orderdb` exist with required tables
   - Use Workbench or CLI to check

2. **Start Services in Order**:
   - `discovery-server` on port **8761**
   - `book-service` on port **8081**
   - `order-service` on port **8082**

3. **Access URLs**:
   - Eureka: [http://localhost:8761](http://localhost:8761)
   - Book API: `http://localhost:8081/books`
   - Order API: `http://localhost:8082/orders`

4. **Use Postman** to test endpoints:

   - `POST http://localhost:8081/books`  
     ```json
     {
       "title": "Spring Boot in Action",
       "author": "Craig Walls",
       "price": 600
     }
     ```

   - `POST http://localhost:8082/orders`  
     ```json
     {
       "bookId": 1,
       "quantity": 2,
       "totalPrice": 1200
     }
     ```

## Author

- Shubhangi

## License

This project is for learning purposes.
