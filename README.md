# Proshop
# ProShop v2

ProShop v2 is a full-stack MERN ecommerce application. It includes product browsing, cart management, user authentication, checkout, PayPal payment integration, product reviews, and admin management.

This version has been updated to show product prices in Indian Rupees and use INR for PayPal checkout.

## Features

- Product listing with pagination
- Product search
- Product details page
- Shopping cart
- User login and registration
- User profile with order history
- Checkout flow with shipping and payment steps
- PayPal payment integration
- Product reviews and ratings
- Admin product management
- Admin user management
- Admin order management
- Product image upload
- MongoDB database seeder

## Tech Stack

- React
- Redux Toolkit
- RTK Query
- React Router
- React Bootstrap
- Node.js
- Express
- MongoDB
- Mongoose
- JWT authentication
- PayPal SDK

## Project Structure

```txt
backend/
  config/
  controllers/
  data/
  middleware/
  models/
  routes/
  utils/
  server.js

frontend/
  public/
  src/
    components/
    screens/
    slices/
    utils/
```

## Environment Variables

Create a `.env` file in the root folder and add:

```env
NODE_ENV=development
PORT=5001
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
PAYPAL_CLIENT_ID=your_paypal_client_id
PAYPAL_APP_SECRET=your_paypal_secret
PAYPAL_API_URL=https://api-m.sandbox.paypal.com
PAGINATION_LIMIT=8
```

Do not commit the `.env` file. It contains private credentials.

## Install Dependencies

Install backend dependencies:

```bash
npm install
```

Install frontend dependencies:

```bash
cd frontend
npm install
cd ..
```

## Seed Database

Import sample users and products:

```bash
npm run data:import
```

Destroy sample data:

```bash
npm run data:destroy
```

## Run Project

Run the frontend and backend together:

```bash
npm run dev
```

Backend API:

```txt
http://localhost:5001
```

Frontend:

```txt
http://localhost:3000
```

If port `3000` is already busy, React may ask to run on another port.

## Sample Login

Admin user:

```txt
admin@email.com
123456
```

Customer users:

```txt
john@email.com
123456
```

```txt
jane@email.com
123456
```

## Currency

Prices are displayed in Indian Rupees:

```txt
₹
```

PayPal checkout is configured to use:

```txt
INR
```

Currency settings are defined in:

```txt
frontend/src/constants.js
```

## Build Frontend

Create a production build:

```bash
npm run build --prefix frontend
```

## Notes

- Make sure MongoDB is running before starting the backend.
- PayPal checkout requires valid PayPal sandbox credentials.
- The `.env` file is ignored by git and should not be pushed.
- The backend port is set to `5001` to avoid conflicts with services that may use port `5000`.

## License

This project is based on the ProShop MERN ecommerce application and is intended for learning and portfolio use.
