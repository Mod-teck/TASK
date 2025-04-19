# Task: Build a “Software Project Management” Web Application using HTML, CSS (Tailwind), and Angular

## Description:
Design and develop a complete web application for managing software projects using **HTML**, **Tailwind CSS**, and **Angular**. The application should enable users to:

- Create new projects
- Manage tasks within each project
- Track project progress
- Add team members

The frontend should be fully dynamic and interactive.

---

## Requirements:

### 1. Frontend:

#### HTML & Tailwind CSS:
- Design a modern and elegant UI using **Tailwind CSS**
- Follow best **UX/UI** practices
- Utilize **Flexbox** and **Grid** for responsive layout
- Ensure responsiveness across all devices (mobile, tablet, desktop)

#### Angular:
- Structure app using small, reusable **components**
- Use **Angular services** for shared logic and data
- Implement **RxJS** for asynchronous operations (search, filters)
- Use **Angular Routing** to navigate between:
  - `Projects`
  - `Tasks`
  - `Team Members`

---

### 2. Core Features:

#### ✅ Project Management:
- Create new project with:
  - Project Name
  - Project Description
  - Start Date and End Date
- Display all projects with:
  - Name
  - Description
  - Progress Percentage
  - Number of Tasks
- Enable **edit** and **delete** functionality

#### ✅ Task Management:
- Add tasks within each project
- Each task includes:
  - Task Title
  - Task Description
  - Status: `In Progress`, `Completed`, `Delayed`
  - Assigned Team Member
- Allow **edit** and **delete** for tasks

#### ✅ Team Management:
- Add team members per project
- Each member includes:
  - Name
  - Role: `Project Manager`, `Developer`, `Designer`
  - Optional Profile Picture
- Display team members list per project

#### ✅ Progress Tracking:
- Display progress bar for each project based on completed tasks
- Show “Project Completed” message if all tasks are done

#### ✅ Search & Filter:
- Search for projects or tasks
- Filter projects by status:
  - `In Progress`
  - `Completed`
  - `Delayed`

---

### 3. Advanced Features:

#### 🌙 Dark Mode:
- Toggle to enable/disable **Dark Mode**
- Use **Tailwind CSS dark mode utilities**

#### 🖱️ Drag and Drop:
- Reorder tasks or move them between projects
- Use `ngx-drag-drop` for implementation

#### 🎞️ Animations:
- Animate element transitions (e.g., fade in/out tasks)
- Use **Angular Animations**

#### 📁 Export Data:
- Export project data (tasks, team) to:
  - PDF (`jsPDF`)
  - CSV (`PapaParse`)

---

### 4. Local Storage:
- Store all data (projects, tasks, team) in **LocalStorage**
- Retrieve and display saved data on app reload

---

## Creative Design Guidelines:

### 🏠 Dashboard Layout:
- Display all projects as **cards** with:
  - Project Name
  - Progress Bar
  - Completed/Incomplete Tasks count
- Prominent `+` button for new project

### 📄 Project Details Page:
- Project Info: name, description, dates
- Task list with status icons:
  - ✓ = Completed
  - ⏳ = In Progress
- Team members with roles
- “Add Task” button near tasks list

### 📊 Tables & Components:
- Responsive tables for tasks and team members
- Support **sorting** and **filtering**
- Buttons: `Edit`, `Delete`, `Change Status`

### 🔗 Navigation:
- Top Navbar with links to:
  - Dashboard
  - Projects
  - Tasks
  - Team

---

## ✨ Visual Effects:
- Use **Tailwind CSS**:
  - Light shadows
  - Rounded corners
  - Color status indicators: green, yellow, red

---

## 💡 User Experience (UX):
- Clear button/link functionality
- Confirmation dialogs for `edit`/`delete`
- Smooth drag & drop with animations
