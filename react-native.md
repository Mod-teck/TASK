## 🚀 Functional Requirements

1. **Authentication Flow**  
   - **Sign In / Sign Up Screens** using email/password against a mock REST endpoint.  
   - Securely store a dummy JWT (or token) with **AsyncStorage** or **SecureStore**.

2. **Item Catalog**  
   - Fetch a paginated list of items (e.g. products) from a mock API (you can run a `json-server` or similar).  
   - Display in a scrollable **FlatList** with **infinite scroll** and **pull-to-refresh**.  
   - Each item: `id`, `title`, `thumbnailUrl`.

3. **Item Details & Favorites**  
   - Tap an item to navigate to a **Details** screen with a **shared element** (Hero) animation on the thumbnail.  
   - Show full info: `title`, `description`, `price`.  
   - “Add to Favorites” toggle persists locally; Favorites appear on a separate tab.

4. **Offline Caching & Sync**  
   - Cache item list and details with **realm** or **SQLite** so the app works offline.  
   - When online again, sync new data in background (show a “syncing” indicator).

5. **Push Notifications Stub**  
   - Integrate a dummy **Push Notification** handler (use `react-native-push-notification` or equivalent) to schedule a local notification 5 seconds after a button press.

---

## ⚙️ Technical Requirements

- **Language & Framework**:  
  - React Native (>=0.70) with **TypeScript**  
- **State Management**:  
  - **Redux Toolkit** with **Redux Saga** or **React Query** for data-fetching/state.  
- **Navigation**:  
  - React Navigation (v6) with **Bottom Tabs** + **Stack**.  
- **Animations**:  
  - **Reanimated 2** + **React Navigation Shared Element** (for Hero animation).  
- **Dependency Injection** (optional):  
  - **tsyringe** or **InversifyJS**.  
- **Form Handling & Validation**:  
  - **React Hook Form** + **Yup** for auth forms.  
- **Networking**:  
  - Axios with global error interceptor + retry logic (e.g. axios-retry).  
- **Offline DB**:  
  - Realm or SQLite (via `react-native-sqlite-storage`).  
- **Push Notifications**:  
  - Setup a local notification schedule (no server required).

---

## 🧪 Testing

1. **Unit Tests**  
   - Services, reducers, sagas/queries using **Jest** & **React Native Testing Library**.  
2. **Component & Integration Tests**  
   - Snapshot & behavior tests for Login, Item List, Detail screen.  
3. **End-to-End** (Bonus)  
   - Use **Detox** or **Appium** for a simple login → load list → open details scenario.

---

## 🐳 (Optional) Mock API

- Provide a `docker-compose.yml` or makefile to run a **json-server** with sample item data on port 3001.

---

## 📥 Deliverables

1. **GitHub Repository**  
   - Complete source code in a public or private repo.  
2. **README.md**  
   - Setup instructions (SDK versions, how to run mock API).  
   - Architectural decisions (why Redux Toolkit/Saga vs React Query, Realm vs SQLite, etc.).  
   - How to run tests and (optional) CI pipeline.  
3. **Postman Collection** or sample **curl** commands for the mock API.
