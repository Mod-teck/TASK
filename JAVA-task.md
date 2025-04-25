# 🎯 Objective
Build a simple **Order Management System** using Spring Boot that showcases advanced concepts.  
**Level:** Senior / Advanced

---

## 📋 Basic Requirements

### Microservices Architecture  
- Create **two separate** Spring Boot applications:
  1. **Product Service**  
     - Manage products (CRUD) with fields: `id`, `name`, `price`, `quantity`.
  2. **Order Service**  
     - Manage orders (create order, get order details) linked to products by `id`.  

- Services communicate with each other via **OpenFeign** or **WebClient**.

---

## 🔐 Security & JWT Authentication  
- Add authentication using **JWT**.  
- **`/products`** create/update endpoints: accessible **only** to users with **ADMIN** role.  
- **`/orders`** create endpoint: accessible **only** to users with **USER** role.  
- Implement using **Spring Security** + **JWT**.

---

## 🔄 Resilience & Fault Tolerance  
In **Order Service**, use **Resilience4j** (or **Hystrix**) to add:  
- **Circuit Breaker** when calling Product Service.  
- **Retry Mechanism** (e.g., 3 retries on failure).

---

## 💾 Database  
- **Product Service**:  
  - Use **H2** (for development)  
  - Use **Flyway** for migrations to create the `products` table.  
- **Order Service**:  
  - Use **PostgreSQL** (e.g., via Docker)  
  - Define `orders` and `order_items` tables.  
- Use **Spring Data JPA** + **Hibernate** in both services.

---

## 🧪 Testing  
- **Unit Tests** for Product Service using **Mockito**.  
- **Integration Test** for creating an order using **Testcontainers**.

---

## 🐳 Dockerization  
- Create a **Dockerfile** for each service.  
- **(Bonus)** Provide a **docker-compose.yml** to run:
  - Product Service
  - Order Service
  - Databases
  - Netflix Eureka (Service Discovery)

---

## 🎁 Additional (Bonus) Requirements  
- **API Documentation**: Swagger / OpenAPI  
- **Advanced Logging**: Logback or simple ELK Stack  
- **Validation**: DTO validation (e.g., product price must be non-negative)  
- **Messaging**: Send an event via Kafka or RabbitMQ when product quantity changes

---

## 📥 Deliverables  
1. **Source code** in a Git repository.  
2. **README.md** including:
   - Instructions to run the project.
   - Architectural decisions (e.g., why Resilience4j over Hystrix?).  
3. **Postman Collection** for testing the APIs.
