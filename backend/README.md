# YathraGo Backend

<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

## Description

YathraGo is a comprehensive transport management system backend built with modern web technologies. This backend API serves the YathraGo mobile and web applications, providing secure authentication, real-time communication, and robust data management for transport operations.

## Technologies Used

### Core Framework
- **NestJS** - A progressive Node.js framework for building efficient and scalable server-side applications
- **TypeScript** - Strongly typed programming language that builds on JavaScript
- **Node.js** - JavaScript runtime environment

### Database & ORM
- **PostgreSQL** - Advanced open-source relational database
- **Prisma ORM** - Next-generation ORM for Node.js and TypeScript

### Authentication & Security
- **JWT (JSON Web Tokens)** - Secure token-based authentication
- **Passport.js** - Authentication middleware for Node.js
- **Argon2** - Secure password hashing algorithm

### Communication & Notifications
- **Android SMS Gateway** - SMS sending service integration

### File Handling & HTTP
- **Multer** - Node.js middleware for handling multipart/form-data (file uploads)
- **Axios** - Promise-based HTTP client for making API requests

## Architecture Features

### Modular Structure
- **User Management** - Customer, driver, and owner authentication
- **Vehicle Management** - Vehicle registration and tracking
- **Authentication Module** - Secure login and registration
- **Prisma Module** - Database connection and operations
- **Common Module** - Shared utilities and middleware

### Security Features
- JWT-based authentication
- Role-based access control
- Input validation and sanitization
- Secure password storage with Argon2
- OTP-based phone verification

### Database Design
- Relational database structure with PostgreSQL
- Type-safe queries with Prisma
- Automated migrations
- Data integrity constraints

## Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- PostgreSQL database
- [SMSGate](https://sms-gate.app) mobile app (for SMS functionality)

## Environment Setup

Create a `.env` file in the root directory with the following variables:

```env
# Database
DATABASE_URL="postgresql://username:password@localhost:5432/yathrago"
DIRECT_URL="postgresql://username:password@localhost:5432/yathrago"

# JWT
JWT_SECRET="your-jwt-secret-key"
JWT_EXPIRES_IN="7d"

# SMS Configuration
SMS_PROVIDER="dummy"  # Options: "dummy", "smsgate"

# SMS-Gate Configuration (only needed if SMS_PROVIDER=smsgate)
# Get these credentials from your SMS-Gate app's Home screen
SMSGATE_USERNAME="sms"
SMSGATE_PASSWORD="password"
SMSGATE_BASE_URL="http://YOUR_PHONE_IP:8080"
SMSGATE_SIM_NUMBER=1  # Optional: 1 or 2 for dual SIM devices (leave empty to use default SIM)

# Other configurations
PORT=3000
```

## Project Setup

### 1. Install Dependencies

```bash
npm install
```

### 2. Database Setup

```bash
# Generate Prisma client
npx prisma generate

# Run database migrations
npx prisma migrate dev

# (Optional) Seed the database
npx prisma db seed
```

### 3. Start the Application

```bash
# Development mode
npm run start:dev

# Production mode
npm run start:prod

# Debug mode
npm run start:debug
```

## API Documentation

Once the server is running, you can access the Swagger API documentation at:
```
http://localhost:3000/api
```

## Database Management

### Prisma Commands

```bash
# View database in Prisma Studio
npx prisma studio

# Reset database
npx prisma migrate reset

# Deploy migrations to production
npx prisma migrate deploy

# Pull schema from existing database
npx prisma db pull

# Push schema changes without migrations
npx prisma db push
```

## Project Structure

```
src/
├── auth/              # Authentication module
├── common/            # Shared utilities and middleware
├── customer/          # Customer-specific operations
├── driver/            # Driver-specific operations
├── owner/             # Vehicle owner operations
├── prisma/            # Prisma service and configuration
├── user/              # User management
├── vehicle/           # Vehicle management
├── app.controller.ts  # Main app controller
├── app.module.ts      # Root module
├── app.service.ts     # Main app service
└── main.ts            # Application entry point
```

## License

This project is part of the YathraGo ecosystem.