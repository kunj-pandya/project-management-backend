<h1 align="center"> Project Management Backend</h1>

<p align="center">
  <strong>A full-featured backend API built with Express, MongoDB, and JWT — complete with authentication, email verification, and password recovery.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18+-green?logo=node.js" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express.js-black?logo=express" alt="Express" />
  <img src="https://img.shields.io/badge/MongoDB-6+-brightgreen?logo=mongodb" alt="MongoDB" />
  <img src="https://img.shields.io/badge/License-MIT-blue" alt="License MIT" />
</p>

---

## Overview

This backend powers a **Project Management System**, designed to explore **authentication workflows**, **token management**, and **secure email verification** — built as part of my backend learning journey.

It includes **JWT-based auth**, **secure cookies**, **email verification**, **password reset**, and **token refresh logic**, following clean architecture principles.

---

## Features

✅ User Registration & Login with JWT  
✅ Email Verification Flow (with token expiry)  
✅ Password Reset via Email  
✅ Refresh Token Handling  
✅ Secure Cookie-Based Auth  
✅ Input Validation with Express-Validator  
✅ Centralized Error Handling  
✅ Health Check Endpoint  

---

## 🛠 Tech Stack

| Category | Technology |
|-----------|-------------|
| **Runtime** | Node.js |
| **Framework** | Express.js |
| **Database** | MongoDB + Mongoose |
| **Authentication** | JWT (Access & Refresh Tokens) |
| **Mail Service** | Nodemailer + Mailgen |
| **Security** | Cookie-parser, CORS |
| **Environment** | dotenv |

---

## API Endpoints

```
| Method | Endpoint                             | Description                            |
| ------ | ------------------------------------ | -------------------------------------- |
| GET    | `/api/v1/healthcheck`                | Check server status                    |
| POST   | `/api/v1/auth/register`              | Register user & send verification mail |
| POST   | `/api/v1/auth/login`                 | Login and get tokens                   |
| POST   | `/api/v1/auth/logout`                | Logout user                            |
| GET    | `/api/v1/auth/verify-email/:token`   | Verify user email                      |
| POST   | `/api/v1/auth/forgot-password`       | Send password reset email              |
| POST   | `/api/v1/auth/reset-password/:token` | Reset password                         |
| GET    | `/api/v1/auth/current-user`          | Get logged-in user                     |
```
---

## Folder Structure

```
project-management/
│
├── node_modules/ # Project dependencies
│
├── notes/ # Learning notes or project references
│ └── NOTES.md
│
├── public/ # Public assets
│ └── images/
│
├── src/
│ ├── controllers/ # Route controllers (business logic)
│ │ ├── auth.controller.js
│ │ └── healthCheck.controller.js
│ │
│ ├── db/ # Database configuration and connection
│ │ └── index.js
│ │
│ ├── middlewares/ # Express middlewares
│ │ ├── auth.middleware.js
│ │ └── validator.middleware.js
│ │
│ ├── models/ # Mongoose schemas and models
│ │ └── user.model.js
│ │
│ ├── routes/ # Express routes
│ │ ├── auth.routes.js
│ │ └── healthCheck.routes.js
│ │
│ ├── utils/ # Utility functions and helpers
│ │ ├── api-error.js
│ │ ├── api-response.js
│ │ ├── async-handler.js
│ │ ├── constants.js
│ │ └── mail.js
│ │
│ ├── validators/ # Request data validators
│ │ └── index.js
│ │
│ ├── app.js # Express app configuration
│ └── index.js # Entry point for server startup
│
├── .env # Environment variables
├── .prettierrc # Prettier configuration
├── .prettierignore # Files ignored by Prettier
├── package.json # Project metadata and scripts
├── package-lock.json # Dependency lock file
├── PRD.md # Project documentation / product requirements
└── README.md # Project overview and documentation
```

---

## ⚙️ Setup Instructions

### 1 Clone the Repository
  ```bash
    git clone https://github.com/<your-username>/project-management-backend.git
    cd project-management-backend
  ```

### 2 Install Dependencies
  ```bash
    npm install 
  ```

### 3 Configure Environment Variables

-Create a .env file at the root:

  ```bash
    PORT=8000
    MONGODB_URI=your_mongodb_connection_string
    CORS_ORIGIN=*
    ACCESS_TOKEN_SECRET=your_access_secret
    REFRESH_TOKEN_SECRET=your_refresh_secret
    REFRESH_TOKEN_EXPIRY=10d
    REFRESH_TOKEN_SECRET=your_refresh_secret
    FORGOT_PASSWORD_REDIRECT_URL=http://localhost:3000/forgot-password
    MAIL_SMTP_HOST=sandbox.smtp.mailtrap.io
    MAIL_SMTP_PORT=your_mail_smtp_port
    MAIL_SMTP_USER=your_mail_smtp_user
    MAIL_SMTP_PASS=your_mail_smtp_pass

  ```

### 4 Start the Server

  ```bash
    npm run dev
  ```  


Server will start at http://localhost:5000

## Author

**Kunj Pandya**  
 MERN Stack Developer • Building & Learning  
 Connect with me on [GitHub](https://github.com/kunj-pandya)

---

## License

This project is licensed under the **MIT License** — free to use, modify, and learn from.
