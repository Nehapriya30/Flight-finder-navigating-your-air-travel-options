# ✈️ Flight Finder - Navigating Your Air Travel Option

## 🧾 Full Stack Development with MERN
## 🎥 Demo Links

- [📽️ Project Video](https://drive.google.com/file/d/1pC1eQYezBeBYpmnp9M-4fjWzxmS1ZNfF/view?usp=drive_link)
- [📁 Project Folder](https://drive.google.com/drive/folders/1lhr3vbwaqIPwEwIfraJw-G0kh9aA9WY0?usp=sharing)

---

## 🧑‍🤝‍🧑 Team Details
**Team ID**: LTVIP2025TMID59024

### 👥 Team Members

1. **Yarlagadda Nehapriya (22481A05P9)**  
   *Role*: Full Stack Developer & Project Coordinator  
   *Responsibilities*: Planning, coordination, GitHub management, frontend-backend integration

2. **Yadala Pujitha (23481A12P4)**  
   *Role*: Frontend Developer  
   *Responsibilities*: React UI design, page routing, user interactions

3. **Y Devisri (24485A1226)**  
   *Role*: Backend Developer  
   *Responsibilities*: API development (Node.js & Express.js), authentication, server logic

4. **Yaddanapudi Murari (22481A12I7)**  
   *Role*: Database Administrator  
   *Responsibilities*: MongoDB schema design, CRUD operations, data consistency

---

## 📌 Project Overview

### 🎯 Purpose
To simplify flight booking by providing real-time availability, secure transactions, and a user-friendly search interface.

### 🌟 Key Features
- 🔍 Search and filter flights
- ✈️ Book tickets with user login
- 🧑‍💼 Admin panel for managing flights
- 📧 Email confirmations & booking history

---

## 🏗️ Architecture

### 💻 Frontend
- Built using **React.js**
- Components, hooks, React Router for navigation
- **Material-UI** for UI elements

### 🧠 Backend
- Developed using **Node.js** and **Express.js**
- RESTful APIs for all CRUD operations

### 🗃️ Database
- **MongoDB** stores user, flight, and booking data
- **Mongoose** for schema & validation

### 🧩 React Components
- `SearchForm.js`: Captures user input
- `FlightList.js`: Displays results
- **Redux** for state management

### 🔗 API Routes (Node.js / Express.js)
```javascript
app.get('/api/flights', flightController.search);
app.post('/api/bookings', authMiddleware, bookingController.create);
```

### 🔐 Middleware
- JWT validation
- Rate limiting

### 🧬 MongoDB Schema Sample
```javascript
const User = new Schema({
  email: { type: String, unique: true },
  bookings: [{ type: Schema.Types.ObjectId, ref: 'Booking' }]
});
```

---

## ⚙️ Setup Instructions

### ✅ Prerequisites
- Node.js ≥ 18
- MongoDB installed and running
- npm or yarn

### 🛠 Installation
```bash
git clone https://github.com/your-username/FlightFinder.git
cd FlightFinder
cd server && npm install
cd ../client && npm install
```

### 🌍 Environment Variables
Create `.env` in `/server`:
```
PORT=3000
MONGODB_URI=mongodb+srv://nehapriya:<db_password>@cluster0.mongodb.net/?retryWrites=true&w=majority
```

---

## 📁 Folder Structure

### Client
```
/client
 └── /src
     ├── /components
     ├── /pages
     ├── /api
     ├── App.js
     └── index.js
```

### Server
```
/server
 ├── /controllers
 ├── /routes
 ├── /models
 ├── server.js
 └── .env
```

---

## ▶️ Running the Application

### Frontend
```bash
cd client
npm start
```

### Backend
```bash
cd server
npm start
```

---

## 📡 API Documentation

### POST `/api/auth/register`
Registers a new user
```json
{ "name": "John", "email": "john@example.com", "password": "secret" }
```

### POST `/api/auth/login`
Logs in an existing user

### GET `/api/flights`
Retrieves available flights

### POST `/api/bookings`
Books a flight for the logged-in user

---

## 🔒 Authentication
- JWT (JSON Web Token) based
- Tokens stored in HTTP-only cookies
- Protected routes validate tokens

---

## 🖥️ User Interface Pages
- Home page with flight search
- Login and Register forms
- Admin dashboard
- Booking confirmation

---

## 🧪 Testing
- Manual API testing using **Postman**
- Unit testing with **Jest** and **React Testing Library**

---



## ⚠️ Known Issues
- No password recovery implemented yet
- UI responsiveness on tablets needs improvement

---

## 🔮 Future Enhancements
- Razorpay/Stripe integration for payments
- Role-based admin access
- Real-time flight tracking integration

