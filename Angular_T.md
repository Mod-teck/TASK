# 🛠️ Advanced Angular E-Commerce Admin Dashboard

## 🎯 Objective:
Build an admin dashboard for managing products in an e-commerce platform. The project should demonstrate advanced Angular skills such as:

- Using **NgRx** (state management)
- Clean and scalable **project architecture** (with modules and feature folders)
- Implementing **Lazy Loading**
- Creating **Guards, Interceptors, and Services**
- Connecting to a **mock API** (JSON Server or local mock data)
- Responsive design using **Angular Material** or **Tailwind CSS**

---

## 📋 Project Details

### 1. 🔐 Login Module
- Login page using **Reactive Forms**
- Form validation
- On login, store a **fake JWT token**
- Protect routes using **AuthGuard**

---

### 2. 📊 Dashboard Module (Lazy Loaded)
- Display basic statistics:
  - Total number of products
  - Count of active and inactive products
  - Monthly orders chart (use **Chart.js** or **ngx-charts**)

---

### 3. 🛒 Products Module (Lazy Loaded)
- Product table displaying:
  - **Name**, **Price**, **Status** (active/inactive), **Category**
- Functionalities:
  - **Add**, **Edit**, **Delete** product
- Technologies:
  - **NgRx Store + Effects** for state management
  - **Reactive Forms**
  - **Dialog modals** for add/edit actions
  - **Pagination, Search, and Filter**

---

### 4. 🗂️ Categories Module (Optional)
- Manage product categories
- Reuse the structure from the **Products Module**

---

### 5. ⚙️ Settings Module
- Page for updating **user profile settings** (name, email, etc.)
- Use **Two-way data binding**

---
