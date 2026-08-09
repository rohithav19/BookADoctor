# 🩺 Book a Doctor - MERN Application

A complete full-stack **doctor appointment booking application** built using **MongoDB Atlas, Express.js, React.js, and Node.js (MERN)**.

The application allows patients to register and log in, browse doctors, view doctor profiles, book appointments, and manage their appointments. Doctors can manage their profiles and appointments, while administrators can manage users, doctors, and overall system activities.

---

## 🎯 Features

* **User Authentication:** Secure patient registration and login
* **Doctor Management:** View and manage doctor profiles
* **Doctor Search:** Browse doctors based on specialization and availability
* **Appointment Booking:** Patients can book appointments with available doctors
* **Appointment Management:** View and manage upcoming and previous appointments
* **Appointment Status:** Track Pending, Confirmed, Completed, and Cancelled appointments
* **Patient Dashboard:** Manage appointments and profile information
* **Doctor Dashboard:** View and manage scheduled appointments
* **Admin Dashboard:** Manage users, doctors, and appointments
* **Medical Documents:** Support for managing relevant patient documents
* **Role-Based Access:** Separate access for Patients, Doctors, and Administrators
* **Responsive Design:** User-friendly interface for different screen sizes

---

# 🛠️ Tech Stack

## Frontend

* React.js
* Vite
* React Router DOM
* Axios
* CSS3
* JavaScript

## Backend

* Node.js
* Express.js
* MongoDB Atlas
* Mongoose
* JWT Authentication
* CORS
* dotenv

---

# 📋 Prerequisites

Before running the project, make sure the following are installed:

* **Node.js** (v16 or higher)
* **npm**
* **MongoDB Atlas account**
* **Visual Studio Code**
* **Google Chrome or any modern web browser**

---

# 🚀 Installation

## 1. Download or Clone the Project

Open the project folder in Visual Studio Code.

```bash
git clone <your-repo-url>
cd Book-A-Doctor
```

---

## 2. Install Backend Dependencies

Navigate to the server directory:

```bash
cd server
npm install
```

---

## 3. Install Frontend Dependencies

Open another terminal or navigate back to the project root:

```bash
cd ../frontend
npm install
```

---

# ⚙️ Configuration

## Server `.env`

Create a `.env` file inside the **server** folder.

```env
PORT=5000
MONGO_URI=your_mongodb_atlas_connection_string
JWT_SECRET=your_secret_key
```

The `MONGO_URI` contains the connection string obtained from **MongoDB Atlas**.

> **Important:** Do not upload the `.env` file to GitHub because it contains sensitive configuration information.

---

# 🎮 Running the Application

The application can be run locally using separate frontend and backend development servers.

## Terminal 1 - Start Backend

```bash
cd server
npm run dev
```

If Nodemon is not configured, use:

```bash
node server.js
```

The backend server normally runs at:

**http://localhost:5000**

---

## Terminal 2 - Start Frontend

```bash
cd frontend
npm run dev
```

The React development server normally runs at:

**http://localhost:5173**

Open the frontend URL in your browser to access the **Book a Doctor** application.

---

# 👥 User Roles

### 👩‍⚕️ Patient

Patients can:

* Register and log in
* Browse available doctors
* View doctor profiles
* Select available appointment slots
* Book appointments
* View upcoming appointments
* View previous appointments
* Track appointment status
* Manage their profile

### 👨‍⚕️ Doctor

Doctors can:

* Log in to their account
* Manage their profile
* View scheduled appointments
* View relevant patient information
* Manage appointment availability
* Update appointment status
* Mark appointments as completed or cancelled

### 👨‍💼 Administrator

Administrators can:

* Manage patient accounts
* Manage doctor accounts
* Verify doctor information
* Monitor appointments
* Manage system activities
* Monitor overall platform operations

---

# 📅 Appointment Workflow

The basic appointment workflow is:

```text
Patient Registration
        ↓
Patient Login
        ↓
Browse Doctors
        ↓
Select Doctor
        ↓
View Available Slots
        ↓
Book Appointment
        ↓
Appointment Confirmation
        ↓
Doctor Reviews Appointment
        ↓
Appointment Status Updated
        ↓
Consultation Completed
```

---

# 📚 API Endpoints

## User Routes

```text
POST /api/users/register
POST /api/users/login
GET  /api/users/profile
PUT  /api/users/profile
```

## Doctor Routes

```text
GET  /api/doctors
GET  /api/doctors/:id
POST /api/doctors
PUT  /api/doctors/:id
DELETE /api/doctors/:id
```

## Appointment Routes

```text
POST /api/appointments
GET  /api/appointments
GET  /api/appointments/:id
PUT  /api/appointments/:id
DELETE /api/appointments/:id
```

> The exact endpoint names may vary depending on the routes implemented in the project.

---

# 📁 Project Structure

```text
BOOK-A-DOCTOR/
│
├── server/
│   ├── config/
│   │   └── db.js
│   │
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── doctorController.js
│   │   └── appointmentController.js
│   │
│   ├── middleware/
│   │   ├── auth.js
│   │   └── errorHandler.js
│   │
│   ├── models/
│   │   ├── User.js
│   │   ├── Doctor.js
│   │   └── Appointment.js
│   │
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── doctorRoutes.js
│   │   └── appointmentRoutes.js
│   │
│   ├── .env
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── public/
│   │
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── assets/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   │
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

# 🗄️ Database

The application uses **MongoDB Atlas** as the cloud database.

The main collections include:

* **Users** – Stores patient and user account information
* **Doctors** – Stores doctor profiles and availability
* **Appointments** – Stores appointment and booking information
* **Medical Documents** – Stores information related to uploaded patient documents, when implemented

**Mongoose** is used to define schemas and communicate between the Node.js backend and MongoDB Atlas.

---

# 🔐 Authentication and Security

The application uses authentication mechanisms to protect user accounts and restricted resources.

Security features include:

* User authentication
* JWT-based authorization, when implemented
* Password protection
* Role-based access
* Protected API routes
* Environment variables for sensitive configuration
* CORS configuration

---

# 🖥️ Main Application Pages

The application includes the following major pages:

* **Landing/Home Page**
* **Login Page**
* **Registration Page**
* **Doctors Page**
* **Doctor Profile Page**
* **Appointment Booking Page**
* **My Appointments Page**
* **Patient Dashboard**
* **Doctor Dashboard**
* **Admin Dashboard**
* **Profile Page**

---

# 🧪 Testing

The following functionalities can be tested:

* User registration
* User login and logout
* Doctor listing
* Doctor profile viewing
* Appointment booking
* Appointment status updates
* Patient appointment history
* Doctor appointment management
* Admin operations
* MongoDB Atlas database operations
* Protected routes and authentication

---

# 🤝 Contributing

Contributions and improvements are welcome. The project can be extended with additional features such as online payment, video consultation, doctor reviews, prescriptions, reminders, and notifications.

---

# 📝 License

This project is developed for **educational and academic purposes**.

---

# 📧 Support

For issues or questions related to the project, please check the project documentation or contact the project developer.

---

**🩺 Book a Doctor — Making Doctor Appointment Booking Simple and Convenient!**
