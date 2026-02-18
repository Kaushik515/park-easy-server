# 🚗 ParkEasy – Backend Service

Backend service for the ParkEasy parking management system.  
This service handles user authentication, parking space management, and booking operations using RESTful APIs.

Built with Node.js, Express.js, and MongoDB.

---

## 📌 Overview

ParkEasy backend is responsible for:

- User registration and authentication (JWT-based)
- Managing parking spaces
- Handling booking operations
- Secure API access with middleware protection
- Database integration with MongoDB

The system is designed with modular architecture and separation of concerns to ensure scalability and maintainability.

---

## 🏗 Architecture Overview

The application follows a layered architecture pattern:

- **Routes Layer** → Defines API endpoints
- **Controller Layer** → Contains business logic
- **Model Layer** → MongoDB schemas & data structure
- **Middleware Layer** → Authentication & request validation
- **Config Layer** → Database connection & environment setup

Each component is isolated to improve readability, maintainability, and scalability.

---

## 📂 Folder Structure

park-easy-server/
│── config/
│ └── db.js
│
│── controllers/
│ └── (business logic files)
│
│── middleware/
│ └── authMiddleware.js
│
│── models/
│ └── (MongoDB schemas)
│
│── routes/
│ └── (API route definitions)
│
│── server.js
│── package.json


---

## 🔐 Authentication

- JWT-based authentication
- Secure login & registration
- Protected routes using middleware
- Token validation on sensitive operations

---

## 📡 API Endpoints

### Authentication Routes
- `POST /api/auth/register`
- `POST /api/auth/login`

### Booking Routes
- `GET /api/bookings`
- `POST /api/bookings`
- `PUT /api/bookings/:id`
- `DELETE /api/bookings/:id`

### Parking Routes
- `GET /api/parking`
- `POST /api/parking`
- `PUT /api/parking/:id`
- `DELETE /api/parking/:id`

---

## ⚙️ Environment Variables

Create a `.env` file in the root directory and add:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

---

## 🚀 Installation & Running Locally

1. Clone the repository

git clone https://github.com/Kaushik515/park-easy-server.git

2. Install dependencies

npm install

3. Add environment variables in `.env`

4. Start the server

npm start

---

## 🛠 Tech Stack

- Node.js
- Express.js
- MongoDB
- JWT Authentication
- REST API Architecture

---

## 🎯 Key Engineering Practices

- Modular folder structure
- Separation of concerns
- Environment-based configuration
- Secure authentication middleware
- RESTful API design principles
