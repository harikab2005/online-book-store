# Online Bookstore

A modern, responsive online bookstore web application built with Node.js, Express, and Firebase. ReadMinds provides users with a seamless book browsing and purchasing experience.

## Features

### 🔐 User Authentication
- User registration and login system
- Password hashing with bcrypt
- Session management with express-session
- Protected routes for authenticated users

### 📚 Book Catalog
- Featured books showcase
- Free online books section
- Book search functionality
- Swiper-based carousels for book displays
- Responsive book grid layout

### 🛒 Shopping Experience
- Shopping cart functionality
- Payment processing page
- Multiple payment options (Debit/Credit Cards, UPI, Net Banking, Wallet)
- Order summary and confirmation

### 🎨 User Interface
- Modern, responsive design
- Mobile-friendly layout
- Interactive sliders and carousels
- Clean and intuitive navigation
- Font Awesome icons integration

## Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web application framework
- **Firebase Admin SDK** - Database and authentication
- **Firestore** - NoSQL database
- **bcrypt** - Password hashing
- **express-session** - Session management
- **body-parser** - Request body parsing

### Frontend
- **EJS** - Template engine
- **HTML5/CSS3** - Structure and styling
- **JavaScript** - Client-side functionality
- **Swiper.js** - Touch slider library
- **Font Awesome** - Icons
- **Google Fonts** - Typography

## Installation

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- Firebase project setup

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/online-book-store.git
   cd online-book-store
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Firebase Configuration**
   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Generate a service account key
   - Download the service account JSON file
   - Rename it to `key.json` and place it in the project root

4. **Environment Setup**
   - Update the session secret in `server.js`
   - Ensure Firebase configuration is properly set up

5. **Start the application**
   ```bash
   npm start
   ```
   or
   ```bash
   node server.js
   ```

6. **Access the application**
   Open your browser and navigate to `http://localhost:4000`

## Project Structure

```
online-book-store/
├── server.js              # Main server file
├── key.json              # Firebase service account key
├── package.json          # Dependencies and scripts
├── public/               # Static files
│   ├── styles.css       # Main stylesheet
│   ├── script.js        # Client-side JavaScript
│   ├── payment.css      # Payment page styles
│   ├── payment.js       # Payment functionality
│   └── images/          # Book images and assets
├── views/               # EJS templates
│   ├── dashboard.ejs    # Main dashboard page
│   ├── login.ejs        # Login page
│   ├── signup.ejs       # Registration page
│   └── payment.ejs      # Payment page
└── README.md           # Project documentation
```

## API Endpoints

### Authentication
- `GET /` - Redirect to login
- `GET /login` - Login page
- `GET /signup` - Registration page
- `POST /loginSubmit` - Handle login
- `POST /signupSubmit` - Handle registration
- `POST /logout` - User logout

### Main Application
- `GET /dashboard` - Main dashboard (protected)
- `GET /payment` - Payment page (protected)

## Database Schema

### Users Collection
```javascript
{
  email: "user@example.com",
  name: "User Name",
  password: "hashed_password"
}
```

## Features in Detail

### Authentication System
- Secure user registration with email validation
- Password hashing using bcrypt with salt rounds
- Session-based authentication
- Protected routes that redirect to login if not authenticated

### Book Management
- Featured books with pricing and discount information
- Free books section for promotional content
- Search functionality for book discovery
- Interactive book sliders using Swiper.js

### Payment Processing
- Multiple payment method support
- Secure payment form with validation
- Payment summary and confirmation
- Support for Indian payment methods (UPI, Net Banking)

### Responsive Design
- Mobile-first approach
- Touch-friendly navigation
- Optimized for various screen sizes
- Modern CSS with flexbox and grid layouts
