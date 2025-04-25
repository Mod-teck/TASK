# 🎯 Objective:  
Build a small Node.js service that demonstrates your mastery of advanced concepts like TypeScript, security, caching, testing, and containerization within one working day.  

---

## 🛠 Functional Tasks:  

### **Authentication & Authorization**  
- Create a JWT system with endpoints for registration (`/auth/register`) and login (`/auth/login`).  
- Each user has a role: **USER** or **ADMIN**.  
- Secure all other endpoints based on the user's role.  

---

### **Products Module**  
- Implement full CRUD operations for products (`/products`):  
  - `GET /products` with pagination (limit + offset).  
  - `POST /products` (ADMIN only).  
  - `PUT /products/:id` (ADMIN only).  
  - `DELETE /products/:id` (ADMIN only).  
- Each product includes fields: `id`, `name`, `price`, `quantity`.  
- Apply Redis caching for `GET /products` (cache expires after 60 seconds).  

---

### **Orders Module**  
- Create a purchase order via `POST /orders` (USER only) containing a list of `{ productId, qty }`.  
- When creating an order:  
  - Verify product quantity availability in the database.  
  - Deduct the quantity from stock using transactions.  
- View order details via `GET /orders/:id` (USER only).  

---

## ⚙️ Technical Requirements:  

### **Language & Framework**  
- Node.js with TypeScript.  
- **Express** or **NestJS** (choose one).  

### **Database**  
- PostgreSQL (can be run via Docker).  
- ORM: **TypeORM** or **Sequelize**.  

### **Caching**  
- Redis (can be run via Docker).  

### **Security**  
- JWT with Passport.js or similar library.  
- Validate DTOs using **class-validator**.  

### **Rate Limiting**  
- Limit to **100 requests per IP per hour** for all endpoints using a library like **express-rate-limit**.  

### **Documentation**  
- Document the API using **Swagger** (OpenAPI).  

---

## 🧪 Testing:  

### **Unit Tests**  
- Test product and order services using **Jest** and **ts-jest**.  

### **Integration Tests**  
- Test end-to-end order creation flow using **SuperTest** and **Testcontainers** (PostgreSQL + Redis).  

---

## 🐳 Dockerization:  
- Create a **Dockerfile** for each service (app + database + Redis).  
- Create a **docker-compose.yml** file to deploy all services together:  
  - Node.js app  
  - PostgreSQL  
  - Redis  

---

## 📥 Submission:  
1. Git repository (GitHub/GitLab) with full source code.  
2. `README.md` including:  
   - Setup instructions (local and Docker).  
   - Technical decisions explained (e.g., why NestJS/Express, TypeORM/Sequelize).  
   - Usage examples (curl/Postman Collection).  
3. **Postman Collection** for API testing.  
