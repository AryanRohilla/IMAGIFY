# Imagify
Imagify is a full-stack web application that leverages AI to generate stunning images from text prompts. Users can register, log in, generate images, and purchase credits to unlock more generations. The project is built with React (client) and Express/MongoDB (server), and integrates Razorpay for payments.

## Features

- **Text-to-Image Generation:** Instantly turn your imagination into visuals using AI.
- **User Authentication:** Secure registration and login with JWT.
- **Credit System:** Each user has a credit balance; generating images consumes credits.
- **Purchase Credits:** Buy more credits via Razorpay integration.
- **Responsive UI:** Modern, mobile-friendly design with Tailwind CSS.
- **Testimonials & Steps:** Informative sections to guide and inspire users.

## Technologies Used

- **Frontend:** React, Tailwind CSS, Framer Motion, React Router, React Toastify
- **Backend:** Express.js, MongoDB, Mongoose, JWT, Razorpay, Axios, Bcrypt
- **Deployment:** Vite (client), Node.js (server)

## Getting Started

### Prerequisites

- Node.js & npm
- MongoDB Atlas account
- Razorpay account (for payment integration)

### Installation

#### 1. Clone the repository

```sh
git clone https://github.com/yourusername/imagify.git
cd imagify
```

#### 2. Setup Server

```sh
cd server
npm install
```

- Configure environment variables in `.env` (see `server/.env` for example).

#### 3. Setup Client

```sh
cd ../client
npm install
```

- Configure environment variables in `.env` (see `client/.env` for example).

### Running the Project

#### Start the Server

```sh
npm run server
```

#### Start the Client

```sh
npm run dev
```

## Folder Structure

```
IMAGIFY/
│
├── client/                # Frontend React application
│   ├── public/            # Static assets (favicon, images, etc.)
│   ├── src/
│   │   ├── assets/        # Image and SVG assets
│   │   ├── components/    # Reusable React components
│   │   ├── context/       # React context providers
│   │   ├── pages/         # Page-level React components
│   │   ├── styles/        # CSS or Tailwind config files
│   │   ├── utils/         # Utility/helper functions
│   │   ├── App.jsx        # Main App component
│   │   ├── main.jsx       # Entry point for React
│   │   └── index.css      # Global styles
│   ├── .env               # Environment variables
│   ├── package.json       # Frontend dependencies
│   └── ...                # Other config files
│
├── server/                # Backend Express application
│   ├── config/            # Database and external service configs
│   ├── controllers/       # Route handler logic
│   ├── middlewares/       # Express middlewares (auth, error handling)
│   ├── models/            # Mongoose models (User, Transaction)
│   ├── routes/            # API route definitions
│   ├── utils/             # Utility/helper functions
│   ├── .env               # Environment variables
│   ├── server.js          # Entry point for Express server
│   ├── package.json       # Backend dependencies
│   └── ...                # Other config files
│
├── README.md              # Project documentation
└── LICENSE                # License file
```

## API Endpoints

- `POST /api/user/register` – Register a new user
- `POST /api/user/login` – Login
- `GET /api/user/credits` – Get user credits
- `POST /api/user/pay-razor` – Initiate payment
- `POST /api/user/verify-razor` – Verify payment
- `POST /api/image/generate-image` – Generate image (requires credits)

## License

This project is licensed under the ISC License.

--

**Imagify** – Unleash your creativity with AI-powered image generation!