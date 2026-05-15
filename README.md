# ShopX E-Commerce Project Documentation

# Project Overview

ShopX is a full-stack E-Commerce web application developed using React.js, Node.js, Express.js, and MongoDB.

The application allows users to:

* Register and Login
* View Products
* Add Products to Cart
* Remove Products from Cart
* View Cart Total
* Logout Securely

The project follows a modern full-stack architecture with frontend and backend separated.

---

# Technologies Used

## Frontend

* React.js
* React Router DOM
* Axios
* CSS3
* Context API
* Vite

## Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JWT Authentication
* bcryptjs
* dotenv
* cors

---

# Project Structure

```bash
ecommerce/
│
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── styles/
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   ├── CartContext.jsx
│   │   └── AuthContext.jsx
│   │
│   └── package.json
│
├── server/
│   ├── models/
│   ├── routes/
│   ├── server.js
│   ├── .env
│   └── package.json
│
└── README.md
```

---

# Frontend Features

## Home Page

* Hero section
* Product cards
* Responsive layout
* Add to cart functionality

## Authentication

### Register

Users can create an account using:

* Username
* Email
* Password

### Login

Users can login securely.

JWT token is stored in localStorage.

### Logout

Logout removes the token and redirects the user.

## Cart System

* Add items to cart
* Remove items from cart
* Cart count updates dynamically
* Total amount calculation

---

# Backend Features

## User Authentication API

### Register Route

```bash
POST /api/auth/register
```

Stores user data securely after hashing password using bcrypt.

### Login Route

```bash
POST /api/auth/login
```

Authenticates user and returns JWT token.

---

## Product APIs

### Add Product

```bash
POST /api/products/create
```

Adds new products to MongoDB.

### Get Products

```bash
GET /api/products
```

Fetches all products from database.

---

# Database

MongoDB is used as the database.

Database collections:

* users
* products

## MongoDB Connection

```env
MONGO_URL=mongodb://127.0.0.1:27017/ecommerce
```

---

# Authentication Flow

1. User registers
2. Password gets encrypted using bcrypt
3. User logs in
4. JWT token generated
5. Token stored in localStorage
6. Navbar changes dynamically

---

# Cart Functionality

Cart state is managed using React Context API.

## Features

* Add product
* Remove product
* View total
* Dynamic cart count

---

# UI Design

The UI uses:

* Dark premium theme
* Purple accent colors
* Responsive product cards
* Hover animations
* Mobile responsiveness

---

# Installation Steps

# Backend Setup

## Step 1

Open terminal:

```bash
cd server
```

## Step 2

Install dependencies:

```bash
npm install
```

## Step 3

Create .env file:

```env
MONGO_URL=mongodb://127.0.0.1:27017/ecommerce
```

## Step 4

Run backend:

```bash
node server.js
```

Expected output:

```bash
MongoDB Connected
Server Running On Port 5000
```

---

# Frontend Setup

## Step 1

Open second terminal:

```bash
cd client
```

## Step 2

Install dependencies:

```bash
npm install
```

## Step 3

Run frontend:

```bash
npm run dev
```

Frontend runs on:

```bash
http://localhost:5173
```

---

# API Testing

## Register User

```bash
POST http://localhost:5000/api/auth/register
```

Request Body:

```json
{
  "username":"Sai",
  "email":"sai@gmail.com",
  "password":"123456"
}
```

---

## Login User

```bash
POST http://localhost:5000/api/auth/login
```

Request Body:

```json
{
  "email":"sai@gmail.com",
  "password":"123456"
}
```

---

## Add Product

```bash
POST http://localhost:5000/api/products/create
```

Request Body:

```json
{
  "name":"Headphone",
  "price":1999,
  "image":"https://images.unsplash.com/photo-1505740420928-5e560c06d30e"
}
```

---

## Get Products

```bash
GET http://localhost:5000/api/products
```

---

# Security Features

* Password hashing using bcrypt
* JWT authentication
* Protected authentication flow

---

# Future Improvements

* Payment gateway integration
* Product search
* Product categories
* Wishlist
* Quantity selector
* Order history
* Admin dashboard
* Checkout system

---

# Conclusion

ShopX is a modern full-stack E-Commerce platform built using MERN stack technologies.

The project demonstrates:

* Frontend development
* Backend API development
* Database integration
* Authentication system
* State management
* Full-stack architecture

This project is suitable for:

* Internship submissions
* Portfolio projects
* Full-stack learning
* Resume showcase
