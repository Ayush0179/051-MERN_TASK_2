# Campus Account Portal

A full-stack web application built using the **MERN stack** that provides user registration and login functionality with secure password hashing and MongoDB database integration.

## 🚀 Features

- **User Registration** — Create an account using your name, email address, and password.
- **User Login** — Verify registered users using their email and password.
- **Password Security** — Passwords are hashed using `bcryptjs` before being stored in the database.
- **MongoDB Integration** — Store user account information using MongoDB and Mongoose.
- **Input Validation** — Validate user details and handle invalid inputs.
- **Duplicate Account Prevention** — Prevent registration with an email address that already exists.
- **Responsive Interface** — A clean, modern authentication interface built with React.
- **REST API** — Backend endpoints built using Express.js.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| MongoDB Atlas | Cloud database |
| Express.js | Backend API framework |
| React.js | Frontend user interface |
| Node.js | JavaScript runtime |
| Mongoose | MongoDB object modelling |
| bcryptjs | Password hashing |
| React Router | Frontend navigation |
| Vite | Frontend development server |
| CSS | Application styling |

## 📁 Project Structure

```text
campus-account-portal/
├── client/
│   ├── public/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Login.jsx
│   │   │   └── Register.jsx
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   └── index.css
│   ├── package.json
│   └── index.html
│
├── server/
│   ├── models/
│   │   └── User.js
│   ├── routes/
│   │   └── auth.js
│   ├── .env
│   ├── server.js
│   └── package.json
│
├── .gitignore
└── README.md
```

## ⚙️ Prerequisites

Before running the project, make sure you have:

- [Node.js](https://nodejs.org/) installed.
- npm installed with Node.js.
- A [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account or another MongoDB instance.
- [Git](https://git-scm.com/) installed (optional, for version control).

## 📥 Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/campus-account-portal.git
cd campus-account-portal
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Set up the backend

Open a terminal in the project root:

```bash
cd server
npm install
```

Create a `.env` file inside the `server` folder:

```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
```

Replace `your_mongodb_connection_string` with your MongoDB Atlas connection string. Ensure your database credentials and network access settings are configured correctly.

**Important:** Never commit or publish your `.env` file or expose your database credentials.

Start the backend:

```bash
npm run dev
```

The API should be available at:

`http://localhost:5000`

### 3. Set up the frontend

Open a **second terminal** in the project root:

```bash
cd client
npm install
npm run dev
```

Open the local URL displayed in the terminal, usually:

`http://localhost:5173`

## 🔌 API Endpoints

Base URL: `http://localhost:5000/api/auth`

| Method | Endpoint | Description |
|---|---|---|
| POST | `/register` | Register a new user |
| POST | `/login` | Verify a user's login credentials |

### Register a user

**Request body:**

```json
{
  "name": "Alex Johnson",
  "email": "alex@example.com",
  "password": "examplePassword123"
}
```

### Log in

**Request body:**

```json
{
  "email": "alex@example.com",
  "password": "examplePassword123"
}
```

The API returns a response indicating whether registration or login succeeded, along with safe user information where applicable.

## 🔒 Security Notes

- Passwords are hashed before being saved to the database.
- The password field is excluded from normal user queries.
- User input is validated on the backend.
- Database credentials should be stored in environment variables.
- The current login implementation verifies credentials but does **not** establish a persistent authenticated session or issue an authentication token.

For production deployment, add session or token-based authentication, protected backend routes, rate limiting, and appropriate security configuration.

## 🧪 Testing

1. Start the backend and frontend in separate terminals.
2. Open the application in your browser.
3. Register a new account.
4. Check that the account is stored in MongoDB.
5. Log in using the registered email and password.
6. Test invalid credentials and duplicate email registration.

You can also check backend health at:

`http://localhost:5000/api/health`

## 🔮 Future Enhancements

- User dashboard
- Persistent authentication with JWT or secure sessions
- Protected routes
- Forgot password and password reset
- User profile management
- Email verification
- Improved form validation and error handling
- Deployment to a cloud hosting platform

## 👨‍💻 Author

AYUSH R

GitHub: [Your GitHub Profile](https://github.com/Ayush0179)

## 📄 License

This project is intended for educational and learning purposes. Add a license if you intend to distribute it under specific reuse terms.
