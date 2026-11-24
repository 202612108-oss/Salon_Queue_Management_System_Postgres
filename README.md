
# Salon Queue Management System

# Salon Queue Management System

A live salon queue for customers, receptionists, barbers, and the waiting-area display. The frontend is a React/Vite app; the API and real-time service use Express, Socket.IO, and SQLite.

## About the Project

Customers can join from a phone and track their place. Staff can manage arrivals and service, while the TV display shows the live queue.

## Technologies Used

- React
- Vite
- TypeScript
- Tailwind CSS
- Node.js
- Express
- SQLite
- Socket.IO

## Main Features

- Customer queue registration
- Service selection
- Barber selection
- Live queue tracking
- Reception Dashboard
- Barber View
- Waiting Area TV
- Owner Settings
- English, Gujarati, and Hindi support

## Local development

Requires Node.js and npm. From the repository root:

```sh
npm install
npm run dev
```

The frontend runs at `http://localhost:5173`; the API runs at `http://localhost:5000`.

## Deployment

The root `vercel.json` builds and serves the frontend from `frontend/dist`. Import this repository into Vercel with the repository root as the project root. The install command, build command, output directory, and SPA route rewrite are configured in the repository.

The backend is a separate service configured in `render.yaml`. Deploy it on Render with a persistent disk for SQLite, then set `VITE_BACKEND_URL` in the Vercel project to the backend's public base URL (for example, `https://your-service.onrender.com`). Set the backend's `FRONTEND_URL` to the Vercel deployment URL so browser API and Socket.IO requests are allowed.

The Render configuration uses a persistent disk and a paid Render plan. Review the service and storage pricing in Render before creating it. Do not commit `.env` files or local database files; they are ignored by Git.

## Screens

1. Home
2. Join Queue
3. My Status
4. Reception Dashboard
5. Barber View
6. Waiting Area TV
7. Owner Settings

