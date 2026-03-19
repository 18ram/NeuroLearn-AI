# NeuroLearn AI 🧠

NeuroLearn AI is a comprehensive, AI-powered educational platform designed to help students and lifelong learners master complex subjects through intelligent document analysis, interactive quizzes, and data-driven progress tracking.

## 🚀 Features

- **AI Document Analysis**: Upload PDFs or text documents to get instant, high-quality summaries and key concept extractions.
- **Interactive Quizzes**: Automatically generate quizzes with varying difficulty levels (Easy, Medium, Hard) based on your uploaded content.
- **Smart Flashcards**: Create flashcards for active recall and spaced repetition study sessions.
- **Learning Dashboard**: Track your performance with real-time metrics, including:
  - **Total Documents**: Count of your learning materials.
  - **Learning Sessions**: History of completed quizzes and flashcard reviews.
  - **Average Score**: Performance tracking across all quiz sessions.
  - **Learning Streak**: Consistency tracking to keep you motivated.
  - **Performance Trend**: Visual chart showing your progress over time.
- **Secure Authentication**: Integrated with Firebase Auth for secure Google login.
- **Real-time Persistence**: All your documents and progress are saved securely in Google Cloud Firestore.

## 🛠️ Tech Stack

- **Frontend**: React 19, TypeScript, Vite
- **Styling**: Tailwind CSS, Framer Motion (for smooth animations)
- **Icons**: Lucide React
- **Charts**: Recharts
- **AI Engine**: Google Gemini AI (`@google/genai`)
- **Backend/Database**: Firebase (Firestore, Authentication)
- **PDF Processing**: `pdfjs-dist`

## ⚙️ Setup Instructions

### 1. Prerequisites
- Node.js (v18 or higher)
- A Google Cloud Project with Gemini API access.
- A Firebase Project.

### 2. Environment Variables
To run this application, you need to set up the following environment variables in your environment or a `.env` file:

```env
# Gemini AI API Key
GEMINI_API_KEY=your_gemini_api_key_here

# Firebase Configuration (from firebase-applet-config.json)
VITE_FIREBASE_API_KEY=your_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain
VITE_FIREBASE_PROJECT_ID=your_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
VITE_FIREBASE_APP_ID=your_app_id
```

*Note: In the AI Studio Build environment, these are managed via the Secrets menu.*

### 3. Installation
```bash
# Install dependencies
npm install

# Start the development server
npm run dev
```

The application will be available at `http://localhost:3000`.

## 📝 Summary of Work

NeuroLearn AI was built to bridge the gap between passive reading and active learning. By leveraging the Gemini 1.5 Flash model, the application transforms static study materials into dynamic learning experiences. 

Key technical implementations include:
- **Surgical AI Prompting**: Custom prompts to ensure AI outputs are structured correctly for quizzes and flashcards.
- **Real-time Data Sync**: Using Firestore `onSnapshot` to ensure the dashboard reflects the latest learning sessions immediately.
- **Responsive Design**: A mobile-first, bento-grid inspired UI that works across all devices.
- **Robust Error Handling**: Custom Firestore error handlers to diagnose and fix security rule issues in real-time.

---
Built with ❤️ for learners everywhere.
