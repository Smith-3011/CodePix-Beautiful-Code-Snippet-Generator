# 🎨 CodePix – Beautiful Code Snippet Generator

CodePix is a full-stack, AI-powered web application that helps developers **create beautiful, shareable code snippets** with customizable themes, fonts, and backgrounds. It also provides **AI tools** to explain, optimize, translate, and generate code, making it useful for documentation, social sharing, and learning.

The project focuses on **developer experience, clean UI, and productivity**, combining a modern React frontend with a Node.js backend and Firebase for authentication and data storage.

---

## 🚀 Key Features

### ✨ Code Snippet Creation
- Create beautiful code snippets with **20+ themes**
- Custom fonts and customizable backgrounds
- **Real-time preview** while editing code
- Export snippets as **PNG / SVG**
- Responsive design for desktop and tablet

### 🤖 AI-Powered Tools
- **Explain Code**: Get a clear explanation of any code snippet
- **Optimize Code**: Improve performance and readability
- **Translate Code**: Convert code between languages
- **Generate Code**: Generate new code from prompts
- Powered by **Google Gemini / Groq** via backend APIs

### 📚 Snippet Management
- Save snippets to your personal library
- Organize and search saved snippets
- Share snippets easily
- Keep snippets **private** with authentication

### 🔐 Authentication & Security
- Secure login using **Firebase Authentication**
- User profiles and private snippet storage
- Protected backend API endpoints
- Only authenticated users can access saved snippets and AI features

### 🧑‍💻 Developer Experience
- Language auto-detection
- Dark / Light mode
- Keyboard shortcuts
- Clean and customizable UI
- Fast development using Vite

---

## 🛠️ Tech Stack

### Frontend
- React.js (v19+)
- Tailwind CSS
- Zustand (State Management)
- Vite
- Axios

### Backend
- Node.js (v18+)
- Express.js
- REST APIs

### Auth & Database
- Firebase Authentication
- Firestore (for snippet storage)

### AI Integration
- Google Gemini and/or Groq APIs

### Dev Tools
- Git & GitHub
- Postman

---

## 🏗️ System Architecture

- **Frontend (React)**:
  - Handles code editor UI, theming, preview, and exports
  - Manages user state and snippet library
  - Communicates with backend for AI operations

- **Backend (Node + Express)**:
  - Exposes REST APIs for AI features (explain, optimize, translate, generate)
  - Validates requests and forwards them to AI providers
  - Secures endpoints for authenticated users

- **Firebase**:
  - Handles user authentication
  - Stores user snippets securely in Firestore

- **AI Services**:
  - Processes code-related requests and returns results to backend

---

## 📁 Project Structure

```text
CodePix/
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── services/
│   ├── utils/
│   ├── index.js
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── store/
│   │   ├── lib/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
└── README.md
```

## 🔐 Authentication Flow

- Users sign up / log in using **Firebase Authentication**
- After login:
  - Users can create, save, and manage snippets
  - Users can access AI features
- Snippets are stored **per user** in Firestore
- Backend APIs are protected and only accessible to authenticated users

---

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v18+)
- Firebase Account
- AI API Key (Google Gemini and/or Groq)

---

### 🔧 Backend Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/codepix.git
cd codepix/backend

# Install dependencies
npm install
```

### Create a .env file in backend/:
```bash
PORT=5000
AI_API_KEY=your_ai_api_key
```

### Start the backend server:
```bash
Start the backend server:
```

### Backend will run on:
```bash
http://localhost:5000
``` 

### 🎨 Frontend Setup
``` bash 
# Go to frontend folder
cd ../frontend

# Install dependencies
npm install
```

### Configure Firebase:

1) Create a Firebase project

2) Enable Authentication and Firestore

3) Copy your Firebase config into:

`src/lib/firebase.js`

### Start the frontend:
```bash
npm run dev
```
### Frontend will run on:
```bash
http://localhost:5173
```

## 📡 API Highlights

- `POST /api/ai/explain` – Explain code  
- `POST /api/ai/optimize` – Optimize code  
- `POST /api/ai/translate` – Translate code  
- `POST /api/ai/generate` – Generate code from prompt  

All endpoints:
- Validate input  
- Call AI provider (Gemini / Groq)  
- Return formatted response to frontend  

---

## 📖 Usage

- **Create Snippet**: Paste or type code, choose theme, font, and background  
- **Export**: Download snippet as PNG or SVG  
- **AI Tools**: Use Explain, Optimize, Translate, or Generate features  
- **Save**: Store snippets in your personal library  
- **Manage**: Search, organize, and reuse saved snippets  

---

## 📊 Performance & Reliability

- Client-side caching for faster UI interactions  
- Secure API calls with validation  
- Firebase Firestore for scalable snippet storage  
- Handles **1000+ saved snippets** per user workspace smoothly  
- Optimized rendering for real-time preview updates  

---

## 🚀 Deployment

### Backend
- Deploy on Render / Railway / AWS / etc.  
- Set environment variables in hosting dashboard  

### Frontend

```bash
npm run build
```

- Deploy the dist/ folder to Netlify / Vercel

## 🧪 Testing

- API testing using Postman  
- Manual testing for:
  - Authentication flows  
  - Snippet creation and export  
  - AI features  
  - Snippet saving and retrieval  
  - Error handling and edge cases  

---

## 🤝 Contributing

1. Fork the repository  
2. Create a new feature branch  
3. Commit your changes  
4. Open a Pull Request  

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 💡 Future Improvements

- Team workspaces for shared snippet libraries  
- Version history for snippets  
- More export formats  
- More AI models and custom prompts  
- Browser extension for quick snippet capture  

