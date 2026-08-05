# 🚀 Full-Stack Project Management Platform

A robust, full-stack project management and tracking platform designed for educational and organizational environments. This system features strict Role-Based Access Control (RBAC), real-time agile project boards, and an end-to-end evaluation engine, all powered by React, Tailwind CSS, and Firebase.

---

## ✨ Key Features

### 🛡️ Dual Role-Based Access Control (RBAC)
*   **Administrator Suite:** Complete control over project creation, student enrollment tracking, and performance evaluation.
*   **Student Suite:** An interactive dashboard for discovering available projects, enrolling, and managing tasks via an Agile Kanban interface.

### 📊 Interactive Agile Project Board
*   **Kanban Interface:** Students can visually manage their project workflows with drag-and-drop or state-based task tracking (e.g., To Do, In Progress, Review, Done).
*   **Real-Time Synchronization:** Powered by Firebase Realtime Database / Firestore, ensuring all team members and admins see updates instantly.
*   **Task Lifecycle Management:** Track individual tasks from creation to completion within specific project scopes.

### 📈 End-to-End Evaluation & Reporting Engine
*   **Modal-Driven Grading:** Admins can quickly assess student submissions and assign grades using the dedicated `GradeModal` interface without leaving their workflow.
*   **Analytical Dashboards:** The `ReportsSection` provides high-level insights into class progress, project completion rates, and overall performance metrics.
*   **Comprehensive Tracking:** Detailed views of individual student performance (`StudentsSection`) and overarching project health (`ProjectsSection`).

### ⚡ Modern Component-Driven Architecture
*   **React.js (Vite):** Lightning-fast development and optimized production builds.
*   **Tailwind CSS:** Responsive, utility-first styling ensuring sub-second UI rendering and a seamless experience across desktop and mobile devices.
*   **React Router:** Fluid, Single-Page Application (SPA) navigation without page reloads.

---

## 🛠️ Technology Stack

*   **Frontend Framework:** React.js (Bootstrapped with Vite)
*   **Styling:** Tailwind CSS
*   **Routing:** React Router DOM
*   **Backend & BaaS:** Firebase (Authentication, Firestore/Realtime DB)
*   **Icons:** Lucide React (or similar)
*   **State Management:** React Context API / Hooks

---

## 📂 Project Structure

```text
frontend/
├── src/
│   ├── components/
│   │   ├── AdminDashboard/       # Admin-specific modules
│   │   │   ├── AddProjectModal.jsx
│   │   │   ├── AdminDashboard.jsx
│   │   │   ├── DashboardContent.jsx
│   │   │   ├── GradeModal.jsx
│   │   │   ├── ProjectDetailsModal.jsx
│   │   │   ├── ProjectDetailsPage.jsx
│   │   │   ├── ProjectsSection.jsx
│   │   │   ├── ReportsSection.jsx
│   │   │   ├── Sidebar.jsx
│   │   │   └── StudentsSection.jsx
│   │   ├── Navigation/           # Global navigation components
│   │   │   ├── Navbar.jsx
│   │   │   └── Sidebar.jsx
│   │   ├── StudentDashboard/     # Student-specific modules
│   │   │   ├── Dashboard.jsx
│   │   │   ├── EnrollProject.jsx
│   │   │   └── ProjectBoard.jsx  # Kanban interface
│   │   └── ui/                   # Reusable UI components (buttons, inputs, etc.)
│   ├── App.jsx                   # Main application routing & layout
│   ├── firebaseconfig.js         # Firebase initialization
│   ├── index.css                 # Global Tailwind styles
│   └── main.jsx                  # React DOM rendering entry point
├── package.json
├── tailwind.config.js
└── vite.config.js
```

---

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   **Node.js:** Ensure you have Node.js installed (v16 or higher recommended).
*   **Firebase Account:** You will need a Firebase project set up with Authentication and Firestore/Realtime Database enabled.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Mugen47/Project-Management-Tool.git
    cd Project-Management-Tool/frontend
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```

3.  **Configure Firebase:**
    *   Go to your Firebase Console and grab your project's configuration object.
    *   Open `src/firebaseconfig.js` (or create a `.env` file if you are using environment variables) and paste your credentials:
    ```javascript
    // src/firebaseconfig.js example
    import { initializeApp } from "firebase/app";

    const firebaseConfig = {
      apiKey: "YOUR_API_KEY",
      authDomain: "YOUR_AUTH_DOMAIN",
      projectId: "YOUR_PROJECT_ID",
      storageBucket: "YOUR_STORAGE_BUCKET",
      messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
      appId: "YOUR_APP_ID"
    };

    const app = initializeApp(firebaseConfig);
    export default app;
    ```

4.  **Start the development server:**
    ```bash
    npm run dev
    # or
    yarn dev
    ```

5.  **Access the application:** Open your browser and navigate to `http://localhost:5173` (or the port specified by Vite).

---

## 📝 Usage

*   **Admin Login:** Create an admin account via Firebase console or sign up and manually assign admin claims/roles in your database. Log in to access the Admin Dashboard to create projects and grade students.
*   **Student Login:** Sign up as a standard user. Navigate to the `EnrollProject` tab to join an active project. Use the `ProjectBoard` to manage tasks dynamically.

---

## 👨‍💻 Author

*   **Mugen47** - *Initial work* - [GitHub Profile](https://github.com/Mugen47)
