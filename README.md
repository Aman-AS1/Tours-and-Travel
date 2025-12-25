# Tours and Travel 🌍✈️

A comprehensive tours and travel management system built with Node.js, Express, and modern web technologies. This application provides a platform for managing tourist destinations and travel services.

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- **Tour Management**: Browse and manage various tour packages
- **User Authentication**: Secure user registration and login system
- **Booking System**: Easy-to-use booking interface for tours
- **Admin Panel**: Administrative controls for managing tours and bookings
- **Responsive Design**: Mobile-friendly user interface
- **RESTful API**: Well-structured API endpoints

## 🛠 Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Frontend**: HTML, CSS, JavaScript
- **Additional Tools**: Various utility libraries

## 📁 Project Structure

```
Tours-and-Travel/
├── controllers/      # Request handlers and business logic
├── models/          # Database models and schemas
├── routes/          # API route definitions
├── utils/           # Helper functions and utilities
├── public/          # Static files (CSS, JS, images)
├── app.js           # Express application setup
├── server.js        # Server configuration and startup
├── package.json     # Project dependencies and scripts
└── .gitignore       # Git ignore rules
```

## 📦 Prerequisites

Before running this application, ensure you have the following installed:

- **Node.js** (v14.x or higher)
- **npm** or **yarn**
- **MongoDB** (local installation or MongoDB Atlas account)
- **Git**

## 🚀 Installation

1. **Clone the repository**

```bash
git clone https://github.com/Aman-AS1/Tours-and-Travel.git
cd Tours-and-Travel
```

2. **Install dependencies**

```bash
npm install
```

## ⚙️ Configuration

1. **Create environment variables file**

Create a `.env` file in the root directory:

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# Database Configuration
DATABASE_URL=mongodb://localhost:27017/tours-and-travel
# OR for MongoDB Atlas
# DATABASE_URL=mongodb+srv://<username>:<password>@cluster.mongodb.net/tours-and-travel

# Authentication
JWT_SECRET=your_jwt_secret_key_here
JWT_EXPIRES_IN=90d

# Other configurations
SESSION_SECRET=your_session_secret_here
```

2. **Database Setup**

Ensure your MongoDB server is running, or configure your MongoDB Atlas connection string.

## 🏃 Running the Application

### Development Mode

```bash
npm run dev
```

### Production Mode

```bash
npm start
```

The application will be available at `http://localhost:3000`

## 📚 API Documentation

### Base URL

```
http://localhost:3000/api
```

### Main Endpoints

#### Tours
- `GET /api/tours` - Get all tours
- `GET /api/tours/:id` - Get single tour by ID
- `POST /api/tours` - Create new tour (Admin only)
- `PATCH /api/tours/:id` - Update tour (Admin only)
- `DELETE /api/tours/:id` - Delete tour (Admin only)

#### Users
- `POST /api/users/signup` - Register new user
- `POST /api/users/login` - User login
- `GET /api/users/profile` - Get user profile
- `PATCH /api/users/update-profile` - Update user profile

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
5. Push to the branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request

### Contribution Guidelines

- Follow the existing code style
- Write clear commit messages
- Add comments for complex logic
- Test your changes thoroughly
- Update documentation as needed

## 📝 Scripts

```bash
# Start the server
npm start

# Run in development mode with nodemon
npm run dev

# Run tests (if configured)
npm test

# Lint code
npm run lint
```

## 🐛 Troubleshooting

### Common Issues

1. **MongoDB Connection Error**
   - Ensure MongoDB is running
   - Check your connection string in `.env`
   - Verify network connectivity for Atlas

2. **Port Already in Use**
   - Change the PORT in `.env` file
   - Kill the process using the port: `lsof -ti:3000 | xargs kill -9` (macOS/Linux)

3. **Module Not Found**
   - Run `npm install` to install dependencies
   - Clear node_modules and reinstall: `rm -rf node_modules && npm install`

## 👨‍💻 Author

**Aman AS**
- GitHub: [@Aman-AS1](https://github.com/Aman-AS1)

## 🙏 Acknowledgments

- Thanks to all contributors who have helped shape this project
- Inspired by modern travel booking platforms
- Built with love for travelers worldwide

---

**Note**: This is a learning/portfolio project. Please configure proper security measures before deploying to production.

For questions or support, please open an issue on GitHub.
