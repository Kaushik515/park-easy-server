<h1 align="center">🅿️ ParkEasy - Backend API</h1>
<p align="center">
  Scalable REST API for Smart Parking Management System
</p>

<p align="center">
  Built with Node.js, Express, MongoDB & JWT Authentication
</p>

---

## 📌 Overview

ParkEasy Server is the backend service powering the ParkEasy smart parking platform.

It provides secure and scalable REST APIs for:

- 🔐 User Authentication & Authorization
- 🏢 Parking Management
- 📍 Space Allocation
- 📅 Booking System
- 👤 Profile Management

The system follows a modular architecture to ensure maintainability and scalability.

---

## 🛠 Tech Stack

- 🟢 Node.js
- 🚀 Express.js
- 🍃 MongoDB
- 📦 Mongoose
- 🔐 JWT Authentication
- 🌍 Deployed on Render

---
Client (React)
↓
REST API (Express Server)
↓
MongoDB Database

The backend follows a layered structure:

- Routes → Controllers → Services → Database (Mongoose Models)

---

## 📂 Project Structure

src/
│
├── config/
│   └── db.js
│
├── modules/
│   ├── auth/
│   │   ├── auth.controller.js
│   │   ├── auth.service.js
│   │   ├── auth.routes.js
│   │   └── auth.model.js
│   │
│   ├── parking/
│   │   ├── parking.controller.js
│   │   ├── parking.service.js
│   │   ├── parking.routes.js
│   │   └── parking.model.js
│   │
│   ├── space/
│   │   ├── space.controller.js
│   │   ├── space.service.js
│   │   ├── space.routes.js
│   │   └── space.model.js
│   │
│   ├── booking/
│   │   ├── booking.controller.js
│   │   ├── booking.service.js
│   │   ├── booking.routes.js
│   │   └── booking.model.js
│
├── middleware/
│   ├── auth.middleware.js
│   └── error.middleware.js
│
├── utils/
│   └── generateToken.js
│
├── app.js
└── server.js


## 🔐 Authentication

The API uses **JWT-based authentication**.

- Users receive a token upon login.
- Protected routes require token validation middleware.
- Role-based access supported (User / Owner).

---

## 📡 API Endpoints

### 🔐 Auth Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /auth/register | Register new user |
| POST | /auth/login | Authenticate user |

---

### 🏢 Parking Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /parkings | Get all parkings |
| POST | /parkings | Create new parking (Owner) |
| GET | /parkings/:id | Get parking details |

---

### 📍 Space Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /spaces | Get available spaces |
| POST | /spaces | Create parking space |

---

### 📖 Booking Routes

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /bookings | Get user bookings |
| POST | /bookings | Create booking |
| DELETE | /bookings/:id | Cancel booking |

---

## ⚙️ Installation & Setup

Clone the repository:

```bash
git clone https://github.com/Kaushik515/park-easy-server
cd park-easy-server
Install dependencies : npm install
Run development server : npm run dev

🔑 Environment Variables

Create a .env file in the root directory:
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

🚀 Deployment

The backend is deployed on Render.

Make sure environment variables are configured in the deployment platform.

🧪 Future Improvements

Payment Gateway Integration

Rate Limiting & API Security Enhancements

Unit & Integration Testing

Dockerization

CI/CD Pipeline

👨‍💻 Author

Kaushik Kotha

📜 License

This project is licensed under the MIT License.
## 🏗 System Architecture

