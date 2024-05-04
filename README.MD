# Inventory Management Backend

This repository contains the backend code for an Inventory Management Application. It provides APIs for managing inventory items with CRUD operations, categorization, user authentication (signup and login) using JWT, and password hashing for security.

## Features

- **CRUD Operations:** Allows creating, reading, updating, and deleting inventory items.
- **Categories:** Supports categorization of inventory items for better organization and search.
- **User Authentication:** Provides endpoints for user signup and login using JWT for secure authentication.
- **Password Hashing:** Ensures the security of user passwords by hashing them before storing in the database.

## Technologies Used

- **Node.js:** The backend is developed using Node.js, a runtime environment for executing JavaScript code outside of a browser.
- **Express.js:** Utilized as the web application framework for Node.js to build robust APIs.
- **MongoDB:** A NoSQL database used for storing inventory data and user information.
- **JWT (JSON Web Tokens):** Employed for user authentication and authorization.
- **bcrypt:** Utilized for hashing passwords before storing them in the database.

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/inventory-management-backend.git

   ```

2. Install dependencies

   cd inventory-management-backend
   npm install

3. Set up environment variables:Create a .env file in the root directory and add the following variables:

   PORT=3000
   MONGODB_URI=mongodb://localhost:27017/inventory_management
   JWT_SECRET=your_secret_key

4. Start server
   
   npm run backend (With Nodemon)


## API Endpoints

1. User Authentication

   POST /api/auth/register: Register a new user.

   POST /api/auth/login: Authenticate a user and generate a JWT token.

   GET /api/auth/logout: Log out the current user.
   
   GET /api/auth/getuser: Get details of the currently logged-in user (Protected Route).
   
   GET /api/auth/loggedin: Check if a user is logged in.
   
   PATCH /api/auth/updateuser: Update user details (Protected Route).
   
   PATCH /api/auth/changepassword: Change user password (Protected Route).
   
   POST /api/auth/forgotpassword: Send reset password link to user's email.
   
   PUT /api/auth/resetpassword/:resetToken: Reset user password using reset token.

2. Inventory Management

   POST /api/products: Create a new product (Protected Route).

   GET /api/products: Get all products (Protected Route).

   GET /api/products/:id: Get a product by ID (Protected Route).

   PATCH /api/products/:id: Update a product by ID (Protected Route).

   DELETE /api/products/:id: Delete a product by ID (Protected Route).

3. Middlewares

   protect: Middleware for user authentication. Protects routes by verifying JWT token.
   
   upload: Middleware for handling file uploads using multer.



## Aryan Bahl