# Agrownex – Production-Ready Insurance Platform

Agrownex is a modern, type-safe web application that delivers agriculture-focused insurance with real-time weather analytics and an AI assistant. It is built with React 18 + Vite on the frontend and Express 5 on the backend, with support for deployment on Netlify and Vercel.

## 🌾 App Features

- 📱 Responsive layout with global header/footer and mobile navigation
- 🏠 Home page with:
  - Hero section
  - Insurance products
  - Partners
  - How it works
  - Impact metrics
  - Call-to-action
  - Local weather widget
- 🌦️ Weather analytics page with:
  - Geolocation support
  - New Delhi fallback location
  - Location search using Open-Meteo geocoding
  - Current weather
  - Hourly forecast
  - Daily forecast
  - Sunrise and sunset information
  - 6-month climatology
  - Interactive Recharts visualizations
  - Loading and error states
- 🤖 AI Assistant with:
  - Gemini API integration
  - Local chat history
  - Model fallback
  - Speech-to-Text input
  - Text-to-Speech playback
- 💬 Floating chat widget with scripted replies and local persistence
- 🛡️ Insurance products with detailed product cards and tier comparison
- 💼 Solutions page with interactive accordions
- 🤝 Partners page with lead form and local storage
- 📚 Resources page with searchable articles
- 💰 Quote calculator with:
  - Interactive calculations
  - Location geocoding
  - Weather-aware risk factor
  - Insurance quote estimation

## 🛠️ Tech Stack

- **React 18** – Frontend SPA
- **TypeScript** – Type-safe development
- **Vite 7** – Frontend tooling and development server
- **React Router 6** – Client-side routing
- **TailwindCSS 3** – Styling
- **Radix UI** – Accessible UI primitives
- **TanStack Query** – Data fetching and state management
- **Recharts** – Data visualization
- **Express 5** – Backend API
- **Vitest** – Testing
- **Gemini API** – AI assistant
- **Open-Meteo API** – Weather and climate data

## 📁 Project Structure

