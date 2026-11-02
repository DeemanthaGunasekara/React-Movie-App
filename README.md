# 🎬 React Movie App

A responsive movie discovery web application built with **React 19**, **Vite**, **React Router v7**, and **The Movie Database (TMDB) API**, containerized with **Docker** and **Nginx**.

---

## ✨ Features

- **Trending Movies**: Browse popular movies fetched live from TMDB API.
- **Instant Search**: Search movie titles with live API queries.
- **Favorites**: Save and remove favorites with persistent browser `localStorage`.
- **Responsive UI**: Dark-themed grid layout with card hover animations and mobile navbar.
- **Docker Ready**: Production-optimized build served through Nginx with SPA routing support.

---

## 🛠️ Tech Stack

- **React 19** + **Vite 8**
- **React Router v7**
- **TMDB REST API**
- **Context API** (State & `localStorage`)
- **Docker** + **Nginx**

---

## 🚀 Quick Start

### With Docker (Recommended)

```bash
docker compose up --build
```
Visit **`http://localhost:8080`** in your browser.

### Local Development

```bash
cd Frontend
npm install
npm run dev
```
Visit **`http://localhost:5173`** in your browser.

---

## 🔑 TMDB API Key

The app uses a free TMDB API key configured in `Frontend/src/services/api.js`. You can replace `API_KEY` with your own key from [themoviedb.org](https://www.themoviedb.org/) if desired.

---

## 📜 Scripts

Run inside the `Frontend` directory:
- `npm run dev` - Start Vite development server
- `npm run build` - Build production bundle to `Frontend/dist`
- `npm run lint` - Run Oxlint checks

---

## 📄 License

MIT License
