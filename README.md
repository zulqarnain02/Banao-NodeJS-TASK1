# Authentication System with Forgot Password

This project implements a secure authentication system with user login, registration, forgot password, and reset password functionalities. The project uses React for the frontend and Node.js with Express for the backend.

## Features
- **User Registration**: Allows users to create an account by providing basic details (email, password, etc.).
- **User Login**: Allows registered users to log in with their credentials.
- **Forgot Password**: Allows users to request a password reset link via email.
- **Reset Password**: Provides a form to allow users to set a new password using a unique token received in the reset email.
- **Logout**: Allows users to securely log out by removing the JWT token from localStorage.

## Tech Stack
- **Frontend**:
  - React
  - Axios for API requests
  - TailwindCSS for styling
- **Backend**:
  - Node.js
  - Express.js
  - MongoDB with Mongoose for database management
  - JWT for user authentication
  - Nodemailer for email handling (used for sending password reset emails)
  - Bcrypt for password hashing

## Installation

### Backend (API)
1. Clone the repository:  
   `git clone https://github.com/your-username/repository-name.git`  
   `cd repository-name/api`

2. Install dependencies:  
   `npm install`

3. Set up environment variables by creating a `.env` file and adding the following:  
   ```bash
   JWT_SECRET=your_jwt_secret_key  
   EMAIL_HOST=smtp.mailtrap.io  
   EMAIL_PORT=2525  
   EMAIL_USER=your_mailtrap_username  
   EMAIL_PASS=your_mailtrap_password
   ```

4. Start the backend server:  
   `npm start`

### Frontend (React)
1. Navigate to the `client` folder:  
   `cd client`

2. Install dependencies:  
   `npm install`

3. Start the frontend development server:  
   `npm start`

## Routes

### Auth Routes
- **POST /register**: Register a new user.
- **POST /login**: Log in a user and return a JWT token.
- **POST /forgot-password**: Send a password reset link to the user's email.
- **POST /reset-password/:token**: Reset the user's password using a valid token.

## How to Use
1. **Register**: Navigate to the `/register` page, provide your details, and click "Register."
2. **Login**: After registering, you can log in using your email and password on the `/login` page.
3. **Forgot Password**: If you've forgotten your password, click the "Forgot Password" link on the login page, provide your email, and click "Send Reset Link."
4. **Reset Password**: You will receive an email with a reset link. Click the link to navigate to the password reset page where you can set a new password.
5. **Logout**: After logging in, you can click the "Logout" button to securely log out.

## Contributing
- Fork the repository
- Create a new branch (`git checkout -b feature-name`)
- Commit your changes (`git commit -am 'Add new feature'`)
- Push to the branch (`git push origin feature-name`)
- Create a new pull request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
