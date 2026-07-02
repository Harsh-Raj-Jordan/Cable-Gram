# Cable-Gram 💬

*A modern, real-time full-stack chat application built for scalable, instant communication.*

---

## 🌟 Project Overview (STAR Method)

This project was developed with a focus on solving real-world communication challenges, demonstrating production-ready development practices, and serving as a robust portfolio piece for software engineering placements.

### **Situation (The Problem)**
In today's fast-paced digital world, delayed communication causes friction in collaboration and connectivity. Traditional HTTP-based polling mechanisms for chat applications are inefficient, resource-heavy, and lack the true "instant" feel required by modern users. There was a need for a seamless, low-latency, and secure real-time messaging platform that also supports rich media sharing.

### **Task (The Objective)**
The goal was to architect and develop **Cable-Gram**, a full-stack real-time chat application from scratch. The application needed to support instantaneous bidirectional messaging, secure user authentication, optimized media (image) uploads, global state management, and a highly responsive, modern user interface. 

### **Action (The Implementation)**
To achieve a highly performant and scalable solution, I took the following actions:
- **Real-Time Engine:** Implemented bidirectional, event-driven communication using **Socket.io** to ensure messages are delivered instantly without page reloads or constant server polling.
- **Backend Architecture:** Built a robust RESTful API using **Node.js** and **Express**, connected to a **MongoDB** database (via Mongoose) for efficient data modeling and retrieval.
- **Security & Authentication:** Secured user data by implementing JWT (JSON Web Tokens) for stateless authentication and **bcryptjs** for secure password hashing. Integrated **Arcjet** for rate-limiting and enhanced endpoint security.
- **Media Management:** Integrated **Cloudinary** to handle image uploads, ensuring media is stored reliably and delivered via a global CDN, taking the load off the main server.
- **Frontend Experience:** Developed a highly responsive and dynamic Single Page Application (SPA) using **React 19** and **Vite**. Styled the application using **Tailwind CSS** and **DaisyUI** for a premium, accessible user interface.
- **State Management:** Leveraged **Zustand** to efficiently manage complex global states (like active chat threads, online user status, and authentication state) without the boilerplate of Redux.

### **Result (The Impact)**
The result is a fully functional, highly optimized chat application capable of handling concurrent users with minimal latency. 
- **For the User:** Provides a fluid, instant, and visually appealing chatting experience with secure media sharing.
- **For the Developer (Me):** Gained profound hands-on experience in full-stack architecture, WebSocket integration, modern React state management, and robust security practices. This project clearly demonstrates my ability to tackle complex, real-world engineering problems—making it a strong testament to my readiness for software engineering roles.

---

## 🛠️ Tech Stack

**Frontend:**
- React (v19) + Vite
- Tailwind CSS & DaisyUI (Styling)
- Zustand (State Management)
- Axios (HTTP Client)
- Socket.io-client
- React Router (Navigation)
- Lucide React (Icons)

**Backend:**
- Node.js & Express.js
- MongoDB & Mongoose
- Socket.io (WebSockets)
- JWT & bcryptjs (Auth & Security)
- Cloudinary (Media Storage)
- Resend (Email Services)
- Arcjet (Security/Rate Limiting)

---

## 🚀 How to Run the Project Locally

Follow these steps to get the project up and running on your local machine:

### 1. Prerequisites
- [Node.js](https://nodejs.org/) (v20.0.0 or higher recommended)
- [MongoDB](https://www.mongodb.com/) (Local or Atlas URI)
- [Cloudinary Account](https://cloudinary.com/) (For image uploads)

### 2. Clone the Repository
```bash
git clone <your-repo-url>
cd Cable-Gram
```

### 3. Install Dependencies
Install dependencies for both the frontend and backend concurrently from the root directory:
```bash
npm run build
```
*(Alternatively, you can navigate to `frontend` and `backend` folders separately and run `npm install`)*

### 4. Environment Variables
Create a `.env` file in the **`backend`** directory and configure the necessary keys (refer to `backend/.env.example` if available). 
```env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

### 5. Start the Application

You need to run both the backend server and the frontend development server.

**Start the Backend Server:**
```bash
cd backend
npm run dev
```

**Start the Frontend Server:**
Open a new terminal window/tab:
```bash
cd frontend
npm run dev
```

### 6. Open in Browser
Once both servers are running, open your browser and navigate to:
```
http://localhost:5173
```
*(The port might differ slightly based on Vite's allocation, check your frontend terminal output)*
