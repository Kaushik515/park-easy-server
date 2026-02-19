# 🟩 2️⃣ park-easy-server README.md

```markdown
<h1 align="center">🅿️ ParkEasy Server</h1>
<p align="center">
  Smart Parking Management System – Backend API
</p>

---

## 🚀 Overview

This repository contains the backend API for ParkEasy.

The server handles:

- 🔐 Authentication (JWT)
- 🏢 Parking management
- 📅 Space management
- 📖 Booking system
- 👤 Profile management

---

## 🛠 Tech Stack

- 🟢 Node.js
- 🚀 Express.js
- 🍃 MongoDB
- 🔐 JWT Authentication
- 📦 Mongoose ODM
- 🌍 Deployed on Render

---

## 🏗 Architecture

Client (React)  
⬇  
REST API (Express)  
⬇  
MongoDB Database  

---

## 📡 API Endpoints

### 🔐 Authentication
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /auth/register | Register user |
| POST | /auth/login | Login user |

---

### 🏢 Parking
| Method | Endpoint |
|--------|----------|
| GET | /parkings |
| POST | /parkings |

---

### 📍 Spaces
| Method | Endpoint |
|--------|----------|
| GET | /spaces |
| POST | /spaces |

---

### 📖 Bookings
| Method | Endpoint |
|--------|----------|
| GET | /bookings |
| POST | /bookings |
| DELETE | /bookings/:id |

---

## ⚙️ Setup Instructions

```bash
git clone https://github.com/Kaushik515/park-easy-server
cd park-easy-server
npm install
npm run dev
🔐 Environment Variables
Create a .env file:

PORT=5000
MONGO_URI=your_mongodb_connection
JWT_SECRET=your_secret
📂 Project Structure
src/
 ├── controllers/
 ├── routes/
 ├── models/
 ├── middleware/
 ├── config/
 └── server.js
