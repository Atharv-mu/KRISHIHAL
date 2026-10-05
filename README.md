# 🌾 Farmer–Buyer Platform

A web-based platform designed to connect **farmers and buyers** through a simple, accessible, and scalable digital interface.

The project currently focuses on delivering a **Frontend MVP** that demonstrates the complete user journey and core interface. The backend, database, authentication, and production full-stack integration are planned as the next implementation phase.

---

## 🚀 Current Status

> **Frontend MVP is ready and deployed.**
> Backend, database, authentication, and full-stack deployment are planned for the next implementation phase.

The current version is focused on demonstrating:

* Farmer and buyer user journeys
* Responsive web interface
* Core navigation and UI flows
* Product/farm-related interactions
* Clean and accessible user experience

---

## 🛠️ Technical Stack

### Frontend — Prototype Ready

* **HTML5**
* **Tailwind CSS**
* **JavaScript**
* **Lucide Icons**

The frontend is currently implemented and serves as the working MVP for demonstrating the platform's user experience.

### Backend — Proposed

* **Node.js**
* **Express.js**
* **REST APIs**

The backend architecture is planned to handle business logic, API communication, user management, and data processing.

### Database — Proposed

* **PostgreSQL**

PostgreSQL is planned as the primary relational database for storing users, farmer/buyer profiles, products, transactions, and other application data.

### Authentication — Proposed

* **Mobile OTP Authentication**
* **Role-Based Authentication**
* **Farmer Verification**
* **Buyer Verification**

Authentication and verification workflows will be integrated during the backend implementation phase.

### Deployment — Target

* **Render**
* Full-stack deployment

The target deployment architecture is intended to host the frontend/backend application and supporting services through a production-ready setup.

---

## 🏗️ Proposed Architecture

```text
┌───────────────────┐
│   Farmer / Buyer  │
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
│   Node.js +       │
│    Express.js     │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│    PostgreSQL     │
│     Database      │
└───────────────────┘
```

### Architecture Flow

**Farmer / Buyer → Web Frontend → REST API → Node.js + Express → PostgreSQL**

This architecture is designed to keep the frontend, business logic, API layer, and database logically separated, making the application easier to scale and maintain.

---

## 📂 Project Structure

The current frontend MVP can be organized as:

```text
project/
│
├── index.html
├── assets/
│   ├── images/
│   └── icons/
│
├── css/
│   └── styles.css
│
├── js/
│   └── script.js
│
└── README.md
```

> The backend structure will be added during the next implementation phase.

A proposed backend structure is:

```text
backend/
│
├── src/
│   ├── controllers/
│   ├── routes/
│   ├── models/
│   ├── middleware/
│   ├── services/
│   └── config/
│
├── server.js
├── package.json
└── .env
```

---

## 🎯 Key User Roles

### 👨‍🌾 Farmer

The platform is intended to allow farmers to:

* Create and manage their profile
* Verify their identity
* List agricultural products
* Provide product information
* Connect with potential buyers

### 🛒 Buyer

The platform is intended to allow buyers to:

* Create and verify their profile
* Explore available products
* View farmer/product information
* Connect with farmers
* Participate in the future transaction workflow

---

## 🔐 Authentication & Verification

The planned authentication system will use:

```text
Mobile Number
      ↓
    OTP
      ↓
Authentication
      ↓
Role Selection
      ↓
Farmer / Buyer Verification
```

Role-based access control will ensure that farmers and buyers receive appropriate functionality based on their roles.

> **Note:** These authentication features are part of the proposed backend implementation and are not claimed as completed functionality in the current frontend MVP.

---

## 🗄️ Proposed Database

PostgreSQL will be used as the planned database solution.

A possible database model could include:

```text
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

The exact schema will be finalized during backend development.

---

## 🔌 Proposed REST API

The planned backend may expose REST APIs such as:

| Method   | Endpoint               | Purpose             |
| -------- | ---------------------- | ------------------- |
| `POST`   | `/api/auth/send-otp`   | Send OTP            |
| `POST`   | `/api/auth/verify-otp` | Verify OTP          |
| `POST`   | `/api/auth/register`   | Register user       |
| `GET`    | `/api/farmers`         | Get farmer profiles |
| `GET`    | `/api/products`        | Get products        |
| `POST`   | `/api/products`        | Create product      |
| `PUT`    | `/api/products/:id`    | Update product      |
| `DELETE` | `/api/products/:id`    | Delete product      |

> These endpoints represent the **proposed API design** and should not be interpreted as currently implemented APIs.

---

## 🌐 Deployment

### Current

The **Frontend MVP is deployed** for demonstration purposes.

### Target

The planned full-stack deployment architecture is:

```text
Frontend
   │
   ▼
