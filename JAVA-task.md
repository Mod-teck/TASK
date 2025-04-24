# ✅ Advanced Java Spring Boot – Task Management API

## 🎯 Objective
Build a complete **REST API** for managing tasks assigned to different users. The system should include:

- **JWT-based authentication**
- Full **CRUD functionality**
- **Filtering, sorting, and pagination**
- **Clean, modular architecture**
- Optional **API documentation**

---

## 📋 Project Details

### 1. ✅ User Authentication (Spring Security + JWT)
- Register a new user
- Login and receive a **JWT token**
- Secure all protected endpoints using **JWT**

---

### 2. 📦 Tasks API
Implement full **CRUD** operations for tasks with the following fields:

- `title`
- `description`
- `status` (e.g., TODO, IN_PROGRESS, DONE)
- `priority` (e.g., LOW, MEDIUM, HIGH)
- `dueDate`
- `createdAt`
- `userId`

#### Features:
- Only the task **owner** can update or delete it
- Support for:
  - **Pagination**
  - **Filtering** (by status, date, etc.)
  - **Sorting** (by priority, createdAt, etc.)

---

### 3. ⚙️ Architecture
Use the following technologies:

- **Spring Boot 3+**
- **Spring Data JPA**
- **Spring Security + JWT**
- **MapStruct** or **ModelMapper**
- **Lombok**
- **H2** (in-memory) or **PostgreSQL**

#### Suggested Folder Structure:
- `controller/`
- `service/`
- `repository/`
- `dto/`
- `entity/`
- `exception/`

---

### 4. 🔒 Security
- Implement **Role-Based Access Control** (RBAC)
  - Regular user: can access only their own tasks
  - Admin user: can view all tasks

---

### 5. 🧪 Testing
Include tests using **JUnit 5** and **Mockito**:

- Unit tests for services and authentication
- Integration tests for major endpoints

---

### 6. 📝 Extras (Optional)
- Generate API documentation with **Swagger/OpenAPI**
- Include a `README.md` with:
  - How to run the project
  - Postman collection or example cURL requests

---

