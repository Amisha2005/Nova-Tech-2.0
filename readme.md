# 🚀 Nova-Tech 2.0

> **Nova-Tech 2.0** is a full-stack, AI-powered technical interview platform that helps users practice interviews with an intelligent AI interviewer.  
> It includes secure authentication, resume-based personalization, adaptive difficulty levels, real-time interview chat, and automated performance evaluation.

---

## ✨ Features

- 🤖 AI interviewer powered by **Groq LLM** (`llama-3.3-70b-versatile`)
- 🎚️ Adaptive interview difficulty levels: **Easy**, **Medium**, **Hard**
- 📄 Resume-based question personalization for realistic interview simulation
- 📊 Automated evaluation and scoring after interview completion
- 🔐 JWT-based authentication (signup, login, session-based access)
- 👤 Dedicated authenticated user account page
- 🎨 Responsive UI with dark/light theme support
- 💬 Real-time interview chat interface
- 🍃 MongoDB-powered data persistence

---

## 🛠️ Tech Stack

### Frontend
- **Next.js 16** (App Router)
- **React 19** + **TypeScript**
- **Tailwind CSS**
- **shadcn/ui** + **Radix UI**
- **React Hook Form** + **Zod**
- **next-themes**

### Backend
- **Node.js** + **Express.js**
- **MongoDB** + **Mongoose**
- **JWT** + **bcryptjs**
- **Zod** validation
- **CORS** + **dotenv**
- **Groq SDK** (`llama-3.3-70b-versatile`)

---

## ✅ Prerequisites

Before you begin, ensure you have:

- **Node.js 18+**
- **npm 9+**
- **MongoDB** (local installation or Atlas)
- **Groq API key**

---

## 🚀 Getting Started

### 1) Clone the Repository

~~~bash
git clone <your-repository-url>
cd Nova-Tech-2.0
~~~

### 2) Backend Setup

~~~bash
cd backend
npm install
cp .env.example .env
~~~

Update `backend/.env` with your values:

~~~env
MONGODB_URI=mongodb://127.0.0.1:27017/sampledb
JWT_SECRET_KEY=your_long_random_secret_key
GROQ_API_KEY=your_groq_api_key
~~~

Generate a strong JWT secret:

**Linux / macOS**
~~~bash
openssl rand -hex 64
~~~

**Windows (PowerShell)**
~~~powershell
node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"
~~~

### 3) MongoDB Setup

#### Linux (systemd)
~~~bash
sudo systemctl start mongod
sudo systemctl enable mongod
sudo systemctl status mongod
~~~

#### macOS (Homebrew)
~~~bash
brew tap mongodb/brew
brew install mongodb-community
brew services start mongodb-community
brew services list
~~~

#### Windows
1. Install MongoDB Community Server from the official MongoDB website.
2. Ensure MongoDB service is running.
3. Verify connection:

~~~powershell
mongosh
~~~

### 4) Seed Sample Users

~~~bash
cd backend
npm run seed
~~~

### 5) Run Backend Server

~~~bash
cd backend
npm start
~~~

Backend runs at: **http://localhost:5000**

### 6) Run Frontend App (new terminal)

~~~bash
cd frontend
npm install
npm run dev
~~~

Frontend runs at: **http://localhost:3000**

### 7) Login with Sample Users

- `demo1@example.com / demo123`
- `demo2@example.com / demo123`
- `admin@example.com / admin123`

---

## 📜 Available Scripts

### Backend (/backend)

| Script | Command | Description |
| --- | --- | --- |
| Start Server | `npm start` | Starts Express backend server |
| Seed Users | `npm run seed` | Seeds MongoDB with sample users |
| Test | `npm test` | Runs test script (placeholder/default) |

### Frontend (/frontend)

| Script | Command | Description |
| --- | --- | --- |
| Dev Server | `npm run dev` | Starts Next.js development server |
| Build | `npm run build` | Builds app for production |
| Start | `npm run start` | Runs production build |
| Lint | `npm run lint` | Runs ESLint |
| Audit | `npm run audit` | Runs npm security audit |

## 🔌 API Endpoints

Base URL: `http://localhost:5000/api`

| Module | Method | Endpoint | Description | Auth Required |
| --- | --- | --- | --- | --- |
| Auth | GET | `/auth` | Health/welcome auth route | No |
| Auth | POST | `/auth/register` | Register a new user | No |
| Auth | POST | `/auth/login` | Login user and return JWT | No |
| Auth | GET | `/auth/user` | Get current authenticated user | Yes (Bearer token) |
| Interview | POST | `/chat` | Send/receive interview chat message | No* |
| Interview | POST | `/evaluate` | Evaluate completed interview session | No* |

## 🔐 Environment Variables

| Variable | Required | Description | Example |
| --- | --- | --- | --- |
| `MONGODB_URI` | Yes | MongoDB connection URI | `mongodb://127.0.0.1:27017/sampledb` |
| `JWT_SECRET_KEY` | Yes | Secret key for JWT signing | `64+ char random string` |
| `GROQ_API_KEY` | Yes | API key for Groq inference | `gsk_...` |

## 🧯 Troubleshooting

### 1) `Cannot GET /` on backend root
This is expected if root route is not defined. Use API routes like:
- `http://localhost:5000/api/auth`
- `http://localhost:5000/api/auth/login`

### 2) Login fails with valid credentials
- Ensure backend is running on port `5000`
- Ensure frontend uses `http://localhost:5000` API URLs
- Re-run seed users:
  ~~~bash
  cd backend
  npm run seed
  ~~~

### 3) MongoDB connection error
- Verify MongoDB service is running
- Re-check `MONGODB_URI` in `.env`
- Confirm local port (default `27017`) is available

### 4) Invalid/expired JWT errors
- Ensure `JWT_SECRET_KEY` is set and unchanged
- Clear browser storage and login again

### 5) Groq API errors
- Verify `GROQ_API_KEY` in `.env`
- Check API quota/limits in Groq dashboard

### 6) Port already in use
Use different port or stop conflicting process.

---

## 🤝 Team Collaboration

Recommended workflow for teammates:

1. Pull latest code:
   ~~~bash
   git pull origin main
   ~~~

2. Install dependencies:
   ~~~bash
   cd backend && npm install
   cd ../frontend && npm install
   ~~~

3. Setup environment:
   - Copy `backend/.env.example` to `backend/.env`
   - Add personal/local values for secrets

4. Seed and run project:
   ~~~bash
   cd backend && npm run seed && npm start
   cd frontend && npm run dev
   ~~~

5. Use feature branches:
   ~~~bash
   git checkout -b feature/your-feature-name
   ~~~

6. Open Pull Requests with clear descriptions and test notes.

---

## 📄 License

This project is licensed under the **ISC License**.

---

## ❤️ Built With

**Node.js**, **Express**, **MongoDB**, **Mongoose**, **Next.js**, **React**, **TypeScript**, **Tailwind CSS**, **shadcn/ui**, and **Groq AI**.
