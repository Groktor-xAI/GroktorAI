# Groktor - AI Health Assistant

<p align="center">
  <img src="attached_assets/Ohne_Titel_208_1765068032404.png" alt="Groktor Logo" width="120" height="120" style="border-radius: 50%;">
</p>

<p align="center">
  <strong>Your charming AI health companion powered by Grok</strong>
</p>

<p align="center">
  <a href="https://groktor.fun">Website</a> |
  <a href="https://x.com/GroktorAI">Twitter/X</a>
</p>

---

## About

Groktor is an AI-powered health assistant that combines medical knowledge with a warm, encouraging personality. Describe your symptoms and receive helpful guidance in a conversational format. Groktor takes health seriously while making the experience pleasant and hopeful.

**CA:** `EuJtDzUnVYzwrjxHtvKYH2gTstGez1e5Z5Gka2p5pump`

## Features

- **Conversational AI Health Guidance** - Describe symptoms naturally and receive informed responses
- **Powered by Grok** - Leverages advanced AI for accurate, helpful health information
- **Charming Personality** - Witty and warm responses that lift your spirits while addressing concerns
- **Quick Symptom Selection** - One-click buttons for common symptoms (headache, fever, chest pain, back pain, fatigue, cough)
- **Dark/Light Mode** - Automatic theme detection with manual toggle
- **Mobile Responsive** - Works beautifully on all devices
- **Real-time Chat** - Instant responses with typing indicators
- **Video Background** - Immersive visual experience

## Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first styling
- **Shadcn/UI** - Beautiful, accessible components built on Radix UI
- **TanStack Query** - Powerful data fetching and caching
- **Wouter** - Lightweight client-side routing
- **Framer Motion** - Smooth animations
- **Lucide React** - Beautiful icons

### Backend
- **Node.js** with Express
- **TypeScript** - Type-safe server code
- **OpenAI SDK** - For OpenRouter/Grok integration
- **Zod** - Runtime type validation
- **Drizzle ORM** - Type-safe database queries (PostgreSQL ready)

## Project Structure

```
groktor/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/     # React components
│   │   │   ├── ui/         # Shadcn UI components
│   │   │   ├── Header.tsx
│   │   │   ├── ChatInput.tsx
│   │   │   ├── ChatMessages.tsx
│   │   │   ├── MessageBubble.tsx
│   │   │   ├── WelcomeState.tsx
│   │   │   ├── DisclaimerBanner.tsx
│   │   │   └── TypingIndicator.tsx
│   │   ├── pages/          # Page components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── lib/            # Utilities and helpers
│   │   └── App.tsx         # Main app component
│   ├── public/             # Static assets
│   └── index.html
├── server/                 # Backend Express server
│   ├── index.ts            # Server entry point
│   ├── routes.ts           # API routes
│   ├── openrouter.ts       # AI integration
│   └── storage.ts          # Data storage interface
├── shared/                 # Shared types and schemas
│   └── schema.ts           # Zod schemas and types
└── package.json
```

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn
- OpenRouter API key

### Environment Variables

Create a `.env` file in the root directory:

```env
AI_INTEGRATIONS_OPENROUTER_BASE_URL=https://openrouter.ai/api/v1
AI_INTEGRATIONS_OPENROUTER_API_KEY=your_api_key_here
SESSION_SECRET=your_session_secret
```

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/groktor.git
cd groktor

# Install dependencies
npm install

# Start development server
npm run dev
```

The app will be available at `http://localhost:5000`

### Build for Production

```bash
# Build the application
npm run build

# Start production server
npm start
```

## API Endpoints

### POST /api/chat

Send a message and receive an AI response.

**Request Body:**
```json
{
  "message": "I have a headache",
  "history": []
}
```

**Response:**
```json
{
  "response": "AI response text here..."
}
```

## AI Personality

Groktor is designed to be:

- **Charming & Warm** - Puts users at ease with friendly conversation
- **Witty but Respectful** - Light humor that uplifts without minimizing concerns
- **Hopeful & Encouraging** - Helps see the bright side while being realistic
- **Safety-First** - Drops humor immediately for serious symptoms and recommends emergency care

## Disclaimer

Groktor provides general health information only and is not a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of your physician or other qualified health provider with any questions you may have regarding a medical condition.

## Links

- **Website:** [groktor.fun](https://groktor.fun)
- **Twitter/X:** [@GroktorAI](https://x.com/GroktorAI)

## License

MIT License - see LICENSE file for details.

---

<p align="center">
  Made with care for your health and happiness
</p>
