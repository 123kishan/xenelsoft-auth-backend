# Xenelsoft Auth Backend Task

This is a backend project built using Node.js, Express.js, MongoDB, JWT Authentication.

## Features
- Signup API with validation
- Password hashing using bcrypt
- Duplicate user prevention
- Login API with JWT token generation
- JWT Middleware Authentication
- Protected API to fetch user profile
- Secure response (password not returned)
- Proper error handling

---

## Tech Stack
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT (jsonwebtoken)
- bcryptjs
- dotenv

---

## Setup Instructions

### 1. Clone Repo
```bash
git clone <your_repo_url>
cd xenelsoft-auth-backend
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Setup Environment Variables
Create a `.env` file in root folder:

```env
PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/xenelsoftDB
JWT_SECRET=THIS_IS_MY_SUPER_SECRET_KEY
JWT_EXPIRE=1h
```

You can also copy `.env.example` and rename it to `.env`.

### 4. Run Project
```bash
npm run dev
```

Server will start at:
```
http://localhost:5000
```

---

## API Endpoints

### 1. Signup API
**POST**
```
/api/auth/signup
```

Body (JSON):
```json
{
  "name": "Kishan",
  "email": "kishan@gmail.com",
  "password": "123456"
}
```

---

### 2. Login API
**POST**
```
/api/auth/login
```

Body:
```json
{
  "email": "kishan@gmail.com",
  "password": "123456"
}
```

---

### 3. Protected Profile API
**GET**
```
/api/auth/profile
```

Headers:
```
Authorization: Bearer <JWT_TOKEN>
```

---

## Notes
- Password is hashed using bcrypt.
- JWT token is required for protected routes.
- Token expiration handled properly.
- Password is never returned in profile response.

---

## Author
Backend Task Submission for Xenelsoft Technologies.
