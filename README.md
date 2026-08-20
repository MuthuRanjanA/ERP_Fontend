# 🏢 JAM-ERP Frontend

> **JAM-ERP Frontend** is a modern web interface for the JAM-ERP Enterprise Resource Planning system, developed using **React.js, Vite, Bootstrap, and Axios**.

The frontend provides a user-friendly interface for managing employees, departments, payroll, assets, authentication, and other ERP operations through REST APIs.

---

## 📌 Project Overview

```text
                         ┌─────────────────────┐
                         │       JAM-ERP       │
                         │      FRONTEND       │
                         └──────────┬──────────┘
                                    │
                     ┌──────────────┼──────────────┐
                     │              │              │
                     ▼              ▼              ▼
               ┌──────────┐   ┌──────────┐   ┌──────────┐
               │   Auth   │   │Dashboard │   │  Users   │
               └──────────┘   └──────────┘   └──────────┘
                     │              │              │
                     └──────────────┼──────────────┘
                                    │
             ┌──────────────────────┼──────────────────────┐
             │                      │                      │
             ▼                      ▼                      ▼
       ┌────────────┐        ┌────────────┐        ┌────────────┐
       │ Department │        │  Payroll   │        │   Assets   │
       │ Management │        │ Management │        │ Management │
       └────────────┘        └────────────┘        └────────────┘
                                    │
                                    ▼
                            ┌──────────────┐
                            │ Spring Boot  │
                            │ REST Backend │
                            └──────────────┘
```

---

# 🚀 Features

### 🔐 Authentication

```text
                  ┌───────────────┐
                  │     Login     │
                  └───────┬───────┘
                          │
                          ▼
                  ┌───────────────┐
                  │  Login API    │
                  └───────┬───────┘
                          │
                          ▼
                  ┌───────────────┐
                  │ JWT / Session │
                  │ Authentication│
                  └───────┬───────┘
                          │
                          ▼
                  ┌───────────────┐
                  │   Dashboard   │
                  └───────────────┘
```

The frontend provides:

* Login
* Registration
* Logout
* Protected routes
* JWT-based authentication
* Role-based UI access
* Authentication state management

---

# 📊 Dashboard

The dashboard provides a centralized overview of the ERP system.

```text
┌────────────────────────────────────────────────────────┐
│                      DASHBOARD                          │
├────────────────────┬───────────────────┬───────────────┤
│                    │                   │               │
│    👥 Employees    │   🏢 Departments │   💰 Payroll  │
│                    │                   │               │
├────────────────────┴───────────────────┴───────────────┤
│                                                        │
│                    💻 Assets                           │
│                                                        │
└────────────────────────────────────────────────────────┘
```

---

# 🏢 Department Management

```text
                    Department Module
                           │
            ┌──────────────┼──────────────┐
            │              │              │
            ▼              ▼              ▼
          Create         View           Update
            │              │              │
            └──────────────┼──────────────┘
                           │
                           ▼
                         Delete
```

Features:

* Create department
* View departments
* Update department
* Delete department
* Display department information
* Connect employees with departments

---

# 👨‍💼 Employee Management

```text
                     Employee Module
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
        Create            View            Update
          │                │                │
          └────────────────┼────────────────┘
                           │
                           ▼
                         Delete
```

Features:

* Add employee
* View employee details
* Edit employee information
* Delete employee
* Display employee list
* Manage department assignment

---

# 💰 Payroll Management

```text
                      Payroll Module
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
          Employee        Salary         Payroll
           Details        Details         Records
             │              │              │
             └──────────────┼──────────────┘
                            │
                            ▼
                     Payroll Display
```

Features:

* View payroll information
* Display salary details
* Manage employee payroll records
* Connect payroll information with employees

---

# 💻 Asset Management

```text
                       Asset Module
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
           Create          View          Assign
             │              │              │
             └──────────────┼──────────────┘
                            │
                            ▼
                          Track
```

Features:

* Add assets
* View assets
* Update asset information
* Assign assets to employees
* Track assigned assets

---

# 🔄 Frontend Architecture

```text
┌────────────────────────────────────────────────────────┐
│                    React Application                    │
└───────────────────────────┬────────────────────────────┘
                            │
                            ▼
┌────────────────────────────────────────────────────────┐
│                      Components                         │
│                                                        │
│ Navbar │ Sidebar │ Forms │ Tables │ Cards │ Modals     │
└───────────────────────────┬────────────────────────────┘
                            │
                            ▼
┌────────────────────────────────────────────────────────┐
│                         Pages                           │
│                                                        │
│ Login │ Dashboard │ Employee │ Department │ Payroll    │
│                                                        │
│ Assets │ Profile │ Other Pages                         │
└───────────────────────────┬────────────────────────────┘
                            │
                            ▼
┌────────────────────────────────────────────────────────┐
│                       Services                          │
│                                                        │
│                     Axios / API                         │
└───────────────────────────┬────────────────────────────┘
                            │
                            │ HTTP Requests
                            ▼
┌────────────────────────────────────────────────────────┐
│                   Spring Boot Backend                   │
│                      REST APIs                          │
└────────────────────────────────────────────────────────┘
```

---

# 🌐 API Communication

The frontend communicates with the Spring Boot backend using **Axios**.

```text
┌──────────────────┐
│   React Page     │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│  Event / Action  │
│  Button / Form   │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Axios API Call   │
└────────┬─────────┘
         │
         │ HTTP Request
         ▼
┌──────────────────┐
│ Spring Boot API  │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│    Database      │
└────────┬─────────┘
         │
         │ JSON Response
         ▼
┌──────────────────┐
│ Axios Response   │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Update React UI  │
└──────────────────┘
```