```text
Agrownex/
│
├── client/
│   ├── components/          # Reusable UI components
│   ├── pages/               # Application pages
│   └── lib/                 # Utility functions
│
├── server/
│   └── routes/              # Express API route handlers
│
├── shared/
│   └── api.ts               # Shared client/server API types
│
├── netlify/
│   └── functions/
│       └── api.ts           # Netlify serverless entry
│
├── api/
│   └── [...path].ts         # Vercel serverless entry
│
├── README.md
├── netlify.toml
├── vercel.json
├── minor-report.pdf
├── Agrownex-ppt.pptx
└── package.json

📚 Project Documentation

The complete project documentation and presentation for Agrownex are available below.

📘 Minor Project Report

The complete minor project report contains the project overview, objectives, system design, implementation details, technologies used, results, and future scope.

👉 View Minor Project Report

📊 Agrownex Project Presentation

The project presentation provides an overview of the Agrownex platform, its features, technologies, architecture, implementation, and outcomes.

👉 View Agrownex PPT

🚀 Getting Started
1. Clone the Repository
git clone YOUR_GITHUB_REPOSITORY_URL
cd Agrownex
2. Install Dependencies
pnpm install
3. Start the Development Server
pnpm dev

The application will be available at:

http://localhost:8080
🔐 Environment Variables

Create a .env file locally or configure these variables in your hosting provider.

GEMINI_API_KEY=your_gemini_api_key
PING_MESSAGE=your_custom_ping_message

⚠️ Never commit API keys or other secrets to the GitHub repository.

📜 Available Scripts
Development
pnpm dev

Starts the Vite development server with the Express API.

Production Build
pnpm build

Builds the client and server bundles.

Production Server
pnpm start

Starts the production Express server.

Testing
pnpm test

Runs the Vitest test suite.

Type Checking
pnpm typecheck

Runs TypeScript type checking.

🔌 API Overview

All API routes use JSON and CORS is enabled.

Method	Endpoint	Description
GET	/api/ping	Returns the configured ping message
GET	/api/demo	Returns a sample API response
POST	/api/chat/gemini	Sends prompts to the Gemini AI API
GET	/api/weather	Fetches weather and geocoding data
GET	/api/climate	Fetches climate information
Gemini API
POST /api/chat/gemini

Example request:

{
  "prompt": "What is crop insurance?",
  "system": "You are an agricultural insurance assistant."
}

Example response:

{
  "model": "gemini-model",
  "text": "..."
}
🧭 Frontend Routes
Route	Page
/	Home
/weather	Weather Analytics
/assistant	AI Assistant
/products	Insurance Products
/solutions	Solutions
/partners	Partners
/resources	Resources
/quote	Insurance Quote Calculator
🎨 Styling & Theme

Agrownex uses a custom design system based on HSL CSS variables.

Design tokens are defined in:

client/global.css

TailwindCSS is configured to consume these tokens through:

tailwind.config.ts

The platform uses an agriculture-inspired visual identity with emerald and amber design elements.

Update theme tokens using HSL values to avoid color rendering issues.

🌦️ External APIs
Open-Meteo

Agrownex uses Open-Meteo for:

Weather forecasts
Location geocoding
Climate data
Weather-based risk calculations
Google Gemini

Agrownex uses the Gemini API for:

AI-powered agricultural insurance assistance
Natural-language responses
Conversational support
☁️ Deployment
Netlify

The project includes Netlify configuration for deploying the React SPA and Express API using serverless functions.

netlify.toml
netlify/functions/api.ts

Configure the following environment variables in Netlify:

GEMINI_API_KEY
PING_MESSAGE
Vercel

The project also supports Vercel deployment using:

vercel.json
api/[...path].ts

Configure the following environment variables in Vercel:

GEMINI_API_KEY
PING_MESSAGE
🔒 Security
API keys are stored only on the server.
Secrets must never be exposed in frontend code.
Environment variables are used for sensitive configuration.
Third-party API requests are handled through backend API proxies.
Custom User-Agent headers are used where required.
CORS is enabled for API communication.
🐛 Troubleshooting
Icons Export Error

If a lucide-react icon is unavailable, replace it with a supported icon.

Weather Requests Failing

Make sure the application uses:

/api/weather

instead of directly calling Open-Meteo from the frontend.

Also ensure that your hosting provider allows outbound HTTPS requests.

Gemini API Errors

Check that:

GEMINI_API_KEY is correctly configured.
The selected Gemini model is available.
The backend API is running correctly.

The server supports fallback between preferred Gemini models.

🎯 Project Objective

Agrownex aims to simplify agricultural insurance by combining modern web technology with weather intelligence and AI assistance.

The platform focuses on providing:

🌾 Agriculture-focused insurance
🌦️ Real-time weather intelligence
🤖 AI-powered assistance
📊 Weather-aware risk analytics
💰 Interactive insurance quotations
📱 Modern and responsive user experience

The goal is to provide farmers and agricultural stakeholders with a more accessible, intelligent, and data-driven insurance experience.

🔮 Future Scope

Potential future enhancements include:

AI-based crop disease detection
Satellite-based crop monitoring
Automated claim processing
IoT-based farm monitoring
Advanced crop-risk prediction
Personalized insurance recommendations
Mobile application
Multilingual AI assistance
Real-time insurance claim tracking
Integration with additional agricultural data sources
📄 License

All rights reserved to the project owner.

This project is developed as an academic minor project. The source code, documentation, design, and project materials may not be reproduced or redistributed without permission from the project owner.


### ⚠️ One last check before committing

Your GitHub repository should have these files **at the same level as `README.md`**:

```text
📁 Agrownex
 ├── 📄 README.md
 ├── 📄 minor-report.pdf
 ├── 📊 Agrownex-ppt.pptx
 ├── 📄 package.json
 ├── 📁 client
 ├── 📁 server
 ├── 📁 shared
 ├── 📁 api
 └── 📁 netlify
