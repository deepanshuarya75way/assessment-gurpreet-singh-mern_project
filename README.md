# MERN E-Commerce Platform

A full-stack e-commerce application built with the MERN stack, designed for modern online shopping with a customer storefront and an admin management dashboard.

## Overview

This project combines a React + Vite frontend with an Express + MongoDB backend to deliver a complete shopping experience, including:

- Customer authentication and role-based access
- Product browsing, filtering, and search
- Cart management and checkout flow
- Address management
- Order creation and status tracking
- PayPal payment integration
- Admin dashboard for product and order management
- Product image uploads through Cloudinary

## Tech Stack

### Frontend
- React
- Vite
- Redux Toolkit
- React Router
- Tailwind CSS
- Radix UI components
- Axios

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Cloudinary
- PayPal REST SDK
- Cookie-based session handling

## Features

### Customer Experience
- User registration and login
- Product listing and filtering by category, brand, and price
- Search functionality for products
- Add to cart and manage cart items
- Save and manage delivery addresses
- Checkout flow with PayPal payment return/cancel handling
- View order history and purchase details

### Admin Experience
- Secure admin dashboard
- Product CRUD operations
- Product image upload support
- Order monitoring and status updates
- Role-based authorization for protected routes

## Project Structure

```bash
MERN-PROJECT/
├── client/                  # React frontend
│   ├── src/                 # Application source code
│   ├── public/              # Static assets
│   ├── package.json
│   ├── vite.config.js
│   └── .env
├── server/                  # Express backend
│   ├── controllers/         # Route logic
│   ├── database/            # MongoDB connection setup
│   ├── helpers/             # Cloudinary and PayPal helpers
│   ├── middleware/          # Auth middleware
│   ├── models/              # MongoDB schemas
│   ├── routes/              # API routes
│   ├── server.js            # Application entry point
│   ├── package.json
│   └── .env
├── README.md
└── package.json            # Optional root config if added later
```

## Prerequisites

Before running the project locally, make sure you have:

- Node.js 18+
- npm or yarn
- MongoDB Atlas or a local MongoDB instance
- Cloudinary account
- PayPal Developer account

## Environment Variables

Create a `.env` file in both the `server` and `client` folders.

### Server `.env`

```env
PORT=5000
CLIENT_URL=http://localhost:5173
MONGO_URI=your_mongodb_connection_string
JWT_SECRET_KEY=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

PAYPAL_CLIENT_ID=your_paypal_client_id
PAYPAL_CLIENT_SECRET=your_paypal_client_secret
```

### Client `.env`

```env
VITE_API_URL=http://localhost:5000
```

## Installation

1. Clone the repository

```bash
git clone https://github.com/your-username/mern-project.git
cd mern-project
```

2. Install frontend dependencies

```bash
cd client
npm install
```

3. Install backend dependencies

```bash
cd ../server
npm install
```

## Running the Application

### Start the backend

```bash
cd server
npm run dev
```

The backend runs on the port defined in `PORT` (default: `5000`).

### Start the frontend

```bash
cd client
npm run dev
```

The frontend typically runs on:

```bash
http://localhost:5173
```

## Available Scripts

### Client

```bash
npm run dev
npm run build
npm run preview
npm run lint
```

### Server

```bash
npm run dev
npm run start
```

## Default User Roles

- `user`: regular customer account
- `admin`: administrator access for managing products and orders

## API Overview

The backend exposes APIs under the following route groups:

- `/api/auth` — registration, login, logout
- `/api/admin/products` — admin product management
- `/api/admin/orders` — admin order management
- `/api/shop/products` — products for storefront
- `/api/shop/cart` — cart operations
- `/api/shop/address` — address management
- `/api/shop/order` — checkout and order creation
- `/api/shop/search` — product search
- `/api/shop/review` — product reviews
- `/api/common/feature` — featured content

## Screenshots

Add your application screenshots here for better presentation on GitHub:

```md
![Home Page](./assets/home-page.png)
![Admin Dashboard](./assets/admin-dashboard.png)
```

## Roadmap

Planned improvements include:

- Enhanced product filters and sorting
- Wishlist functionality
- Order status dashboards with analytics
- Better admin reporting
- Product reviews and rating improvements
- Improved mobile responsiveness and accessibility

## License

This project is licensed under the MIT License.

## Author

Built as a full-stack MERN e-commerce project for learning and portfolio use.

If you want, you can also add:
- your GitHub username
- your portfolio website
- project demo URL
- contributor credits
