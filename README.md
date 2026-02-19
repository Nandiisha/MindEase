# MindEase 🧠  
A Full-Stack Real-Time Chat Application

MindEase is a modern full-stack chat platform built to deliver seamless real-time communication with secure authentication and a clean, responsive user interface. The application follows a decoupled client-server architecture and combines REST APIs with WebSocket-based real-time messaging.

---

# 🌐 System Overview

MindEase follows a full-stack architecture:

Frontend (React) → REST APIs → Backend (Node + Express) → MongoDB  
Frontend ↔ Socket.IO ↔ Backend (Real-Time Messaging)

It uses:
- HTTP APIs for authentication and data fetching  
- WebSockets for instant message delivery  
- Persistent database storage for chats and users  

---

# 🏗 Architecture Breakdown

## 1️⃣ Frontend (Client)

**Built With**
- React
- Tailwind CSS (or your styling framework)

**Responsibilities**
- User authentication UI
- Chat interface rendering
- Managing local application state
- Establishing WebSocket connection
- Sending and receiving real-time messages
- Responsive layout for mobile and desktop

**Core Concepts**
- Component-based architecture
- State-driven UI updates
- Form handling
- Socket lifecycle management

---

## 2️⃣ Backend (Server)

**Built With**
- Node.js
- Express.js
- Socket.IO
- MongoDB + Mongoose
- JWT Authentication
- bcrypt for password hashing

**Responsibilities**
- User registration and login
- Token-based authentication
- Protected API routes
- Message storage and retrieval
- Real-time socket communication
- Data validation and security enforcement

---

# 🔐 Authentication Flow

1. User registers  
2. Password is hashed using bcrypt  
3. JWT token is generated  
4. Token sent to frontend  
5. Protected routes validate JWT before granting access  

Security features:
- Password hashing
- JWT expiration
- Server-side validation
- CORS configuration

---

# 💬 Real-Time Messaging Flow

1. User logs in  
2. Frontend establishes WebSocket connection  
3. User selects chat  
4. Message sent via Socket.IO  
5. Backend:
   - Saves message to database  
   - Emits message to recipient  
6. Recipient UI updates instantly  

This ensures:
- Instant message delivery  
- Persistent chat history  
- Seamless user experience  

---

# 🗄 Database Design

## User Schema
- name  
- email  
- password (hashed)  
- profile picture (optional)  
- timestamps  

## Message Schema
- senderId  
- receiverId  
- message text  
- timestamps  

This structure supports scalable message storage and conversation tracking.

---

# 📁 Folder Structure

```
MindEase/
│
├── client/
│   ├── components/
│   ├── pages/
│   ├── hooks/
│   └── utils/
│
├── server/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   └── socket/
│
└── README.md
```

---

# ⚙️ Environment Variables

## server/.env

```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
CLIENT_URL=http://localhost:3000
```

If using media storage:

```
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=
```

---

# 🚀 Local Setup Guide

## 1. Clone Repository

```
git clone https://github.com/Nandiisha/MindEase.git
cd MindEase
```

## 2. Install Dependencies

### Backend
```
cd server
npm install
```

### Frontend
```
cd ../client
npm install
```

## 3. Run Application

### Start Backend
```
npm run dev
```

### Start Frontend
```
npm start
```

Application runs at:
- Frontend: http://localhost:3000  
- Backend: http://localhost:5000  

---

# 🧠 Key Design Decisions

- Decoupled frontend and backend for scalability  
- JWT-based authentication for stateless security  
- Socket.IO for real-time communication  
- MongoDB for flexible document-based storage  

---

# 🔮 Future Improvements

- Group chat functionality  
- Typing indicators  
- Read receipts  
- Message search  
- Media sharing  
- Redis for socket scaling  
- Production-level monitoring  

---

# 🛡 Security Practices

- Password hashing with bcrypt  
- Token expiration and validation  
- Protected routes  
- Environment variable protection  
- Server-side validation  

---

# 🎯 What This Project Demonstrates

- Full-stack development skills  
- REST + WebSocket integration  
- Authentication system design  
- Real-time system architecture  
- Database modeling  
- Scalable backend structure  

---

# 👩‍💻 Author

**Isha Nandi**  
GitHub: https://github.com/Nandiisha
