 🎓 Student Management System

A web-based platform designed for **students and administrators** to manage **academic records**, including **results, attendance, timetable, and personal profiles**. Built with **Express.js**, **MongoDB**, and **EJS**, this project offers a responsive interface for authenticated users.

## ✨ Features

### 🔐 Authentication

* Secure login using **email and password**
* Session-based authentication using `express-session`

### 📊 Academic Results

* View results for multiple semesters (`/result1`, `/result2`, `/result3`)
* Fetch data from **MongoDB collections**

### 📅 Timetable View

* Timetable based on student division

### 📋 Attendance Tracking

* Overview of attendance for all subjects
* Subject-wise attendance details via dynamic routing (`/details/:id`)

### 👤 Student Profile

* View personal and bank details
* Edit personal and banking information

---

## 🛠 **Technologies Used**

### 🔧 Backend

* **Node.js + Express.js** – Server logic and routing
* **MongoDB** – Database for storing student info, results, and attendance
* **Express Session** – Manages login sessions
* **Body-Parser** – Parses form data
* **EJS** – Server-side templating engine for rendering views

### 🗃 Database Structure

* `Student` – PersonalInfo, BankInfo, GenInfo, Username, Password
* `Result` – Contains Result array by semester
* `Attendance` – AttendanceReview by subject
* `Timetable` – Division-wise timetable

---

## 📂 **Project Structure**

```
├── server.js                 # Main Express server
├── views/                   # EJS templates (index, result, profile, edit forms)
├── public/                  # Static assets (CSS, images, etc.)
├── package.json
```

---

 🔄 How the App Works

 1️⃣ Login

* Users enter their **email and password** on `/`
* Verified via `Student` collection
* Session initialized upon successful login

2️⃣ Result Dashboard

* Accessed after login via `/result`, `/result1`, `/result2`, `/result3`
* Fetches results from the `Result` collection based on username

 3️⃣ Attendance Overview

* `/attendence` displays subject-wise attendance
* `/details/:id` shows topic-level attendance detail

 4️⃣ Timetable

* Rendered via `/timetable` using division data from `Student` and `Timetable`

 5️⃣ Profile and Editing

* `/profile` shows personal and bank info
* `/editPersonalInfo` and `/editBankDetails` allow inline editing with POST update logic

---

🚀 How to Run the Project

 📥 1. Clone the Repository

```bash
git clone https://github.com/your-username/student-management-system.git
cd student-management-system
```

 📦 2. Install Dependencies

```bash
npm install
```

 3. Start the Server

```bash
node server.js
```

Visit: [http://localhost:3000](http://localhost:3000)

---

## 🔑 **Environment & Config**

Ensure MongoDB is running locally at:

```
mongodb://localhost:27017/
```

Database used: `admin`
Collections:

* `Student`
* `Result`
* `Attendence`
* `Timetable`


 💡 **Future Enhancements**

* Role-based access (Admin/Teacher login)
* Add password hashing for improved security
* API layer for mobile app integration
* Charts for attendance visualization


---

Let me know if you'd like a PDF version of this README or if you want me to generate a `package.json` or `.env` setup for your project.
