# Project & Team Management Web App

## 📋 Task

Build a **Project & Team Management** web application using **HTML, CSS, JavaScript, and React** (no backend).

---

## 🧾 Description

The objective is to design and develop a complete **Project & Team Management** web application that allows users to:

- ✅ Create and manage projects  
- 👥 Add team members to each project  
- 📝 Assign tasks to team members  
- 📊 Track the progress of each project  

All data will be stored **locally using Local Storage**, ensuring data persistence without the need for a backend server.

---

## 🚧 Requirements

### 1. Frontend Development

#### HTML & CSS

- Design a **modern and clean UI**
- Use **Flexbox** or **CSS Grid** for layout
- Ensure full **responsiveness** on all devices
- Apply **eye-friendly colors** and **readable fonts**

#### React

- Break the app into **small, reusable components**
- Use **React Hooks** (`useState`, `useEffect`) for state and interactivity
- Organize code in **separate files per component**

---

### 2. Core Features

#### 🗂️ Project Management

- Create new projects (name + description)
- List all projects with:
  - Name
  - Description
  - Number of tasks
  - Progress status
- Edit and delete existing projects

#### 👨‍👩‍👧‍👦 Team Management

- Add team members to each project
- Each member has:
  - Name
  - Role (e.g., Manager, Developer, Designer)
- Display a list of team members per project

#### ✅ Task Management

- Create tasks within each project with:
  - Task title
  - Description
  - Start date & due date
  - Status (In Progress / Completed)
  - Assigned member (from the team)
- Edit and delete tasks

#### 📈 Progress Tracking

- Show a **progress bar** per project based on completed tasks
- Show a **completion message** if all tasks are completed

#### 🔍 Search & Filter

- Search bar for projects/tasks
- Filter projects by status:
  - In Progress
  - Completed

---

### 3. 🗃️ Local Storage Integration

- Store all data in **Local Storage**:
  - Projects
  - Team Members
  - Tasks
- On page reload, retrieve and display saved data correctly

---

### 4. 🌟 Optional Enhancements

- **Drag and Drop**: Reorder or move tasks between projects
- **Animations**: Smooth effects for adding/deleting elements (e.g., fade in/out)
- **Dark Mode**: Light/Dark theme toggle

---

## 🚀 Technologies

- HTML5
- CSS3 (Flexbox / Grid)
- JavaScript (ES6+)
- React (Hooks)

---

## 🧠 Notes

This project is **frontend-only** and focuses on UI/UX and state management using React and Local Storage.

