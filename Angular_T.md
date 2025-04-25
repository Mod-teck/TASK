# 🎯 Objective
Build an application that demonstrates mastery of advanced Angular concepts such as complex state management, performance optimization, and clean project architecture, while adhering to best practices.

---

## 📋 Prerequisites
- Use **Angular 17+** with **TypeScript**.
- Initialize the project with **Angular CLI**.
- Apply **RxJS Operators** professionally (e.g., `switchMap`, `debounceTime`, `catchError`).
- Implement **Clean Architecture** (well-organized modules and layer separation).

---

## 📌 Functional Requirements

### 1. Users CRM System
Interactive table to display users with:
- **Pagination** or **Virtual Scroll** (choose one).
- Filter by role (**Admin/User**) + **Search** with `debounceTime` of 300ms.
- Add/Edit user using **Reactive Form** with:
  - **Custom Validator** (e.g., password strength).
  - **Async Validator** to check for unique email.
- Use **NgRx** for user state management (`Load`, `Add`, `Update`, `Delete`).

### 2. Real-time Analytics Dashboard
Display live data using **WebSocket Mock with RxJS**:
- Live visits count.
- Interactive chart using **ngx-charts** updating every 5 seconds.
- Apply **Caching Strategy** to store data for 2 minutes.

### 3. Notifications Hub
Notification service using `Subject` + `RxJS Operators`:
- Toast notifications with types: success, warning, error.
- Manage notification list with multi-select and bulk delete.
- Use a **Custom Directive** to close notifications on outside click.

---

## ⚙️ Advanced Technical Requirements

### Interceptors:
- Add **Authorization Header** via Auth service.
- **Global Error Handling** with automatic retry (3 attempts).

### Route Guards:
- **AuthGuard** for protected routes.
- **RoleGuard** to verify role-based access.

### Performance Optimization:
- Use **OnPush Change Detection Strategy**.
- Use **Standalone Components** + **Lazy Loading**.

### Custom Libraries:
- Create a **Custom Pipe** for date formatting (e.g., `5 minutes ago`).
- Shared **Utility Service** with helper functions.

---

## 🚀 Bonus Points
- Use **Angular Signals** for reactive state management.
- Advanced **Dependency Injection** (e.g., `providedIn: 'root'` vs `@Injectable()`).
- Write **Unit Tests** using Jasmine covering **85%+** of services.
- Setup a simple **CI/CD Pipeline** (tests + build) via **GitHub Actions**.

---

## 📥 Deliverables
A **GitHub Repository** containing:
- Full codebase with **json-server** setup (mock database).
- `README.md` with:
  - Project structure:
    ```bash
    src/
    ├── app/
    │   ├── core/          # Guards, Interceptors, Services
    │   ├── features/      # Modules (Users, Analytics, Notifications)
    │   ├── shared/        # Pipes, Directives, Utilities
    │   └── store/         # NgRx (Actions, Reducers, Effects)
    └── assets/           # Mock Data + Configs
    ```
  - Challenges & innovative solutions.

- (Optional) A 2-minute video explaining:
  - How the WebSocket Mock is built using RxJS.
  - Usage of the Custom Directive for notifications.
