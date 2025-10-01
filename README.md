# 🛒 PrimeMart

PrimeMart is a **full-stack e-commerce web application** built with **React, Node.js, Express, and MongoDB**.  
It allows users to browse products, add them to a cart, place orders, and manage their profiles.  
Admins can manage products, view orders, and control the store through a dashboard.  

---

## 📌 Architecture

[ User / Browser ]
↓
[ Frontend (React) ]
↓ REST API (JSON)
[ Backend (Node.js + Express) ]
↓
[ Database (MongoDB) ]


- **Frontend (React)** – UI for browsing products, cart, checkout, login/register  
- **Backend (Express)** – API server for authentication, products, orders, and admin features  
- **Database (MongoDB)** – Stores users, products, orders, and cart data  

---

## ✨ Features

- ✅ User authentication (**JWT login/register**)  
- ✅ Product listing, search, and details  
- ✅ Cart management & checkout flow  
- ✅ Order history and tracking  
- ✅ Admin dashboard for products & orders  

---

## 📂 Folder Structure

PrimeMart/
├── backend/
│   ├── controllers/        # Business logic (auth, products, orders, etc.)
│   ├── models/             # Mongoose/DB models
│   ├── routes/             # API routes
│   ├── middlewares/        # Auth, validation, error handling
│   ├── utils/              # Helper functions (e.g., token generation, logger)
│   ├── config/             # DB connection, environment configs
│   ├── tests/              # Backend unit/integration tests
│   ├── server.js           # Entry point
│   └── package.json        # Backend dependencies
│
├── frontend/
│   ├── public/             # Static files (index.html, favicon, etc.)
│   ├── src/
│   │   ├── assets/         # Images, icons, styles
│   │   ├── components/     # Reusable UI parts (buttons, navbar, cards)
│   │   ├── pages/          # Page-level components (Home, Login, Cart)
│   │   ├── services/       # API calls (Axios/fetch wrappers)
│   │   ├── context/        # React context providers (auth, cart, theme)
│   │   ├── hooks/          # Custom hooks (useAuth, useFetch)
│   │   ├── utils/          # Helper functions for frontend
│   │   ├── App.js          # Main app component
│   │   └── index.js        # Entry point (ReactDOM render)
│   └── package.json        # Frontend dependencies
│
├── .gitignore              # Ignore node_modules, build files, env
├── README.md               # Project documentation
└── package.json            # Root (optional if using monorepo tools like npm workspaces)

---

## ⚙️ Setup & Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/abanoub-aboelsaad/PrimeMart.git
   cd PrimeMart
Install dependencies

bash
Copy code
cd backend && npm install
cd ../frontend && npm install
Create .env files

Backend .env:
env
PORT=5000
DB_URI=mongodb://yours
JWT_SECRET=your_secret_key
Frontend .env:

env
Copy code
REACT_APP_API_URL=http://localhost:5000/api
Run servers

In backend/:

bash

npm run dev
In frontend/:

bash

npm start
🚀 Example API Routes
Method	Route	Description
POST	/api/auth/register	Register user
POST	/api/auth/login	Login user (JWT)
GET	/api/products	Get all products
GET	/api/products/:id	Get product details
POST	/api/cart	Add item to cart
POST	/api/orders	Place an order
GET	/api/orders/user	Get logged-in user orders
GET	/api/orders	(Admin) get all orders

📜 License
Open-source – free to use and modify.
Developed with ❤️ by abanoub-aboelsaad
