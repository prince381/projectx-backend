# Project X – Backend Service

A backend API service built with Node.js for user authentication, authorization, and account management.  
The project is structured with production-ready patterns including JWT-based authentication, role-based access control (RBAC), centralized error handling, and database abstraction.

## 🚀 Features

- User authentication using JSON Web Tokens (JWT)
- Role-Based Access Control (RBAC) middleware
- Secure token verification and request authorization
- Modular Express application structure
- Centralized error handling and async error wrappers
- Database connection abstraction
- Email utilities for account-related workflows
- Environment-based configuration support

## 🧱 Project Structure

src/
├── server.js # Application entry point
├── app.js # Express app configuration
├── config/
│ └── database.js # Database connection setup
├── auth/
│ └── auth.js # Authentication logic
├── middlewares/
│ └── rbacMiddleware.js # Role-based access control
├── models/
│ ├── User.js # User model
│ ├── EmailCode.js # Email verification / code model
│ └── index.js # Model exports
├── utils/
│ ├── verifyJWT.js # JWT verification utility
│ ├── sendEmail.js # Email sending utility
│ ├── errorHandler.js # Centralized error handling
│ ├── catchError.js # Async error wrapper
│ └── connection.js # Database connection helper


## 🧠 Architecture Overview

- **Express-based API** with a clear separation of concerns
- **JWT authentication** for stateless request validation
- **RBAC middleware** to restrict access based on user roles
- **Centralized error handling** to ensure consistent API responses
- **Utility-driven design** to keep controllers and middleware clean
- **Database abstraction layer** for easier maintenance and scaling

## 📦 Installation

### Clone the repository
```bash
git clone <repository-url>
cd project_x-main
```

### Install dependencies
```bash
npm install
```

or

```bash
yarn install
```

### ▶️ Running the Server
```bash
npm run start
```

or

```bash
yarn start
```

The server initializes via server.js, configures the Express app, establishes the database connection, and starts listening for incoming requests.

### 🔐 Authentication & Authorization
* JWTs are issued during authentication and verified on protected routes
* Role-based middleware enforces access rules per endpoint
* Token verification logic is isolated for reuse and testability

### ⚠️ Error Handling
* Async routes are wrapped using a centralized error-catching utility
* Errors are formatted consistently via a global error handler
* Prevents unhandled promise rejections and improves API reliability

### 🛠️ Tech Stack
* Node.js
* Express
* JWT (JSON Web Tokens)
* MongoDB / Database abstraction layer
* Docker-ready (dependency lock files included)

📄 License

MIT License
