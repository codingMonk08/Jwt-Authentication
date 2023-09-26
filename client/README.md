# Web Application Readme

This is a readme file for a web application that provides user authentication features using various technologies for both the backend and frontend. The application allows users to sign up, log in, and log out using their email and password. Below, you will find an overview of the technologies used and the key features of this web application.

## Backend

### Technologies Used

- **Node.js**: The server-side runtime environment.
- **Express**: The web framework for building the server.
- **MongoDB**: The database for storing user data.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB.
- **bcrypt**: A library for hashing and securing passwords.
- **dotenv**: For loading environment variables.
- **cookie-parser**: For handling cookies.
- **cors**: For enabling Cross-Origin Resource Sharing.
- **email-validator**: For validating email addresses.
- **jsonwebtoken (JWT)**: For creating and verifying JSON Web Tokens.
- **nodemon**: A development tool for automatically restarting the server during development.

### Features

- **User Registration**: Users can sign up by providing their email and password. The password is securely hashed using bcrypt before being stored in the database. Email addresses are validated using email-validator to ensure they are in the correct format.

- **User Authentication**: Users can log in with their registered email and password. Upon successful authentication, the server generates a JSON Web Token (JWT), which is stored in a cookie using cookie-parser and cors. This token is used to authenticate the user for accessing protected routes on the server.

- **Protected Routes**: Certain routes on the server are protected, meaning they require a valid JWT to access. This ensures that only authenticated users can perform certain actions.

- **Secure Password Handling**: User passwords are securely hashed using bcrypt before being stored in the MongoDB database. This ensures that even if the database is compromised, user passwords remain secure.

## Frontend

### Technologies Used

- **React**: The JavaScript library for building user interfaces.
- **axios**: A library for making HTTP requests to the backend.

### Features

- **User Interface**: The frontend is built using React to provide a user-friendly interface. It includes the following components:
  - Sign-up form: Allows users to create an account.
  - Log-in form: Allows users to log in with their credentials.
  - Log-out button: Allows users to log out.
  - User information display: Shows the user's email and a welcome message when they are logged in.

- **State Management**: React hooks are used to manage the state of the user's authentication status and JWT. This ensures that the user interface updates appropriately based on the user's login status.

## Getting Started

To run this web application locally, follow these steps:

1. Clone the repository to your local machine.

2. Navigate to the project directory in your terminal.

3. Install backend dependencies:
   ```
   cd backend
   npm install
   ```

4. Create a `.env` file in the `backend` directory with the following variables:
   ```
   MONGODB_URI=<your MongoDB URI>
   JWT_SECRET=<your JWT secret>
   ```

5. Start the backend server:
   ```
   npm start
   ```

6. Install frontend dependencies:
   ```
   cd ../frontend
   npm install
   ```

7. Start the frontend:
   ```
   npm start
   ```

8. Access the application in your web browser at `http://localhost:3000`.

## Deployment

To deploy this web application to a production environment, you will need to configure a production-ready database, set appropriate environment variables, and choose a hosting platform for both the backend and frontend.

## Conclusion

This web application provides user authentication functionality with secure password handling and a user-friendly frontend built with React. Users can sign up, log in, and enjoy a personalized experience with their email and JWT. The backend is powered by Node.js and Express, while MongoDB stores user data securely. Enjoy using and customizing this web application for your needs!