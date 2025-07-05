# Library Management System API

A RESTful API built with **Node.js**, **Express.js**, **TypeScript**, and **MongoDB** to manage books and borrowing operations for a library system.The Library Management System, a backend application designed to manage books and borrowing operations efficiently in a digital library environment. This system focuses on creating a seamless experience for managing inventory and borrowing records using modern RESTful API practices.
---

**Live URL**: [Visit the live site](https://bookbuddy-server-chi.vercel.app/)


## 📂 Repositories

- **Client:** [Library-Management-Client (React TypeScript	Redux Toolkit  RTK Query Client)](https://github.com/Tanim-Ahmmed/Library-Management-System-Server)  
- **Server:** [Library Management-Server (Node.js, Express.js, TypeScript,  Backend)](https://github.com/Tanim-Ahmmed/Library-Management-System-Server)

##  Features

-  Book Management (CRUD)
-  Borrow books with stock validation
-  Borrow summary aggregation
-  Mongoose schema validations & methods
-  Organized route and service layers
-  Testable with Postman

---

## Tech Stack

- **Backend:** Express.js + TypeScript
- **Database:** MongoDB Atlas + Mongoose
- **Utilities:** dotenv, cors

---

##  Project Setup

###  Clone the ropo:

```json
git clone https://github.com/Tanim-Ahmmed/Library-Management-System-with-Express-MongoDB-and-Mongoose/tree/main
cd library-management-system
```

###  Install dependencies:

```
npm install 
```
### Set environment variables (via .env or config file):

```
DB_USER=your_mongo_username
DB_PASS=your_mongo_password
PORT=5000
```
### Run the development server:
```
npm run dev
```

## Root Endpoint

**GET /** → Welcome message

**POST /api/books** → Create a new book

**GET /api/books** → Get all books (with optional filters: genre, sort, limit)

**GET /api/books/:bookId** → Get a specific book by ID

**Put /api/books/:bookId** → Update a book

**DELETE /api/books/:bookId** → Delete a book

**POST /api/borrow** → Borrow a book

**GET /api/borrow** → Get total borrowed summary by book


## Project File Structure 

```plaintext
library-management-system/
│
├── app/
│   ├── modules/
│   │   ├── Book/
│   │   │   ├── books.controller.ts
│   │   │   ├── books.interface.ts
│   │   │   ├── books.model.ts
│   │   │   ├── books.routes.ts
│   │   │   └── books.service.ts
│   │   │
│   │   └── Borrow/
│   │       ├── borrow.controller.ts
│   │       ├── borrow.interface.ts
│   │       ├── borrow.model.ts
│   │       ├── borrow.routes.ts
│   │       └── borrow.service.ts
│
├── config/
│   └── config.ts         # Environment variable configuration
│
├── node_modules/         # Installed dependencies
│
├── .env                  # Environment variables (not pushed to GitHub)
├── .gitignore            # Ignored files and folders
├── package.json          # NPM package definitions and scripts
├── tsconfig.json         # TypeScript configuration
├── app.ts                # Main Express app setup
├── server.ts             # MongoDB connection and app startup
├── README.md             # Project documentation
```

## Notes:

- app.ts – Express middleware and route setup

- server.ts – Connects to MongoDB and starts the server

- config/config.ts – Reads values from .env or hardcoded (like DB_USER,   DB_PASS)

- Each module (Book, Borrow) is isolated with its own controller, service, model, and interface files

- Use .env for secrets and config separation.