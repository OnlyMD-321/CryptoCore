# Crypto Portfolio Management System

This monorepo contains both the backend (in [CryptoAPI](CryptoAPI/)) and the frontend (in [Crypto-API-UI](Crypto-API-UI/)) for a cryptocurrency portfolio management system. The backend provides RESTful APIs for user authentication, email verification, and portfolio management; the frontend provides a React-based interface for interacting with the API.

## Features

1. User Authentication  
   - Signup, email verification, login, JWT-based session management  
2. Portfolio Management  
   - Create, read, update, and delete portfolios  
   - Add cryptocurrencies to portfolios  
   - View detailed cryptocurrency data  
3. Real-Time Crypto Data  
   - Integrates with third-party data services like CoinMarketCap  
4. MIT Licensed

## Project Structure

• [CryptoAPI](CryptoAPI/) (Backend)  
  - [src/app.js](CryptoAPI/src/app.js): Express server entry point  
  - [src/controllers](CryptoAPI/src/controllers/): Request handlers for authentication, crypto, and portfolios  
  - [src/services](CryptoAPI/src/services/): Business logic for authentication and portfolio management  
  - [src/routes](CryptoAPI/src/routes/): Express routes definitions  
  - [src/utils](CryptoAPI/src/utils/): Utility scripts (database tables creation, mailing, cron jobs)  

• [Crypto-API-UI](Crypto-API-UI/) (Frontend)  
  - [src/main.jsx](Crypto-API-UI/src/main.jsx): Frontend entry point (React + Vite)  
  - [src/App.jsx](Crypto-API-UI/src/App.jsx): Main application component with React Router  
  - [src/views/](Crypto-API-UI/src/views/): Pages for login, signup, dashboard, portfolio management  
  - [src/context/](Crypto-API-UI/src/context/): React Context for Auth and Portfolio states  
  - [src/components/](Crypto-API-UI/src/components/): Reusable React components  

## Installation & Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/CryptoProject.git
   cd CryptoProject
   ```

2. Install dependencies for both backend and frontend:
   ```bash
   # Install backend dependencies

    cd CryptoAPI
    npm install

    # Go to the frontend folder and install its dependencies

    cd ../Crypto-API-UI
    npm install
   ```

3. Configure environment variables for the backend in .env.
Example:
   - Create a `.env` file in the root directory with your database credentials:
     ```
     PORT=5000
    JWT_SECRET=your-secret-key
    DATABASE_URL=postgresql://user:password@localhost:5432/db
     ```

4. Start the backend:
   ```bash
   cd ../CryptoAPI

    npm start

    # Server at <http://localhost:5000>

   ```

5. Start the backend server:
   ```bash
   cd ../Crypto-API-UI

    npm run dev

    # Local dev server at <http://localhost:5173> (by default)

   ```

## Usage

Open the frontend URL in your browser (typically [http://localhost:5173](http://localhost:5173)).  
Create an account using the "Signup" page and verify your email.  
Log in to access the portfolio dashboard, create portfolios, and add cryptocurrencies.

## API Endpoints (Backend)

See [README.md](./CryptoAPI/README.md) for full documentation:

- **POST** `/auth/signup`
- **POST** `/auth/verify`
- **POST** `/auth/login`
- **GET** `/portfolios`
- **POST** `/portfolios`
- **GET** `/cryptos`

…and more.

## License

This project is covered by the MIT License. Feel free to fork and contribute!