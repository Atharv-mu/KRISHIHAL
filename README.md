# Krishihal | A Digital Platform for Fair Farm Prices

> Connecting farmers directly with buyers, so prices reflect real market demand.

<p align="center">
  <a href="https://krishihal.netlify.app/"><img src="https://img.shields.io/badge/Live_Demo-Visit_Site-2e7d32?style=for-the-badge&logo=netlify&logoColor=white" alt="Live demo"></a>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
</p>

**Live demo:** [krishihal.netlify.app](https://krishihal.netlify.app/)

Krishihal is a web platform that aims to give farmers a fair price for their produce by connecting them directly with buyers through a simple, accessible and scalable interface.

The project is currently a **Frontend MVP** that demonstrates the complete user journey and core interface. The backend, database, authentication and full-stack deployment are planned for the next phase.

---

## Contents

- [Current status](#current-status)
- [Tech stack](#tech-stack)
- [Proposed architecture](#proposed-architecture)
- [Project structure](#project-structure)
- [User roles](#user-roles)
- [Authentication and verification](#authentication-and-verification)
- [Proposed database](#proposed-database)
- [Proposed REST API](#proposed-rest-api)
- [Deployment](#deployment)
- [Roadmap](#roadmap)
- [Implemented vs proposed](#implemented-vs-proposed)

---

## Current status

> **The Frontend MVP is built and deployed.** The backend, database, authentication and full-stack deployment are planned.

The current version demonstrates:

- Farmer and buyer user journeys
- A responsive web interface
- Core navigation and UI flows
- Product and farm-related interactions
- A clean, accessible user experience

---

## Tech stack

**Frontend (implemented):** HTML5, Tailwind CSS, JavaScript and Lucide Icons. This is the working MVP that demonstrates the platform's user experience.

**Backend (proposed):** Node.js, Express.js and REST APIs, to handle business logic, API communication, user management and data processing.

**Database (proposed):** PostgreSQL, as the main relational database for users, farmer and buyer profiles, products, transactions and other application data.

**Authentication (proposed):** mobile OTP login, role-based access, and farmer and buyer verification. These will be built alongside the backend.

**Deployment:** the frontend MVP is currently hosted on Netlify and GitHub. The target is a full-stack deployment on Render, hosting the frontend, backend and supporting services.

---

## Proposed architecture

```
┌───────────────────┐
│  Farmer / Buyer   │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│   Web Frontend    │
│ HTML + Tailwind   │
│    + JavaScript   │
└─────────┬─────────┘
          │
          │ REST API
          ▼
┌───────────────────┐
│    Node.js +      │
│    Express.js     │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│    PostgreSQL     │
│     Database      │
└───────────────────┘
```

The frontend, business logic, API layer and database are deliberately kept separate, which makes the application easier to scale and maintain.

---

## Project structure

The current frontend MVP is organised like this:

```
project/
├── index.html
├── assets/
│   ├── images/
│   └── icons/
├── css/
│   └── styles.css
├── js/
│   └── script.js
└── README.md
```

The backend will be added in the next phase. A proposed layout:

```
backend/
├── src/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   ├── services/
│   └── config/
├── server.js
├── package.json
└── .env
```

---

## User roles

### Farmer

Farmers will be able to:

- Create and manage their profile
- Verify their identity
- List agricultural products
- Provide product information
- Connect with potential buyers

### Buyer

Buyers will be able to:

- Create and verify their profile
- Explore available products
- View farmer and product information
- Connect with farmers
- Take part in the future transaction workflow

---

## Authentication and verification

The planned sign-in flow is:

```
Mobile number → OTP → Authentication → Role selection → Farmer / Buyer verification
```

Role-based access control will make sure farmers and buyers only see the features that belong to their role.

> These features belong to the planned backend phase and are not part of the current frontend MVP.

---

## Proposed database

PostgreSQL is the planned database. A possible model:

```
Users
 ├── user_id
 ├── name
 ├── mobile
 ├── role
 └── verification_status

Farmer Profiles
 ├── farmer_id
 ├── user_id
 ├── location
 └── farm_details

Buyer Profiles
 ├── buyer_id
 ├── user_id
 └── business_details

Products
 ├── product_id
 ├── farmer_id
 ├── name
 ├── category
 ├── quantity
 └── price
```

The final schema will be settled during backend development.

---

## Proposed REST API

| Method   | Endpoint               | Purpose             |
| -------- | ---------------------- | ------------------- |
| `POST`   | `/api/auth/send-otp`   | Send OTP            |
| `POST`   | `/api/auth/verify-otp` | Verify OTP          |
| `POST`   | `/api/auth/register`   | Register a user     |
| `GET`    | `/api/farmers`         | Get farmer profiles |
| `GET`    | `/api/products`        | Get products        |
| `POST`   | `/api/products`        | Create a product    |
| `PUT`    | `/api/products/:id`    | Update a product    |
| `DELETE` | `/api/products/:id`    | Delete a product    |

> These endpoints are a **proposed design**. None of them are implemented yet.

---

## Deployment

**Now:** the Frontend MVP is deployed for demonstration at [krishihal.netlify.app](https://krishihal.netlify.app/).

**Target:** a full-stack deployment on Render, with the web application, the Node.js and Express API and the PostgreSQL database all running together.

---

## Roadmap

**Phase 1: Frontend MVP (complete)**

- [x] User interface
- [x] Responsive frontend
- [x] Farmer journey
- [x] Buyer journey
- [x] Core navigation
- [x] Frontend deployment

**Phase 2: Backend**

- [ ] Node.js setup
- [ ] Express.js API
- [ ] REST API integration
- [ ] Business logic
- [ ] API validation

**Phase 3: Database**

- [ ] PostgreSQL setup
- [ ] Database schema
- [ ] User data
- [ ] Farmer profiles
- [ ] Buyer profiles
- [ ] Product data

**Phase 4: Authentication**

- [ ] Mobile OTP
- [ ] Role-based authentication
- [ ] Farmer verification
- [ ] Buyer verification
- [ ] Protected API routes

**Phase 5: Full-stack deployment**

- [ ] Frontend and backend integration
- [ ] PostgreSQL production setup
- [ ] Environment configuration
- [ ] Render deployment
- [ ] Production testing

---

## Implemented vs proposed

I've kept this distinction on purpose, so planned work is never presented as finished.

| Component                    | Status      |
| ---------------------------- | ----------- |
| Frontend                     | Implemented |
| Frontend MVP                 | Ready       |
| Frontend deployment          | Deployed    |
| Node.js backend              | Proposed    |
| Express.js REST APIs         | Proposed    |
| PostgreSQL                   | Proposed    |
| Mobile OTP                   | Proposed    |
| Role-based authentication    | Proposed    |
| Farmer and buyer verification | Proposed   |
| Full-stack Render deployment | Target      |

---

## Summary

Krishihal currently delivers a working Frontend MVP that shows the intended farmer-to-buyer experience. The next phase will turn it into a full-stack application using Node.js, Express.js, REST APIs, PostgreSQL, OTP authentication and role-based access control.

**Primary goal:** build a scalable digital platform that connects farmers and buyers and helps farmers earn fairer prices.
