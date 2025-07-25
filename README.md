# Food Delivery Full Stack Application

A complete food delivery platform with a customer-facing web app, an admin dashboard, and a Node.js/Express backend with MongoDB.

## Live Demo

[View the deployed application here](https://tomato-1-n7x1.onrender.com/)

## Table of Contents

- Features
- Project Structure
- Tech Stack
- Setup & Installation
  - Backend
  - Frontend (User)
  - Admin Dashboard
- API Overview
- Usage
- Folder Structure
- License

---

## Features

- User registration, login, and authentication
- Browse food menu, add to cart, and place orders
- Order history and order tracking
- Admin dashboard for managing food items and orders
- Image upload for food items
- Secure payment integration (Stripe)
- Responsive UI for both user and admin

---

## Project Structure

```
food-del-final/
  backend/    # Node.js/Express API server, MongoDB models, business logic
  frontend/   # React app for customers
  admin/      # React app for admins
```

---

## Tech Stack

- **Backend:** Node.js, Express, MongoDB, Mongoose, JWT, Multer, Stripe
- **Frontend:** React, Vite, Axios, React Router, React Toastify, Stripe.js
- **Admin:** React, Vite, Axios, React Router, React Toastify

---

## Setup & Installation

### Prerequisites

- Node.js (v16+ recommended)
- npm or yarn
- MongoDB instance (local or cloud)

### 1. Backend

```bash
cd backend
npm install
# Create a .env file with your MongoDB URI, JWT secret, Stripe keys, etc.
npm run server
# Server runs on http://localhost:4000 by default
```

#### Example .env

```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
STRIPE_SECRET_KEY=your_stripe_secret
```

### 2. Frontend (User)

```bash
cd frontend
npm install
npm run dev
# App runs on http://localhost:5173 by default
```

### 3. Admin Dashboard

```bash
cd admin
npm install
npm run dev
# Admin dashboard runs on http://localhost:5173 by default (change port if needed)
```

---

## API Overview

- `POST /api/user/register` — Register a new user
- `POST /api/user/login` — User login
- `GET /api/food` — List all food items
- `POST /api/cart` — Add item to cart
- `GET /api/cart` — Get user cart
- `POST /api/order` — Place an order
- `GET /api/order` — Get user orders
- `POST /api/food` — (Admin) Add new food item
- `PUT /api/food/:id` — (Admin) Update food item
- `DELETE /api/food/:id` — (Admin) Delete food item

> See backend/routes/ for full API details.

---

## Usage

- Users can browse the menu, add items to their cart, and place orders.
- Admins can log in to the admin dashboard to manage food items and view orders.
- All images are uploaded and served from the backend `/images` endpoint.

---

## Folder Structure

### backend/
- `server.js` — Express server entry point
- `config/db.js` — MongoDB connection logic
- `models/` — Mongoose schemas (User, Food, Order)
- `controllers/` — Business logic for each resource
- `routes/` — API endpoints
- `middleware/` — Auth and other middleware
- `uploads/` — Uploaded images

### frontend/
- `src/pages/` — Main app pages (Home, Cart, Orders, etc.)
- `src/components/` — UI components (Navbar, FoodDisplay, etc.)
- `src/Context/StoreContext.jsx` — Global state management
- `src/assets/` — Images and icons

### admin/
- `src/pages/` — Admin pages (Add, List, Orders)
- `src/components/` — Admin UI (Navbar, Sidebar)
- `src/assets/` — Admin images/icons

---

## License

This project is licensed under the MIT License.
