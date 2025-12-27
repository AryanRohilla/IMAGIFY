# Imagify - AI Image Generation Platform

Imagify is a full-stack AI-powered image generation platform built with modern web technologies. It allows users to generate high-quality images from text prompts using advanced AI models, manage credits, and purchase additional credits for continued access.

## Technologies Used

### Frontend (client/)
- **React**: UI library for building interactive user interfaces.
- **Vite**: Fast development server and build tool.
- **Tailwind CSS**: Utility-first CSS framework for styling.
- **Axios**: HTTP client for API requests.
- **React Router**: Routing for SPA navigation.
- **React Toastify**: Toast notifications.
- **Framer Motion**: Animation library.

### Backend (server/)
- **Node.js**: JavaScript runtime.
- **Express**: Web framework for building REST APIs.
- **MongoDB**: NoSQL database for storing user and transaction data.
- **Mongoose**: ODM for MongoDB.
- **JWT**: JSON Web Tokens for authentication.
- **Bcrypt**: Password hashing.
- **Razorpay**: Payment gateway for credit purchases.
- **Clipdrop API**: AI image generation service.

## Project Structure

```
client/
  ├── src/
  │   ├── components/      # Reusable UI components (Header, Footer, etc.)
  │   ├── pages/           # Route pages (Home, Result, BuyCredit)
  │   ├── assets/          # Images and icons
  │   ├── context/         # App context for state management
  │   └── main.jsx         # Entry point
  ├── public/              # Static files
  ├── index.html           # Main HTML file
  └── vite.config.js       # Vite configuration

server/
  ├── controllers/         # Route controllers (imageController, userController)
  ├── models/              # Mongoose schemas (userModel, transactionModel)
  ├── routes/              # Express routers
  ├── config/              # MongoDB configuration
  ├── middlewares/         # Auth middleware
  ├── server.js            # Entry point
  └── package.json         # Dependencies
```

## Features

- User registration and login with JWT authentication
- Generate images from text prompts using Clipdrop AI
- Credit-based system for image generation
- Purchase credits via Razorpay integration
- View generated images and manage credit balance
- Responsive design with Tailwind CSS
- Toast notifications for user feedback

## Getting Started

1. **Install dependencies**  
   - `cd client && npm install`
   - `cd server && npm install`

2. **Configure environment variables**  
   - Set up `.env` files in both `client/` and `server/` folders with necessary API keys (MongoDB URI, JWT secret, Clipdrop API key, Razorpay keys).

3. **Run the development servers**  
   - Client: `npm run dev`  
   - Server: `npm run server`