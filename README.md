# YathraGo

YathraGo is a  smart transport services platform built to connect passengers (parents/staff) with verified school and office transport services. The platform ensures safety, real-time tracking, and efficient communication between all stakeholders.

## 🚀 Key Features

- **Passenger App**:
  - Authentication & Account Management 
  - Multiple Profile Management (Multi-Child & Staff profiles)
  - Find school and staff transport services with advanced search 
  - Home Dashboard with live tracking map
  - Communication (Chat & Inform Driver) 
  - History & Records 
  - Payment Management 
  - Reviews & Ratings 
  - Push Notifications 
  - Support & Help (Complaints/Inquiries) 
  - Settings & Preferences 
  - Menu & Account management 
- **Driver App**:
  - Vehicle Registration & Documentation 
  - Home Dashboard (Go Online/Offline, Trip Management) 
  - Navigation & Routing (Step-by-step stop navigation) 
  - Route Setup (Daily route configuration) 
  - Student Management 
  - Attendance Tracking 
  - Ride Requests Management 
  - Vehicle List Management 
  - History & Records 
  - Earnings & Transactions 
  - Profile Management 
  - Notifications 
  - Communication (Chat and Broadcast messages) 
- **Web Dashboard**: Comprehensive portal for admins, transport managers, and vehicle owners.
- **Backend API**: NestJS-based RESTful API with PostgreSQL database 

## 🏗️ Project Architecture

This is a monorepo containing the full YathraGo ecosystem. The project is divided into four main modules:

| Module | Description | Technologies |
|---|---|---|
| [**`/backend`**](./backend) | Core API, business logic, and database management | NestJS, PostgreSQL, Prisma, TypeScript |
| [**`/mobile-customer`**](./mobile-customer) | Mobile application for passengers | React Native, Expo, NativeWind |
| [**`/mobile-driver`**](./mobile-driver) | Mobile application for drivers | React Native, Expo, NativeWind |
| [**`/web-dashboard`**](./web-dashboard) | Administrative web portal | Next.js, React, Tailwind CSS |

## ⚙️ Getting Started

To get started with any specific module, navigate to its respective directory and follow the instructions in its `README.md`.

```bash
# Clone the repository and navigate to the project folder
cd yathrago

# For backend development
cd backend
npm install && npm run start:dev

# For customer mobile app
cd mobile-customer
npm install && npm run dev

# For driver mobile app
cd mobile-driver
npm install && npm run dev

# For web dashboard
cd web-dashboard
npm install && npm run dev
```

## 🛠️ Tech Stack

- **Backend**: NestJS, Node.js, PostgreSQL, Prisma ORM
- **Mobile**: React Native, Expo, NativeWind (Tailwind)
- **Web Frontend**: Next.js, React.js, Tailwind CSS
- **Authentication**: JWT, Argon2

## 📄 License

This project is licensed under the MIT License.
