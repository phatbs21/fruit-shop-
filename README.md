# 🍎 Fruit Shop

Fruit Shop is a full-stack web application (focus on backend) designed for an online fruit store. It features a modern UI built with React and a robust backend powered by Node.js and Express. Users can browse products, add them to the cart, place orders, and track their order history seamlessly.

## 📑 Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Seeding the Database](#seeding-the-database)
- [API Endpoints](#api-endpoints)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## 🚀 Features

✅ User authentication (Login, Register)  
✅ Browse available fruits and products  
✅ Add items to the shopping cart  
✅ Secure checkout process  
✅ View order history  
✅ PayPal payment integration  

---

## 🛠️ Technologies Used

### **Frontend:**
- ⚛️ React
- 🎛 Redux
- 🔀 React Router
- 🎨 Tailwind CSS & Flowbite
- 🔗 Axios

### **Backend:**
- 🟢 Node.js & Express
- 🗄️ MongoDB (Mongoose ORM)
- 🔐 JWT Authentication
- 💳 PayPal API for secure payments

---

## 🏗️ Installation

### 📌 Prerequisites
- Install [Node.js](https://nodejs.org/)
- Install [MongoDB](https://www.mongodb.com/)

### 🔧 Setup Instructions

1️⃣ **Clone the repository:**
```sh
git clone https://github.com/yourusername/fruit-shop.git
cd fruit-shop
```

2️⃣ **Install dependencies:**

- **Backend**
```sh
cd api
npm install
```

- **Frontend**
```sh
cd ../client
npm install
```

3️⃣ **Set up environment variables:**
Create a `.env` file in the `api` directory and add the following:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PAYPAL_CLIENT_ID=your_paypal_client_id
```

---

## ▶️ Usage

### Start the Backend Server
```sh
cd api
npm run server
```

### Start the Frontend
```sh
cd client
npm run dev
```

---

## 🌱 Seeding the Database
To seed the database with initial data, you can use the following endpoints:

- **Seed Users:** `POST /api/seed/users`
- **Seed Products:** `GET /api/seed/products`

---

## 🔌 API Endpoints

### **User Routes**
- `POST /api/users/login` - Login user
- `POST /api/users` - Register user
- `GET /api/users/profile` - Get user profile (protected)
- `PUT /api/users/profile` - Update user profile (protected)

### **Product Routes**
- `GET /api/products` - Get all products
- `GET /api/products/:id` - Get product by ID

### **Order Routes**
- `POST /api/orders` - Create new order (protected)
- `GET /api/orders/:id` - Get order by ID (protected)
- `PUT /api/orders/:id/payment` - Update order payment status (protected)
- `GET /api/orders` - Get all orders for logged-in user (protected)

### **PayPal Config**
- `GET /api/config/paypal` - Get PayPal client ID

---

## 📂 Project Structure
```
fruit-shop/
├── api/
│   ├── data/
│   │   ├── Products.js
│   │   └── Users.js
│   ├── middleware/
│   │   └── Auth.js
│   ├── models/
│   │   ├── Order.js
│   │   ├── Product.js
│   │   └── User.js
│   ├── routes/
│   │   ├── Order.js
│   │   ├── Product.js
│   │   └── User.js
│   ├── .env
│   ├── databaseSeeder.js
│   ├── index.js
│   ├── package.json
│   └── tokenGenerate.js
├── client/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── layouts/
│   │   ├── pages/
│   │   ├── Redux/
│   │   │   ├── Actions/
│   │   │   ├── Constants/
│   │   │   ├── Reducers/
│   │   │   └── store.js
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   ├── .babelrc
│   ├── .eslintrc.cjs
│   ├── index.html
│   ├── package.json
│   ├── postcss.config.js
│   ├── tailwind.config.js
│   └── vite.config.js
├── .gitignore
├── package.json
└── README.md
```

---

## 🤝 Contributing
Contributions are welcome! If you'd like to improve this project, feel free to submit an issue or a pull request.

---

## 📜 License
This project is licensed under the **MIT License**.
