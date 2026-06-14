# ⚙️ E-Commerce Backend (Server)

The REST API backend for a full-stack e-commerce platform. Built with Node.js and Express, using PostgreSQL as the database. Handles authentication, product management, orders, payments, and file uploads.

---

## ✨ Features

- 🔐 JWT-based authentication & authorization
- 🔒 Password hashing with Bcrypt
- 🛍️ Product CRUD with image upload (Cloudinary)
- 📦 Order management
- 👤 User management
- 💳 Payment integration — **Stripe** & **SSLCommerz**
- 📧 Email notifications via Nodemailer
- 🗄️ PostgreSQL database
- 🍪 Cookie-based session handling

---

## 🧱 Tech Stack

| Technology | Purpose |
|---|---|
| Node.js + Express.js | Server framework |
| PostgreSQL + `pg` | Database |
| JWT | Authentication tokens |
| Bcrypt | Password encryption |
| Cloudinary | Image storage |
| Nodemailer | Email service |
| Stripe | Payment gateway |
| SSLCommerz | Local payment gateway |
| Express FileUpload | File handling |
| Dotenv | Environment config |

---

## 📁 Project Structure

```
Server/
├── config/         # Database & environment config
├── controllers/    # Route handler logic
├── database/       # DB connection setup
├── middlewares/    # Auth, error handling middleware
├── models/         # Database models/queries
├── router/         # API route definitions
├── utils/          # Helper functions
├── uploads/        # Temporary file uploads
├── app.js          # Express app setup
└── server.js       # Entry point
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- PostgreSQL database

### Installation

```bash
# Clone the repository
git clone https://github.com/TanvirHassan369/ecommerce-fullstack.git

# Navigate to server
cd "ECommerce(SERVER)/Server"

# Install dependencies
npm install

# Start development server
npm run dev
```

Server runs at `http://localhost:5000`

### Environment Variables
Create `config/config.env`:
```
PORT=5000

# Database
DATABASE_URL=your_postgresql_connection_string

# JWT
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d

# Cloudinary
CLOUDINARY_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Email
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_EMAIL=your_email@gmail.com
SMTP_PASSWORD=your_app_password

# Stripe
STRIPE_SECRET_KEY=your_stripe_secret_key

# SSLCommerz
SSLCOMMERZ_STORE_ID=your_store_id
SSLCOMMERZ_STORE_PASSWORD=your_store_password
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | User login |
| GET | `/api/products` | Get all products |
| GET | `/api/products/:id` | Get single product |
| POST | `/api/orders` | Create new order |
| GET | `/api/orders/:id` | Get order details |
| POST | `/api/payment/stripe` | Process Stripe payment |
| POST | `/api/payment/sslcommerz` | Process SSLCommerz payment |

---

## 🔗 Related

- 🌐 [Client (Frontend)](../../E-Commerce(CLIENT)/Client/README.md)
- 📊 [Admin Dashboard](../../ECommerce(Dashboard)/ecommerce-dashboard-template/README.md)
