# Ledger

A habit tracker that makes consistency feel good. Real streaks, real analytics, no fake data.

## Stack

- **Client**: React + Vite, Tailwind CSS, Framer Motion, Recharts, Lucide icons
- **Server**: Node.js, Express, MongoDB + Mongoose, JWT auth, bcrypt

## Project structure

```
ledger/
  client/     — React app (Vite)
  server/     — Express API
```

## Getting started

### 1. Server

```bash
cd server
cp .env.example .env
# paste your MongoDB Atlas connection string into MONGO_URI
npm install
npm run dev
```

Server runs on `http://localhost:5001` with the included local `.env`, or the `PORT` value you choose.

### 2. Client

```bash
cd client
npm install
npm run dev
```

Client runs on `http://localhost:5173`.

## Environment variables (server/.env)

| Variable | Description |
|---|---|
| `MONGO_URI` | Your MongoDB Atlas connection string |
| `JWT_SECRET` | Any long random string, used to sign auth tokens |
| `JWT_EXPIRES_IN` | Token lifetime, e.g. `7d` |
| `PORT` | Server port (default 5001) |
| `CLIENT_URL` | Client origin for CORS, e.g. `http://localhost:5173` |

## Build status

The core full-stack app is implemented: auth, habit CRUD, daily logging, calendar data, and analytics views.


## Product modules

Ledger now includes the foundations for:
- 30-day, 90-day, and full-year consistency views across all habits
- Per-habit drill-downs and historical completion maps
- 30-day consistency trend graph and behavioral insight
- Milestone stamps
- Weekly recap
- Daily mood + notes
- Habit-specific notes
- Daily planner
- Unified day reflection
- Settings/profile management
