# JnU Health Care Mobile Application

<div align="center">
  <img src="JnU-Health-Care-Frontend/assets/jnu-logo-png.png" alt="JnU Logo" width="200"/>
  
  **A comprehensive digital health care solution for Jagannath University students**
  
  [![React Native](https://img.shields.io/badge/React%20Native-0.72.6-blue.svg)](https://reactnative.dev/)
  [![Expo](https://img.shields.io/badge/Expo-49.0.13-black.svg)](https://expo.dev/)
  [![Node.js](https://img.shields.io/badge/Node.js-Express-green.svg)](https://nodejs.org/)
  [![MongoDB](https://img.shields.io/badge/Database-MongoDB-brightgreen.svg)](https://mongodb.com/)
  [![License](https://img.shields.io/badge/License-ISC-yellow.svg)](LICENSE)
</div>

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Features](#-features)
- [Technology Stack](#-technology-stack)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Running the Application](#-running-the-application)
- [API Documentation](#-api-documentation)
- [Mobile App Features](#-mobile-app-features)
- [Contributing](#-contributing)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)
- [Contact](#-contact)

## 🎯 Project Overview

The **JnU Health Care Mobile Application** is a comprehensive digital solution designed to modernize and streamline mental health and counseling services at Jagannath University. This full-stack application consists of a React Native mobile frontend and a Node.js/Express backend, providing students with easy access to psychological support, appointment booking, and health resources.

### Problem Statement

Traditional counseling services at universities face several challenges:
- **Manual Processes**: Physical form collection and paper-based workflows
- **Accessibility Issues**: Limited access to counseling services and resources
- **Poor Communication**: Lack of direct communication channels with psychologists
- **No Digital Records**: Absence of digital appointment and session tracking
- **Limited Resources**: Insufficient access to mental health articles and resources

### Our Solution

This application digitizes and modernizes the entire counseling ecosystem by providing:
- **Digital Form Submission**: Electronic counseling forms and applications
- **Appointment Management**: Easy booking and tracking of counseling sessions
- **Psychologist Profiles**: Browse and connect with available mental health professionals
- **Health Articles**: Access to curated mental health resources and articles
- **User Profiles**: Personalized user accounts with session history
- **Mobile-First Design**: Native mobile experience optimized for students

## ✨ Features

### 🔐 Authentication & User Management
- Secure user registration and login
- JWT-based authentication
- Password reset functionality
- Profile management with image upload
- Role-based access control

### 📅 Appointment System
- Browse available psychologists
- Book counseling appointments
- View appointment history
- Cancel or reschedule appointments
- Real-time appointment status updates

### 👨‍⚕️ Psychologist Management
- Psychologist profile creation and management
- Availability scheduling
- Patient interaction tools
- Professional credentials display

### 📚 Health Resources
- Curated mental health articles
- Educational content library
- Resource categorization
- Bookmark favorite articles

### 📱 Mobile Experience
- Native React Native interface
- Cross-platform compatibility (iOS/Android)
- Offline capability for basic features
- Push notifications for appointments
- Responsive design with custom fonts

## 🛠 Technology Stack

### Frontend (Mobile App)
- **Framework**: React Native 0.72.6
- **Development Platform**: Expo 49.0.13
- **Navigation**: React Navigation 6.x
- **UI Styling**: NativeWind (Tailwind CSS for React Native)
- **State Management**: React Context API
- **HTTP Client**: Axios
- **Additional Libraries**:
  - Expo Vector Icons
  - React Native SVG
  - React Native Swiper
  - React Native Toast Message
  - Expo Image Picker

### Backend (API Server)
- **Runtime**: Node.js
- **Framework**: Express.js 4.18.2
- **Database**: MongoDB with Mongoose ODM 8.0.1
- **Authentication**: JSON Web Tokens (JWT) 9.0.2
- **Password Hashing**: bcrypt 5.1.1
- **File Upload**: Multer 1.4.5
- **Email Service**: Nodemailer 6.9.8
- **Environment Management**: dotenv 16.3.1

### Development Tools
- **Backend Development**: Nodemon 3.0.2
- **Build Tools**: Babel Core, Expo CLI
- **Version Control**: Git

## 📁 Project Structure

```
JnU-Health-Care-Expo-Nodejs-App/
├── JnU-Health-Care-backend/          # Node.js/Express API Server
│   ├── controller/                   # Route controllers
│   │   ├── artical.js               # Article management
│   │   ├── email.js                 # Email services
│   │   ├── forgotPassword.js        # Password reset
│   │   ├── form.js                  # Form submissions
│   │   ├── login.js                 # User authentication
│   │   ├── profile.js               # User profiles
│   │   ├── psychologist.js          # Psychologist management
│   │   └── signup.js                # User registration
│   ├── middleware/                   # Express middlewares
│   │   ├── isAuth.js                # Authentication middleware
│   │   └── multerPicture.js         # File upload middleware
│   ├── model/                        # MongoDB/Mongoose models
│   │   ├── appointment.js           # Appointment schema
│   │   ├── article.js               # Article schema
│   │   ├── psychologist.js          # Psychologist schema
│   │   ├── signupSchema.js          # User schema
│   │   └── token.js                 # Token schema
│   ├── router/                       # API route definitions
│   │   ├── appointmentRouter.js     # Appointment routes
│   │   ├── articleRouter.js         # Article routes
│   │   ├── authenticationRouter.js  # Auth routes
│   │   ├── profileRouter.js         # Profile routes
│   │   └── psychologistsRouter.js   # Psychologist routes
│   ├── uploads/                      # File storage directory
│   ├── index.js                      # Server entry point
│   ├── index.html                    # API documentation page
│   └── package.json                  # Backend dependencies
│
├── JnU-Health-Care-Frontend/         # React Native Mobile App
│   ├── App/                          # Main application code
│   │   ├── api/                      # API client configuration
│   │   ├── Components/               # Reusable UI components
│   │   │   ├── ArticleCard.jsx      # Article display component
│   │   │   ├── DoctorCard.jsx       # Doctor profile component
│   │   │   ├── InputField.jsx       # Form input component
│   │   │   └── Home/                # Home screen components
│   │   ├── context/                  # React Context providers
│   │   ├── Navigations/              # Navigation configuration
│   │   └── Screens/                  # Application screens
│   │       ├── Appointment.jsx      # Appointment booking
│   │       ├── Articles.jsx         # Articles listing
│   │       ├── Doctors.jsx          # Doctor profiles
│   │       ├── Home.jsx             # Home dashboard
│   │       ├── Login.jsx            # Login screen
│   │       ├── Profile.jsx          # User profile
│   │       └── Registration.jsx     # User registration
│   ├── assets/                       # Static assets
│   │   ├── fonts/                   # Custom fonts
│   │   └── Shared/                  # Shared configurations
│   ├── App.js                        # App entry point
│   ├── app.json                      # Expo configuration
│   └── package.json                  # Frontend dependencies
│
└── README.md                         # This file
```

## 📋 Prerequisites

Before setting up the project, ensure you have the following installed:

- **Node.js** (version 16.x or higher)
- **npm** or **yarn** package manager
- **MongoDB** (local installation or MongoDB Atlas account)
- **Expo CLI** (`npm install -g @expo/cli`)
- **Git** for version control
- **Android Studio** (for Android development)
- **Xcode** (for iOS development, macOS only)

### For Mobile Development
- **Expo Go** app on your mobile device (for testing)
- **Android SDK** (if running on Android emulator)
- **iOS Simulator** (if developing on macOS)

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/JnU-Health-Care-Expo-Nodejs-App.git
cd JnU-Health-Care-Expo-Nodejs-App
```

### 2. Backend Setup

```bash
# Navigate to backend directory
cd JnU-Health-Care-backend

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Or create .env file manually with required variables
```

### 3. Frontend Setup

```bash
# Navigate to frontend directory
cd ../JnU-Health-Care-Frontend

# Install dependencies
npm install

# Install Expo CLI globally (if not already installed)
npm install -g @expo/cli
```

## ⚙️ Configuration

### Backend Environment Variables

Create a `.env` file in the `JnU-Health-Care-backend` directory with the following variables:

```env
# Server Configuration
PORT=3000
NODE_ENV=development

# MongoDB Configuration
MONGODB_URI=mongodb://localhost:27017/jnu_healthcare
# Or for MongoDB Atlas:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/jnu_healthcare

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key
JWT_EXPIRE=7d

# Email Configuration (for Nodemailer)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password

# File Upload Configuration
MAX_FILE_SIZE=5242880  # 5MB in bytes
UPLOAD_PATH=uploads/

# API Configuration
API_VERSION=v1
```

### Frontend Configuration

Update the API endpoint in `JnU-Health-Care-Frontend/App/api/client.js`:

```javascript
// For local development
const baseURL = 'http://localhost:3000';

// For production
// const baseURL = 'https://your-api-domain.com';
```

## 🏃‍♂️ Running the Application

### Start the Backend Server

```bash
# Navigate to backend directory
cd JnU-Health-Care-backend

# Start the server in development mode
npm run dev
# Or start normally
npm start

# The server will run on http://localhost:3000
```

### Start the Mobile App

```bash
# Navigate to frontend directory
cd JnU-Health-Care-Frontend

# Start the Expo development server
npm start
# Or
expo start

# Options to run on specific platforms:
npm run android    # Run on Android device/emulator
npm run ios        # Run on iOS simulator (macOS only)
npm run web        # Run in web browser
```

### Development Workflow

1. **Start Backend**: Run the Node.js server first
2. **Start Frontend**: Launch the Expo development server
3. **Test on Device**: Scan QR code with Expo Go app or use emulators
4. **Hot Reload**: Both frontend and backend support hot reloading for development

## 📖 API Documentation

### Authentication Endpoints

| Method | Endpoint | Description | Authentication |
|--------|----------|-------------|----------------|
| POST | `/auth/signup` | User registration | No |
| POST | `/auth/login` | User login | No |
| POST | `/auth/forgot-password` | Password reset request | No |
| POST | `/auth/reset-password` | Reset password with token | No |

### User Profile Endpoints

| Method | Endpoint | Description | Authentication |
|--------|----------|-------------|----------------|
| GET | `/profile/` | Get user profile | Yes |
| PUT | `/profile/update` | Update user profile | Yes |
| POST | `/profile/upload-image` | Upload profile image | Yes |

### Appointment Endpoints

| Method | Endpoint | Description | Authentication |
|--------|----------|-------------|----------------|
| GET | `/appointment/` | Get user appointments | Yes |
| POST | `/appointment/book` | Book new appointment | Yes |
| PUT | `/appointment/:id` | Update appointment | Yes |
| DELETE | `/appointment/:id` | Cancel appointment | Yes |

### Psychologist Endpoints

| Method | Endpoint | Description | Authentication |
|--------|----------|-------------|----------------|
| GET | `/psychologist/` | Get all psychologists | No |
| GET | `/psychologist/:id` | Get psychologist details | No |
| POST | `/psychologist/register` | Register as psychologist | Yes |
| PUT | `/psychologist/profile` | Update psychologist profile | Yes |

### Article Endpoints

| Method | Endpoint | Description | Authentication |
|--------|----------|-------------|----------------|
| GET | `/article/` | Get all articles | No |
| GET | `/article/:id` | Get specific article | No |
| POST | `/article/create` | Create new article | Yes (Admin) |
| PUT | `/article/:id` | Update article | Yes (Admin) |

### Request/Response Examples

#### User Registration
```javascript
// POST /auth/signup
{
  "name": "John Doe",
  "email": "john@jnu.ac.bd",
  "password": "securePassword123",
  "studentId": "2021-001",
  "department": "Computer Science"
}

// Response
{
  "success": true,
  "message": "User registered successfully",
  "user": {
    "id": "...",
    "name": "John Doe",
    "email": "john@jnu.ac.bd"
  },
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
}
```

#### Book Appointment
```javascript
// POST /appointment/book
{
  "psychologistId": "64f5a6b2c8e4d12345678901",
  "preferredDate": "2024-01-15",
  "preferredTime": "14:00",
  "reason": "Anxiety management",
  "notes": "First time seeking counseling"
}

// Response
{
  "success": true,
  "message": "Appointment booked successfully",
  "appointment": {
    "id": "...",
    "psychologist": {...},
    "date": "2024-01-15",
    "time": "14:00",
    "status": "pending"
  }
}
```

## 📱 Mobile App Features

### Screen Flow

1. **Welcome/Login Screen**: User authentication
2. **Home Dashboard**: Overview of services and quick actions
3. **Doctor Profiles**: Browse available psychologists
4. **Appointment Booking**: Schedule counseling sessions
5. **Articles**: Mental health resources and education
6. **Profile Management**: Personal information and settings
7. **Contact**: Support and emergency contacts

### Key Components

- **Custom Input Fields**: Styled form inputs with validation
- **Doctor Cards**: Psychologist profile display with ratings
- **Article Cards**: Preview cards for health articles
- **Navigation**: Bottom tab navigation with custom icons
- **Toast Messages**: User feedback and notifications

### Styling and Theming

The app uses a custom color scheme and typography:

```javascript
// Colors (assets/Shared/Colours.js)
primary: '#2E86AB',
secondary: '#A23B72',
background: '#F8F9FA',
text: '#333333',
light: '#FFFFFF'
```

Custom fonts include:
- **Roboto**: Main UI text
- **Hindi Siliguri**: Bengali text support
- **Inter**: Additional UI elements

## 🤝 Contributing

We welcome contributions to the JnU Health Care Application! Please follow these guidelines:

### Development Guidelines

1. **Code Style**: Follow JavaScript/React Native best practices
2. **Commits**: Use conventional commit messages
3. **Testing**: Add tests for new features
4. **Documentation**: Update documentation for API changes

### How to Contribute

1. **Fork the Repository**
   ```bash
   git fork https://github.com/your-username/JnU-Health-Care-Expo-Nodejs-App.git
   ```

2. **Create Feature Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make Changes and Test**
   ```bash
   # Make your changes
   # Test thoroughly on both platforms
   ```

4. **Commit and Push**
   ```bash
   git commit -m "feat: add new appointment reminder feature"
   git push origin feature/your-feature-name
   ```

5. **Create Pull Request**
   - Provide clear description of changes
   - Include screenshots for UI changes
   - Link any related issues

### Reporting Issues

When reporting bugs or requesting features:

1. Check existing issues first
2. Use issue templates when available
3. Provide detailed reproduction steps
4. Include environment information
5. Add screenshots or logs if applicable

## 🔧 Troubleshooting

### Common Backend Issues

**MongoDB Connection Failed**
```bash
# Check MongoDB status
sudo systemctl status mongod

# Start MongoDB service
sudo systemctl start mongod

# Check connection string in .env file
```

**Port Already in Use**
```bash
# Find process using port 3000
lsof -i :3000

# Kill the process
kill -9 <PID>

# Or use different port in .env
PORT=3001
```

**JWT Authentication Errors**
```bash
# Verify JWT_SECRET in .env
# Check token expiration settings
# Ensure middleware is properly configured
```

### Common Frontend Issues

**Expo Start Fails**
```bash
# Clear Expo cache
expo start -c

# Reset Metro bundler cache
npx react-native start --reset-cache

# Reinstall node_modules
rm -rf node_modules && npm install
```

**Network Request Failed**
```bash
# Check API endpoint in client.js
# Ensure backend server is running
# Verify network permissions in app.json
```

**Android Build Issues**
```bash
# Clear Gradle cache
cd android && ./gradlew clean

# Check Android SDK configuration
# Verify build tools version
```

**iOS Build Issues (macOS)**
```bash
# Clean iOS build folder
cd ios && rm -rf build/

# Update CocoaPods
cd ios && pod install --repo-update

# Check Xcode version compatibility
```

### Performance Optimization

**Backend Performance**
- Use MongoDB indexes for frequently queried fields
- Implement API response caching
- Optimize image upload and storage
- Use pagination for large data sets

**Frontend Performance**
- Implement lazy loading for screens
- Optimize image loading and caching
- Use FlatList for large lists
- Minimize re-renders with React.memo

### Deployment Considerations

**Backend Deployment**
- Use environment-specific configurations
- Set up proper logging and monitoring
- Configure CORS for production domains
- Use HTTPS in production

**Mobile App Deployment**
- Build optimized bundles for app stores
- Configure app signing and certificates
- Set up push notification services
- Test on various device sizes and OS versions

## 📄 License

This project is licensed under the ISC License. See the [LICENSE](LICENSE) file for details.

## 📞 Contact

**Project Maintainer**: Nahid
- **Email**: [contact email]
- **GitHub**: [GitHub profile]

**Institution**: Jagannath University
- **Department**: [Department Name]
- **Project Type**: Academic/Research Project

**Support**
- Create an issue for bug reports
- Join our [Discord/Slack] for discussions
- Email for sensitive security issues

---

<div align="center">
  <p>Made with ❤️ for Jagannath University Students</p>
  <p>Supporting Mental Health and Wellness in Higher Education</p>
</div>
