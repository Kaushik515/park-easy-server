<p align="center">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Mongoose-880000?style=for-the-badge&logo=mongoose&logoColor=white" />
</p>

<p align="center">
  <h1 align="center">🅿️ ParkEasy Backend API</h1>
  <p align="center">
    <strong>Robust RESTful API for Smart Parking Management</strong>
    <br />
    A scalable backend powering real-time parking discovery and booking.
  </p>
</p>

---

## 📋 Table of Contents
- [📌 Overview](#-overview)
- [🛠 Tech Stack](#-tech-stack)
- [📂 Project Structure](#-project-structure)
- [🏗 Architecture](#-architecture)
- [🔐 Security & Privacy Hardening](#-security--privacy-hardening)
- [⚙️ Setup Instructions](#-setup-instructions)
- [🚀 Deployment](#-deployment)
- [👨‍💻 Author](#-author)
- [📜 License](#-license)

---

## 📌 Overview

The **ParkEasy Backend** is a high-performance REST API designed to manage complex parking logistics. It provides a secure and efficient infrastructure for user authentication, property listings, and real-time availability tracking.

### Core Capabilities:
- 🔐 **Identity Management**: Secure sign-up/login with JWT.
- 🏢 **Asset Management**: Full CRUD for parking locations and spaces.
- 📅 **Transaction Logic**: Approval-based booking workflow.
- ⭐ **Feedback Loop**: Integrated review and rating system.

---

## 🛠 Tech Stack

- **Runtime**: ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
- **Framework**: ![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white)
- **Database**: ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
- **ORM**: ![Mongoose](https://img.shields.io/badge/Mongoose-880000?style=flat&logo=mongoose&logoColor=white)
- **Security**: JWT + Bcrypt
- **Validation**: Joi
- **Deployment**: Render

---

## 📂 Project Structure

```bash
.
├── controllers/
│   ├── address.js
│   ├── booking.js
│   ├── city.js
│   ├── parking.js
│   ├── paymentMethod.js
│   ├── review.js
│   ├── user.js
│   └── spaceRouter.js
│
├── models/
│   ├── bookingSchema.js
│   ├── citySchema.js
│   ├── parkingSchema.js
│   ├── paymentMethodSchema.js
│   ├── reviewSchema.js
│   ├── spaceSchema.js
│   └── userSchema.js
│
├── utils/
│   └── errorHandler.js
│
├── app.js
├── package.json
└── README.md
```

## 🏗 Architecture Pattern

The API follows a structured **Controller-Model** design pattern to ensure clean separation of concerns:

`Request → Middleware (Auth) → Controller → Model (MongoDB) → Response`

---

## 🔐 Authentication

ParkEasy utilizes standard **JWT-based authentication**:
1. Users receive a signed token upon successful login.
2. The `isLoggedIn` middleware validates the `Authorization: Bearer <token>` header.
3. Protected routes (Bookings, Profile) require a valid token to proceed.

---

## 📡 API Modules

| Module | Responsibility |
| :--- | :--- | :--- |
| **👤 Users** | Sign-up, login, and profile updates. |
| **🏢 Parking** | Management and **Search** of physical parking locations. |
| **📍 Spaces** | Control and **Filtering** of individual parking slots. |
| **📅 Bookings** | The core workflow: Search → Request → Approve. |
| **⭐ Reviews** | Community-driven ratings for owners and spots. |

---

## 🔐 Security & Privacy Hardening

The API is built with a "Security-First" approach to protect both infrastructure and user data:

- **🔐 Consolidated Secret Management**: Uses a unified `JWT_SECRET` environment variable for both token issuance and verification, eliminating inconsistent fallback logic.
- **🛡️ Administrative Route Protection**: Sensitive management endpoints (like `GET /user` and `GET /booking`) are protected by the `isLoggedIn` middleware.
- **✨ Automatic Data Sanitization**: Sensitive fields such as `password` hashes are explicitly stripped from JSON responses before reaching the network.
- **🔑 Secure Password Hashing**: Utilizes `bcryptjs` with a cost factor of 10 for industry-standard credential storage.

---

## ⚙️ Setup Instructions

### Prerequisites
- **Node.js**: v18+ (verified compatible)
- **MongoDB**: Atlas account or local installation
- **npm**: v9+

### Installation
1. Navigate to the server directory:
   ```bash
   cd park-easy-server
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Configure Environment Variables:
   Create a `.env` file in the root with the following keys:
   ```text
   url=YOUR_MONGODB_CONNECTION_STRING
   JWT_SECRET=YOUR_SECURE_JWT_SECRET
   PORT=5000
   ```
4. Start the Application:
   ```bash
   # Development mode with nodemon
   npm run dev

   # Production mode
   npm start
   ```

---

## 🚀 Deployment

Currently deployed on **Render**. Automatic deployments are triggered via GitHub hooks. ensure all environment variables are correctly mapped in the Render dashboard.

---

## 👨‍💻 Author

**Kaushik Kotha**

---

## 📜 License

Distributed under the MIT License.