Web Application
   │
   ▼
Node.js + Express API
   │
   ▼
PostgreSQL Database
```

**Target Platform:** Render

---

## 📊 Implementation Roadmap

### Phase 1 — Frontend MVP ✅

* [x] User interface
* [x] Responsive frontend
* [x] Farmer journey
* [x] Buyer journey
* [x] Core navigation
* [x] Frontend deployment

### Phase 2 — Backend 🔄

* [ ] Node.js setup
* [ ] Express.js API
* [ ] REST API integration
* [ ] Business logic
* [ ] API validation

### Phase 3 — Database 🔄

* [ ] PostgreSQL setup
* [ ] Database schema
* [ ] User data
* [ ] Farmer profiles
* [ ] Buyer profiles
* [ ] Product data

### Phase 4 — Authentication 🔄

* [ ] Mobile OTP
* [ ] Role-based authentication
* [ ] Farmer verification
* [ ] Buyer verification
* [ ] Protected API routes

### Phase 5 — Full-Stack Deployment 🔄

* [ ] Frontend + backend integration
* [ ] PostgreSQL production setup
* [ ] Environment configuration
* [ ] Render deployment
* [ ] Production testing

---

## 📌 Current vs Proposed

| Component                    | Status        |
| ---------------------------- | ------------- |
| Frontend                     | ✅ Implemented |
| Frontend MVP                 | ✅ Ready       |
| Frontend Deployment          | ✅ Deployed    |
| Node.js Backend              | 🔄 Proposed   |
| Express.js REST APIs         | 🔄 Proposed   |
| PostgreSQL                   | 🔄 Proposed   |
| Mobile OTP                   | 🔄 Proposed   |
| Role-Based Authentication    | 🔄 Proposed   |
| Farmer/Buyer Verification    | 🔄 Proposed   |
| Full-Stack Render Deployment | 🔄 Target     |

This distinction is intentional to maintain **technical transparency** and avoid representing planned functionality as already implemented.

---

## 🧑‍⚖️ For Project Demonstration / Evaluation

### If asked: "Backend kaha hai?"

A clear and honest response is:

> **"Currently, we have developed the complete frontend MVP for demonstrating the user journey. The backend architecture is designed using Node.js and Express with PostgreSQL, and it will be integrated in the next implementation phase."**

### If asked: "Database implemented hai?"

You can say:

> **"PostgreSQL is our proposed database layer. The current MVP focuses on the frontend experience, while database integration is planned for the next phase."**

### If asked: "Authentication kaise hoga?"

You can say:

> **"The planned authentication system uses mobile OTP with role-based authentication for farmers and buyers, along with verification workflows."**

---

## 💡 Why This Architecture?

The proposed architecture provides:

* **Scalability** through a dedicated backend API
* **Maintainability** through separation of frontend and backend
* **Data consistency** using PostgreSQL
* **Security** through authentication and role-based access
* **Flexibility** for future mobile or third-party clients
* **Easy deployment** through a cloud-based full-stack setup

---

## 🏁 Conclusion

This project currently delivers a **working Frontend MVP** that demonstrates the intended farmer-buyer experience.

The next implementation phase will transform the prototype into a complete full-stack application by integrating:

**Node.js + Express.js + REST APIs + PostgreSQL + OTP Authentication + Role-Based Access Control**

The architecture is intentionally documented as **proposed** where implementation is not yet complete, ensuring that the project presentation remains both **professional and technically honest**.

---

## 📄 Project Status

**Current Stage:** Frontend MVP
**Backend:** Proposed
**Database:** Proposed
**Authentication:** Proposed
**Full-Stack Deployment:** Target
**Primary Goal:** Build a scalable digital platform connecting farmers and buyers
