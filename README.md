# DecodeLab-Internship-Week3
# 🔐 Node.js Authentication & CRUD API (Express + Sequelize + JWT)

This project is a backend REST API built using Node.js, Express, Sequelize ORM, and SQLite. It provides full CRUD operations for users along with secure authentication using bcrypt for password hashing and JWT (JSON Web Tokens) for login sessions. It also includes protected routes using middleware to ensure only authenticated users can access certain endpoints.

---

## 🚀 Features

- User registration with password hashing (bcrypt)
- User login with JWT authentication
- Protected route using middleware
- Full CRUD operations (Create, Read, Update, Delete)
- SQLite database with Sequelize ORM
- Input validation and error handling
- Token-based authentication system

---

## 🛠️ Tech Stack

- Node.js
- Express.js
- Sequelize ORM
- SQLite
- bcrypt.js
- JSON Web Token (JWT)
- dotenv

---

## 📁 Project Structure

server.js → Main backend file containing all routes and logic  
database.sqlite → SQLite database file (auto-generated)

---

## ⚙️ Installation & Setup

### 1. Clone the repository
git clone <your-repo-link>  
cd <project-folder>

### 2. Install dependencies
npm install

### 3. Create .env file
JWT_SECRET=your_secret_key_here

### 4. Run the server
node server.js

Server will run at:
http://localhost:3000

---

## 📌 API Endpoints

### 🟢 Test Route
GET /

Response:
{
  "message": "API with DB Connected"
}

---

## 👤 User CRUD Routes

### ➕ Create User
POST /users  
{
  "name": "Ali",
  "email": "ali@example.com"
}

---

### 📥 Get All Users
GET /users

---

### 📥 Get User by ID
GET /users/:id

---

### ✏️ Update User
PUT /users/:id  
{
  "name": "Updated Name",
  "email": "updated@example.com"
}

---

### ❌ Delete User
DELETE /users/:id

---

## 🔐 Authentication Routes

### 📝 Register User
POST /register  
{
  "name": "Ali",
  "email": "ali@example.com",
  "password": "123456"
}

Response:
{
  "id": 1,
  "name": "Ali",
  "email": "ali@example.com"
}

---

### 🔑 Login User
POST /login  
{
  "email": "ali@example.com",
  "password": "123456"
}

Response:
{
  "message": "Login successful",
  "token": "JWT_TOKEN_HERE"
}

---

## 🔒 Protected Route

### 👤 Get Profile
GET /profile

Headers:
Authorization: Bearer YOUR_TOKEN_HERE

Response:
{
  "message": "Protected profile data",
  "user": {
    "id": 1,
    "name": "Ali",
    "email": "ali@example.com"
  }
}

---

## 🧠 How It Works

- User registers and password is hashed using bcrypt
- User logs in and server verifies credentials
- JWT token is generated on successful login
- Token is sent in Authorization header
- Middleware verifies token before accessing protected routes

---

## ⚠️ Error Handling

- 400 → Missing required fields
- 401 → Unauthorized or invalid token
- 404 → User not found
- 409 → Duplicate email
- 500 → Server error

---

## 📌 Learning Outcomes

This project demonstrates:
- REST API development
- Database integration using ORM
- Authentication and authorization
- Middleware usage in Express
- Secure password handling
- JWT-based authentication system

---

## ⭐ Future Improvements

- Role-based authentication (Admin/User)
- Refresh token system
- Pagination and filtering
- MVC architecture (controllers, routes, models)
- Deployment on cloud platforms (Render/Railway)

---

## 👨‍💻 Author

Backend project built for learning full-stack backend development using Node.js, Express, and Sequelize.
Decode-Lab Internship week 3 
