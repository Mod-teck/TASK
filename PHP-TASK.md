# E-Commerce Backend Requirements

**Level:** Senior / Advanced

## Basic Requirements

### 1. Multi-Tenancy (Advanced Scoping)
- Each **User** has their own set of **Products** and **Orders**.  
- Use **Eloquent Global Scopes** or **Traits** to ensure each user only sees their own products and orders.

### 2. API Authentication & Roles
- Authentication using **Laravel Sanctum** (API Tokens).  
- **Roles** (via Spatie **laravel-permission**):
  - **Admin**: can create/update/delete **any** product.  
  - **Customer**: can create orders and view **only** their own orders.

### 3. Caching & Performance
- Cache the product list in **Redis** for **15 minutes**.  
- Automatically clear/refresh the cache on product update/delete.  
- Optionally use **laravel-model-caching**.

### 4. Queue & Background Jobs
- On order creation, send an email notification to the user using **Laravel Notifications**, queued via **Redis Queue**.  
- Add retry logic (3 attempts) for the notification job on failure.

### 5. Validation & Error Handling
- Use **Form Request** classes for validating product & order data.  
- Add a **Custom Validation Rule** to ensure ordered quantity ≤ available product quantity.  
- Handle errors via exceptions and return a **unified JSON response** structure.

### 6. Testing
- Write **Feature Tests** (with Pest PHP) covering:
  - Order creation with product interaction.  
  - Admin vs. Customer permissions.  
- *(Bonus)* Enable **Parallel Testing** to speed up tests.

---

## Bonus Requirements

1. **API Documentation**: Generate Swagger/OpenAPI docs (e.g. using **L5-Swagger**).  
2. **Real-Time Updates**: Notify users of order status changes in real time with **Laravel Echo** + WebSockets.  
3. **Admin Dashboard**: Simple dashboard (Blade or Inertia.js) showing stats (product count, order count).  
4. **CI/CD**: Add `.github/workflows/laravel.yml` to run tests automatically.  
5. **Monitoring**: Use **Laravel Telescope** for performance/error monitoring.

---

## Database Schema

```sql
-- products table
CREATE TABLE products (
  id         BIGINT UNSIGNED PRIMARY KEY,
  name       VARCHAR(255) NOT NULL,
  price      DECIMAL(10,2) NOT NULL,
  quantity   INT NOT NULL,
  user_id    BIGINT UNSIGNED NOT NULL,
  FOREIGN KEY (user_id) REFERENCES users(id)
);

-- orders table
CREATE TABLE orders (
  id          BIGINT UNSIGNED PRIMARY KEY,
  user_id     BIGINT UNSIGNED NOT NULL,
  total_price DECIMAL(10,2) NOT NULL,
  status      VARCHAR(50)    NOT NULL,
  FOREIGN KEY (user_id) REFERENCES users(id)
);

-- order_items table
CREATE TABLE order_items (
  id         BIGINT UNSIGNED PRIMARY KEY,
  order_id   BIGINT UNSIGNED NOT NULL,
  product_id BIGINT UNSIGNED NOT NULL,
  quantity   INT NOT NULL,
  FOREIGN KEY (order_id)   REFERENCES orders(id),
  FOREIGN KEY (product_id) REFERENCES products(id)
);
