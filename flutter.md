## 🚀 Functional Requirements

1. **Authentication Flow**  
   - **Login Screen**: Username/password authentication against a mock endpoint.  
   - **Secure Token Storage**: Save the JWT (or dummy token) securely on the device.

2. **Product Catalog**  
   - Fetch a paginated list of products from a REST API (mock JSON server).  
   - Each product has: `id`, `name`, `price`, `imageUrl`.  
   - Display in a scrollable **Grid** or **List** with pull-to-refresh and infinite-scroll pagination.

3. **Product Details**  
   - Tap a product to navigate to a details screen with a **Hero animation** on the image.  
   - Show extended info: description, availability, and an “Add to Favorites” toggle.

4. **Favorites Management**  
   - Mark/unmark favorites.  
   - Persist favorites locally (Hive or SharedPreferences).  
   - Separate “Favorites” tab to view saved items.

5. **Search & Filter**  
   - Search by name with `debounceTime` of **300ms**.  
   - Filter by price range via a custom slider UI.

---

## ⚙️ Technical Requirements

- **State Management**: Riverpod or BLoC (candidate’s choice).  
- **Networking**: Dio or http with structured error handling + retry logic.  
- **Local Storage & Caching**: Hive (or Sembast/SharedPreferences) to cache product list for offline use.  
- **Dependency Injection**: get_it or Riverpod’s built-in DI.  
- **Routing**: AutoRoute or Navigator 2.0 (deep-linking optional).  
- **Clean Architecture**: Separate into `data`, `domain`, and `presentation` layers.

---

## ✨ Advanced Touches

- **Animations**: Hero + custom page transition.  
- **Offline Support**: Show cached data when offline, with a “stale data” banner.  
- **Form Validation**: Use Formz or reactive_forms for login form.  
- **Dark Mode**: Fully support light/dark themes.  

---

## 🧪 Testing

- **Unit Tests**: Domain layer (use cases + models).  
- **Widget Tests**: Login screen, product list, detail page.  
- **Integration Test**: Full login → fetch products → view details (using `integration_test`).

---

## 🐳 Docker (Optional)

- Include a `docker-compose.yml` to spin up the mock JSON server (e.g. json-server) with sample product data.

---

## 📥 Deliverables

1. **GitHub Repo** with all source code.  
2. **README.md** detailing:
   - Setup instructions (Flutter SDK version, how to run mock API).  
   - Architectural decisions (why Riverpod/BLoC, Dio/http, Hive/SharedPreferences, etc.).  
   - How to run tests & (optional) CI instructions.  
3. **Postman Collection** (or simple curl examples) for the mock API.

---
