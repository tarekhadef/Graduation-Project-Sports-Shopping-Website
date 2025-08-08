# Graduation-Project-Sports-Shopping-Website
# 🛍️ Sports Shop Backend – Task Submission

## 1. Entity Chosen & Why

I chose the **Coupon** entity for this task.

### Why?

- **Relevance**: Coupons are essential in e-commerce for promotions, loyalty, and marketing.
- **Challenge**: It required implementing full CRUD with secure access, validation, and database integration.
- **Learning Opportunity**: It allowed me to practice route protection, role-based access, and data modeling with Mongoose.

---

## 2. Routes Summary

### 🔐 Authentication Routes

| Method | Endpoint         | Description        | Access     |
|--------|------------------|--------------------|------------|
| POST   | `/api/auth/signup` | Register a new user | Public     |
| POST   | `/api/auth/login`  | Login and get token | Public     |

---

### 🎟️ Coupon Routes

| Method | Endpoint                     | Description               | Access     |
|--------|------------------------------|---------------------------|------------|
| GET    | `/api/coupons`               | List all coupons          | Admin only |
| POST   | `/api/coupons`               | Create a new coupon       | Admin only |
| PATCH  | `/api/coupons/:id`           | Update a coupon           | Admin only |
| DELETE | `/api/coupons/:id`           | Delete a coupon           | Admin only |

---

## 3. How to Run the Code Locally

### 🔧 Prerequisites

- Node.js & npm
- MongoDB (local or MongoDB Atlas)
- Postman (for testing)

### 📦 Installation Steps

1. **Clone the repository**
bash
git clone https://github.com/your-username/sports-shop-backend.git
cd sports-shop-backend

Install dependencies

bash
npm install
Configure environment variables

Create a .env file:
env
PORT=5000
MONGO_URI=mongodb://localhost:27017/sports-shop
JWT_SECRET=your_jwt_secret
Start the server

npm start
You should see:

Server running on port 5000
MongoDB connected
4. What the Module Does
This backend module provides:

User registration and login with hashed passwords and JWTs.

Coupon management:

Admins can create, update, delete, and list coupons.

Each coupon has a code and discountPercent.

Route protection using middleware to ensure only authorized users access sensitive routes.

MongoDB integration for data persistence.

Clean code structure with separate controllers, routes, and models.

5. Chosen User Roles
Role	Permissions
User	Can register, login, and shop (not coupons)
Admin	Full access including coupon management

✅ Notes
All secure routes require a JWT token in the Authorization header:
Authorization: Bearer <your_token>

Coupon endpoints are admin-only and respond with a 401 Unauthorized if accessed by a regular user.

📌 Example Coupon
json
Copy
Edit
{
  "code": "SUMMER25",
  "discountPercent": 25
}
👤 Author
Tarek Hadef – August 2025 Submission

