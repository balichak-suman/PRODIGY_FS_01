# PRODIGY_FS_01


# User Authentication System

This is a simple Node.js authentication system using JWT (JSON Web Token) for secure login and registration.

## Features
- User registration with hashed passwords
- Secure login with JWT authentication
- Protected routes access
- Logout functionality
- Uses **MongoDB**, **Express.js**, and **Node.js**

## Installation

### 1. Clone the Repository
```sh
git clone https://github.com/balichak-suman/PRODIGY_FS_01
cd user-authentication
2. Install Dependencies
npm install
3. Create a .env File
Create a .env file in the root directory and add the following environment variables:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
4. Run the Server
For normal start:

npm start
For development mode (auto-restarts on changes):

npm run dev
API Endpoints

1. Register a User
Endpoint: POST /auth/register
Request Body:

{
  "username": "exampleUser",
  "email": "user@example.com",
  "password": "securepassword"
}
2. Login a User
Endpoint: POST /auth/login
Request Body:

{
  "email": "user@example.com",
  "password": "securepassword"
}
3. Access Protected Route
Endpoint: GET /auth/protected

Requires a valid authentication token (sent via cookies).
4. Logout
Endpoint: POST /auth/logout

Clears authentication token.
Project Structure

user-authentication/
│── models/
│   └── User.js
│── routes/
│   └── authRoutes.js
│── .env
│── server.js
│── package.json
│── README.md
Technologies Used

Node.js
Express.js
MongoDB
JWT (JSON Web Token)
Bcrypt.js for password hashing
dotenv for environment variables
cors and cookie-parser for security