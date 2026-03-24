# 🚀 Nova-Tech-2.0

> A cutting-edge full-stack web application combining AI/ML capabilities with modern web technologies for interview preparation and skill development.

![Next.js](https://img.shields.io/badge/Next.js-16.2.1-black?style=flat-square&logo=next.js)
![React](https://img.shields.io/badge/React-19.2.0-blue?style=flat-square&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)

---

## 📋 Table of Contents

- [✨ Features](#-features)
- [🏗️ Project Structure](#️-project-structure)
- [🛠️ Tech Stack](#️-tech-stack)
- [📦 Prerequisites](#-prerequisites)
- [🚀 Getting Started](#-getting-started)
- [📝 Available Scripts](#-available-scripts)
- [🔒 Security](#-security)
- [📚 API & Components](#-api--components)
- [🐛 Troubleshooting](#-troubleshooting)
- [🤝 Contributing](#-contributing)


---

## ✨ Features

### 🤖 AI/ML Capabilities
- 👁️ **Face Detection**: Real-time face detection using TensorFlow and MediaPipe
- 🎯 **Object Detection**: COCO-SSD for identifying objects in images/video
- 💪 **Pose Detection**: Skeleton-based pose recognition for fitness tracking
- 🧠 **LLM Integration**: Groq SDK for AI-powered text analysis

### 📖 Educational Platform
- 📚 **Learning Resources**: Comprehensive learning modules and articles
- 🎤 **Interview Preparation**: Structured interview practice modules
- ✅ **Progress Tracking**: Account-based progress monitoring
- 🎉 **Achievement System**: Congratulations and milestone tracking

### 👤 User Management
- 🔐 **Authentication**: Secure login and signup system
- 👤 **Account Management**: User profile and preferences
- 🔑 **Session Management**: Secure session handling
- ⚙️ **User Settings**: Customizable account settings

### 📄 Document Processing
- 📕 **PDF Support**: Full PDF viewing and processing capabilities
- 📊 **Document Analysis**: Extract and analyze document content

### 🎨 Modern UI/UX
- 🌈 **Theme Support**: Light and dark mode themes
- 📱 **Responsive Design**: Mobile-first, fully responsive layouts
- ♿ **Accessibility**: WCAG compliant components
- ⚡ **Performance Optimized**: Fast load times and smooth interactions

---

## 🏗️ Project Structure

```
Nova-Tech-2.0/
├── 📁 frontend/                      # Next.js React application
│   ├── 📁 app/
│   │   ├── 📄 Auth.tsx              # Authentication component
│   │   ├── 📄 layout.tsx            # Root layout
│   │   ├── 📄 page.tsx              # Home page
│   │   ├── 📄 theme-provider.tsx    # Theme configuration
│   │   ├── 📄 globals.css           # Global styles
│   │   ├── 📁 about/                # About page
│   │   ├── 📁 account/              # User account management
│   │   ├── 📁 articles/             # Learning articles
│   │   ├── 📁 congratulations/      # Achievement pages
│   │   ├── 📁 interview/            # Interview prep modules
│   │   ├── 📁 learn/                # Learning resources
│   │   ├─��� 📁 login/                # Login page
│   │   └── 📁 signup/               # Registration page
│   ├── 📄 package.json              # Dependencies
│   ├── 📄 tsconfig.json             # TypeScript config
│   └── 📄 next.config.js            # Next.js config
│
├── 📁 backend/                       # Backend services (API, database)
│   └── (Backend implementation)
│
└── 📄 README.md                     # This file
```

---

## 🛠️ Tech Stack

### 🎨 Frontend Framework
| Technology | Version | Purpose |
|-----------|---------|---------|
| **Next.js** | 16.2.1 | React framework for production |
| **React** | 19.2.0 | UI library |
| **TypeScript** | 5 | Type-safe JavaScript |

### 🎯 AI/ML Libraries
| Library | Version | Purpose |
|---------|---------|---------|
| **TensorFlow.js** | 4.22.0 | Machine learning in browser |
| **TensorFlow Backend** | 4.22.0 | WebGL acceleration |
| **MediaPipe** | 0.10.32 | Vision tasks (pose, hand, face) |
| **TensorFlow COCO-SSD** | 2.2.3 | Object detection |
| **TensorFlow Face Detection** | 1.0.3 | Face recognition |
| **Face-API.js** | 0.22.2 | Face detection & recognition |

### 🎮 UI Component Libraries
| Library | Version | Purpose |
|---------|---------|---------|
| **Radix UI** | 1.4.3 | Headless UI components |
| **Tailwind CSS** | 4 | Utility-first CSS framework |
| **Lucide React** | 0.555.0 | Icon library |

### 📝 Form & Validation
| Library | Version | Purpose |
|---------|---------|---------|
| **React Hook Form** | 7.68.0 | Performant form handling |
| **Zod** | 4.1.13 | TypeScript-first validation |

### 🔧 Utilities
| Library | Version | Purpose |
|---------|---------|---------|
| **Groq SDK** | 0.37.0 | LLM API integration |
| **PDF.js** | 5.5.207 | PDF rendering |
| **Next Themes** | 0.4.6 | Theme management |
| **React Router DOM** | 7.10.1 | Client-side routing |

### 🔧 Development Tools
| Tool | Version | Purpose |
|------|---------|---------|
| **ESLint** | 9 | Code linting |
| **PostCSS** | 4 | CSS transformation |

---

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** >= 18.0.0 ([Download](https://nodejs.org/))
- **npm** >= 9.0.0 (comes with Node.js)
- **Git** >= 2.0.0 ([Download](https://git-scm.com/))

### Optional but Recommended
- **VS Code** - Code editor
- **Git Bash** (Windows users) - Better terminal experience

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Amisha2005/Nova-Tech-2.0.git
cd Nova-Tech-2.0
```

### 2️⃣ Setup Frontend

```bash
cd frontend
npm install
```

### 3️⃣ Setup Environment Variables

Create a `.env.local` file in the `frontend/` directory:

```env
# Add your environment variables here
NEXT_PUBLIC_API_URL=http://localhost:3001
GROQ_API_KEY=your_groq_api_key_here
```

### 4️⃣ Start Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

### 5️⃣ Setup Backend (Optional)

```bash
cd ../backend
npm install
npm run dev
```

Backend will run on [http://localhost:3001](http://localhost:3001)

---

## 📝 Available Scripts

### Frontend Scripts

```bash
# 🏃 Start development server with hot reload
npm run dev

# 🏗️ Build for production
npm run build

# 🚀 Start production server
npm start

# 🧹 Run ESLint
npm run lint

# 🔒 Audit security vulnerabilities (high severity only)
npm audit

# 🛠️ Fix security vulnerabilities automatically
npm audit fix

# 💪 Force fix with dependency overrides
npm audit fix --force
```

### Backend Scripts

```bash
# 🏃 Start development server
npm run dev

# 🏗️ Build for production
npm run build

# 🚀 Start production server
npm start
```

---

## 🔒 Security

### 🛡️ Vulnerability Management

This project includes security measures to prevent known vulnerabilities:

**Current Security Status:**
- ✅ **node-fetch** vulnerabilities fixed via overrides
- ✅ **All high-severity vulnerabilities** addressed
- ✅ Regular security audits enabled

### 🔧 npm Audit Management

```bash
# Check for vulnerabilities
npm audit

# Audit only high-severity issues
npm audit --audit-level=high

# Fix vulnerabilities automatically
npm audit fix

# Force fix with overrides (use with caution)
npm audit fix --force
```

### 📋 Active Security Overrides

```json
{
  "overrides": {
    "node-fetch": "^3.3.2",
    "next": "16.2.1"
  }
}
```

These overrides ensure that:
- Nested dependencies use patched versions
- Security headers are properly forwarded
- No redirect vulnerabilities exist

---

## 📚 API & Components

### 🔐 Authentication
- **Auth.tsx** - Main authentication component
- Login endpoint - POST `/api/auth/login`
- Signup endpoint - POST `/api/auth/signup`
- Logout endpoint - POST `/api/auth/logout`

### 🤖 AI/ML Endpoints
- Face Detection - POST `/api/ml/face-detect`
- Object Detection - POST `/api/ml/object-detect`
- Pose Detection - POST `/api/ml/pose-detect`

### 📖 Content Endpoints
- Get Articles - GET `/api/articles`
- Get Courses - GET `/api/learn`
- Get Interview Questions - GET `/api/interview`

### 👤 User Endpoints
- Get Profile - GET `/api/user/profile`
- Update Profile - PUT `/api/user/profile`
- Get Account Settings - GET `/api/user/settings`

---

## 🐛 Troubleshooting

### ❌ npm Installation Issues

**Problem**: npm audit shows vulnerabilities

**Solution**:
```bash
# Clean cache
npm cache clean --force

# Remove node_modules and lock file
rm -rf node_modules package-lock.json

# Fresh install
npm install

# Fix vulnerabilities
npm audit fix --force
```

### ❌ Port Already in Use

**Problem**: Port 3000 is already in use

**Solution**:
```bash
# Use a different port
npm run dev -- -p 3001
```

### ❌ Module Not Found

**Problem**: "Module not found" errors

**Solution**:
```bash
# Reinstall dependencies
rm -rf node_modules
npm install

# Clear Next.js cache
rm -rf .next
npm run dev
```

### ❌ TypeScript Errors

**Problem**: TypeScript compilation errors

**Solution**:
```bash
# Check TypeScript configuration
npx tsc --noEmit

# Rebuild
npm run build
```

### ❌ Build Fails

**Problem**: Production build fails

**Solution**:
```bash
# Clean everything
rm -rf .next node_modules package-lock.json

# Reinstall
npm install

# Build again
npm run build
```

### 💡 Common Issues & Solutions

| Issue | Cause | Solution |
|-------|-------|----------|
| Port 3000 in use | Another app using port | Change port: `npm run dev -- -p 3001` |
| CORS errors | Backend not running | Start backend: `cd backend && npm run dev` |
| Styling not applied | Tailwind not compiled | Clear cache: `rm -rf .next` |
| API errors | Environment variables missing | Create `.env.local` with required vars |

---

## 🤝 Contributing

We love contributions! Here's how to help:

### 🍴 Fork & Clone
```bash
git clone https://github.com/YOUR_USERNAME/Nova-Tech-2.0.git
cd Nova-Tech-2.0
```

### 🌿 Create Feature Branch
```bash
git checkout -b feature/your-feature-name
```

### 💻 Make Changes
- Write clean, modular code
- Follow TypeScript best practices
- Add comments for complex logic
- Ensure no security vulnerabilities

### ✅ Test Your Changes
```bash
npm run lint
npm audit
npm run build
```

### 📤 Submit Pull Request
```bash
git add .
git commit -m "feat: description of your feature"
git push origin feature/your-feature-name
```

Then open a PR on GitHub!

### 📝 Guidelines
- ✅ Write descriptive commit messages
- ✅ Update documentation
- ✅ Test thoroughly
- ✅ Fix all linting issues
- ✅ No security vulnerabilities
- ✅ Include screenshots for UI changes

---

## 📖 Documentation

- 📚 [Next.js Documentation](https://nextjs.org/docs)
- 🔗 [React Documentation](https://react.dev)
- 🎨 [Tailwind CSS Docs](https://tailwindcss.com/docs)
- 🧩 [Radix UI Components](https://www.radix-ui.com/)
- 🧠 [TensorFlow.js Guide](https://www.tensorflow.org/js)
- 🤖 [MediaPipe Documentation](https://developers.google.com/mediapipe)
- 🔐 [Zod Validation](https://zod.dev)

---





## 🐞 Known Issues

| Issue | Status | Workaround |
|-------|--------|-----------|
| TensorFlow models load time | 🟡 In Progress | Cache models locally |
| Large PDF rendering | 🟡 Optimizing | Lazy load pages |
| Mobile face detection | 🟢 Fixed | Use updated MediaPipe |

---






## 📈 Project Stats

![GitHub Stars](https://img.shields.io/github/stars/Amisha2005/Nova-Tech-2.0?style=flat-square)
![GitHub Forks](https://img.shields.io/github/forks/Amisha2005/Nova-Tech-2.0?style=flat-square)
![GitHub Issues](https://img.shields.io/github/issues/Amisha2005/Nova-Tech-2.0?style=flat-square)
![Last Commit](https://img.shields.io/github/last-commit/Amisha2005/Nova-Tech-2.0?style=flat-square)

---

## 🔄 Changelog

### Version 0.1.0 (Current)
- ✨ Initial release
- 🤖 AI/ML capabilities integrated
- 📖 Educational platform launched
- 🔐 Security vulnerabilities fixed
- 📱 Responsive design implemented

---

<div align="center">

### ⭐ If you like this project, please consider giving it a star! ⭐

**[Back to Top](#-nova-tech-20)**

Made with ❤️ by the Nova-Tech Team

</div>
