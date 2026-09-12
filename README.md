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
└── package.json

## 📚 Project Documentation

The complete project documentation and presentation for **Agrownex** are available below.

### 📘 Minor Project Report

The complete minor project report contains the project overview, objectives, system design, implementation details, technologies used, results, and future scope.

👉 [View Minor Project Report](./minor%20report.pdf)

### 📊 Agrownex Project Presentation

The project presentation provides an overview of the Agrownex platform, its features, technologies, architecture, implementation, and outcomes.

👉 [View Agrownex PPT](./Agrownex%20ppt.pptx)