---

# 🔐 Protected Route Flow

```text
                      User
                       │
                       ▼
                ┌──────────────┐
                │  React Router│
                └──────┬───────┘
                       │
                       ▼
                ┌──────────────┐
                │ Authentication│
                │    Check      │
                └──────┬───────┘
                       │
                ┌──────┴──────┐
                │             │
              Valid         Invalid
                │             │
                ▼             ▼
          ┌──────────┐   ┌──────────┐
          │ Protected│   │  Login   │
          │   Page   │   │   Page   │
          └──────────┘   └──────────┘
```

---

# 🛠️ Technology Stack

| Category              | Technology   |
| --------------------- | ------------ |
| Frontend Framework    | React.js     |
| Build Tool            | Vite         |
| UI Framework          | Bootstrap    |
| HTTP Client           | Axios        |
| Routing               | React Router |
| Authentication        | JWT          |
| Programming Language  | JavaScript   |
| Package Manager       | npm          |
| Backend Communication | REST API     |
| Version Control       | Git / GitHub |

---

# 📁 Project Structure

```text
JAM-ERP-FRONTEND/
│
├── public/
│
├── src/
│   │
│   ├── assets/
│   │
│   ├── components/
│   │   ├── Navbar/
│   │   ├── Sidebar/
│   │   ├── ProtectedRoute/
│   │   └── ...
│   │
│   ├── pages/
│   │   ├── Login/
│   │   ├── Register/
│   │   ├── Dashboard/
│   │   ├── Employee/
│   │   ├── Department/
│   │   ├── Payroll/
│   │   ├── Assets/
│   │   └── ...
│   │
│   ├── services/
│   │   └── api/
│   │
│   ├── constants/
│   │
│   ├── App.jsx
│   ├── main.jsx
│   └── ...
│
├── .env
├── .gitignore
├── package.json
├── package-lock.json
├── vite.config.js
└── README.md
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone <YOUR_FRONTEND_REPOSITORY_URL>
cd JAM-ERP-FRONTEND
```

## 2. Install Dependencies

```bash
npm install
```

## 3. Configure Backend URL

Create a `.env` file:

```env
VITE_BACKEND_URL=http://localhost:8080
```

> Change the backend URL according to your deployment environment.

## 4. Start Development Server

```bash
npm run dev
```

The application will normally be available at:

```text
http://localhost:5173
```

---

# 🔗 Frontend & Backend Architecture

```text
                         JAM-ERP
                            │
             ┌──────────────┴──────────────┐
             │                             │
             ▼                             ▼
      ┌─────────────┐               ┌─────────────┐
      │  FRONTEND   │               │   BACKEND   │
      │             │               │             │
      │ React + Vite│◄──── REST ───►│Spring Boot  │
      │ Bootstrap   │      API      │Spring       │
      │ Axios       │               │Security     │
      └─────────────┘               │JWT          │
                                    └──────┬──────┘
                                           │
                                           ▼
                                    ┌─────────────┐
                                    │  Database   │
                                    └─────────────┘
```

---

# 📱 Responsive UI

The frontend is designed to provide a responsive user interface for different screen sizes.

```text
┌──────────────────────────────┐
│          Desktop             │
│                              │
│  Sidebar │     Content       │
│          │                   │
└──────────────────────────────┘

┌──────────────────┐
│      Tablet      │
│                  │
│   Content Area   │
│                  │
└──────────────────┘

┌──────────────┐
│    Mobile    │
│              │
│   Content    │
│              │
└──────────────┘
```

---

# 🧪 Development

Run the development server:

```bash
npm run dev
```

Build the production version:

```bash
npm run build
```

Preview the production build:

```bash
npm run preview
```

---

# 🚀 Deployment

```text
                  ┌─────────────────┐
                  │  Source Code    │
                  │     GitHub      │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │   npm build     │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │ Production Build│
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │ Hosting Service │
                  └────────┬────────┘
                           │
                           ▼
                         Users
```

---

# 🎯 Project Objectives

* Build a modern ERP user interface
* Provide easy navigation between ERP modules
* Consume secure REST APIs
* Implement authentication and protected routes
* Provide role-based access to frontend features
* Create reusable React components
* Provide responsive UI
* Connect frontend with Spring Boot backend

---

# 🔮 Future Enhancements

```text
Current Frontend
       │
       ▼
┌──────────────────────┐
│ React + REST API     │
└──────────┬───────────┘
           │
           ▼
    Future Improvements
           │
     ┌─────┼─────┐
     │     │     │
     ▼     ▼     ▼
   Charts Notifications Advanced
   & BI     & Email   UI/UX
     │     │     │
     └─────┼─────┘
           │
           ▼
   ┌─────────────────┐
   │ Cloud Deployment│
   │ & CI/CD         │
   └─────────────────┘
```

Future improvements may include:

* Advanced dashboard charts
* Data visualization
* Improved search and filtering
* Pagination
* Notifications
* Advanced form validation
* Better mobile responsiveness
* CI/CD integration
* Cloud deployment
* Performance optimization

---

# 👨‍💻 Project Type

**Group Project — JAM-ERP**

### Development Focus

```text
Frontend
   │
   ├── React.js
   ├── Vite
   ├── Bootstrap
   ├── Axios
   ├── React Router
   └── REST API Integration
```

---

# 📜 License

This project was developed as an academic/group project for learning and demonstrating modern frontend development, REST API integration, authentication, authorization, and enterprise application development.
