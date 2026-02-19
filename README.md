
```markdown
<h1 align="center">🅿️ ParkEasy Backend API</h1>
<p align="center">
  RESTful API for Smart Parking Management System
</p>

---

## 📌 Overview

ParkEasy Backend is a REST API built with **Node.js, Express, and MongoDB**.

It powers the ParkEasy platform by handling:

- 🔐 User authentication
- 🏢 Parking management
- 📍 Space management
- 📅 Booking system
- ⭐ Reviews & Ratings
- 💳 Payment methods
- 🏙 City & Address management

The backend follows a structured Controller–Model architecture.

---

## 🛠 Tech Stack

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT Authentication
- Render (Deployment)

---

## 📂 Project Structure
├── controllers/
│ ├── address.js
│ ├── booking.js
│ ├── city.js
│ ├── parking.js
│ ├── paymentMethod.js
│ ├── review.js
│ ├── user.js
│ └── spaceRouter.js
│
├── models/
│ ├── bookingSchema.js
│ ├── citySchema.js
│ ├── parkingSchema.js
│ ├── paymentMethodSchema.js
│ ├── reviewSchema.js
│ ├── spaceSchema.js
│ └── userSchema.js
│
├── utils/
│ └── errorHandler.js
│
├── app.js
├── package.json
└── README.md

---

## 🏗 Architecture Pattern

The backend follows a structured MVC-style design:

Route → Controller → Mongoose Model → MongoDB


- Controllers handle request & response logic
- Models define database schemas
- Utilities handle centralized error management

---

## 🔐 Authentication

- JWT-based authentication
- Protected routes for bookings and profile operations
- Token validation middleware

---

## 📡 Core Functional Modules

### 👤 Users
- Register
- Login
- Profile management

### 🏢 Parking
- Create parking
- Retrieve parking listings

### 📍 Spaces
- Add parking spaces
- Retrieve available spaces

### 📅 Bookings
- Create booking
- View booking history
- Cancel booking

### ⭐ Reviews
- Add reviews
- Retrieve ratings

### 💳 Payment Methods
- Add payment options
- Manage user payment methods

---

## ⚙️ Installation & Setup

Clone the repository:

```bash
git clone https://github.com/Kaushik515/park-easy-server
cd park-easy-server
Install dependencies:

npm install


Run server:

npm start
🔑 Environment Variables

Create a .env file:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

🚀 Deployment

The backend is deployed on Render.

Ensure environment variables are configured in deployment settings.

🧪 Future Improvements

Structured service layer

API validation (Joi / Zod)

Rate limiting

Logging (Winston)

Unit testing (Jest)

API documentation (Swagger)

👨‍💻 Author

Kaushik Kotha

📜 License

MIT License
