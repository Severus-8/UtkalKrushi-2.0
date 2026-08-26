# Utkal Krushi (ଉତ୍କଳ କୃଷି) 🌾(2.0 hehehe)

A simple, reliable, and multilingual React frontend built for the farming community of Odisha and India.

## About

Utkal Krushi puts weather forecasts, AI crop diagnosis, fertilizer planning, mandi prices, government schemes, and more into one clean, easy-to-use portal — designed for farmers with varying levels of literacy and internet access.

The frontend is fully self-contained: every screen, calculator, and language switch works out of the box. It talks to a backend API for live data (weather, AI diagnosis, mandi prices, etc.), but falls back gracefully where possible so the app stays usable even without one connected.

## Features

- **Multilingual & Accessible** — switch instantly between Odia (ଓଡ଼ିଆ), Hindi (हिंदी), and English, with large touch targets, a high-contrast palette, and Text-to-Speech / Voice Input support.
- **Weather & Agro-Advisory** — live forecasts by district, GPS auto-location, and spray-safety advisories based on wind and rain.
- **AI Crop Doctor** — upload a photo or describe symptoms to get a disease diagnosis with organic and chemical remedies.
- **Fertilizer & Yield Calculator** — enter land size, crop, and soil details to get exact fertilizer bag quantities and an application schedule.
- **Mandi Prices & MSP Tracker** — live market rates across Odisha districts compared against government MSP.
- **Government Schemes Directory** — Odisha state and central government subsidy schemes with eligibility, documents, and apply links.
- **Krushi Mitra AI Chatbot** — a conversational assistant for farming questions, with voice input/output.
- **Crop Cultivation Guide** — seasonal guides for Kharif, Rabi, and Summer crops.
- **Farmer Khata (Ledger)** — track expenses and profit per acre.
- **Emergency Helplines** — one-tap dial for Kisan Call Center, PMFBY, and veterinary helplines.

## Why simple and reliable

- Built with a small, well-known stack — no heavy or experimental dependencies.
- UI, state management, language switching, voice features, and calculators are all implemented client-side, so most of the app works even before a backend is connected.
- Talks to any backend (Node.js, Python, Java, etc.) through one configurable base URL — no frontend code changes needed to swap backends.

## Tech Stack

- **React 18** + **Vite** for a fast dev/build setup
- **Tailwind CSS** for styling
- **Lucide Icons**
- **Web Speech API** for voice input and narration

## Project Structure

```
src/
├── components/       # UI sections (Weather, Crop Doctor, Fertilizer Calculator, Chatbot, etc.)
├── data/             # Static data: crops, diseases, schemes, mandi prices, translations
├── utils/            # Speech utilities, Gemini API integration
├── config/
│   └── api.js        # Backend API base URL & endpoint config
├── App.jsx
└── main.jsx
```

## Getting Started

1. Install dependencies:
   ```bash
   npm install
   ```
2. Start the dev server:
   ```bash
   npm run dev
   ```
   The app runs at `http://localhost:5173`.
3. Build for production:
   ```bash
   npm run build
   ```
   Static assets are output to the `dist/` folder.

## Connecting a Backend

By default the app looks for a backend at `http://localhost:5000/api`. To point it at a different backend, create a `.env` file in the project root:

```env
VITE_API_BASE_URL=http://localhost:5000/api
```

The frontend expects endpoints for weather, crop diagnosis, fertilizer calculation, mandi prices, schemes, chatbot, farmer ledger, and auth. See `src/config/api.js` for the full endpoint list, and `BACKEND_API_GUIDE.md` for exact request/response formats.

## Contributing

This started as a hackathon project and is still evolving. Forks, issues, and pull requests are welcome.

## Disclaimer

AI-generated recommendations, diagnoses, and predictions are for informational purposes only and should not replace professional agricultural advice.
