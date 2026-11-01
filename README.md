# 🎬 React Movie App

A modern, responsive movie discovery web application built with **React 19**, **Vite**, and **React Router v7**, powered by **The Movie Database (TMDB) API**.

Browse trending and popular movies, search through thousands of titles, and manage your personal collection of favorites saved directly to your browser's local storage.

---

## ✨ Features

- **🔥 Popular Movies**: Browse trending and popular movies fetched live from TMDB API.
- **🔍 Instant Search**: Search for movies by title with real-time API queries.
- **❤️ Favorites Management**: Save and remove movies from your favorites with persistent browser `localStorage`.
- **⚡ Centralized State**: Powered by React Context API (`MovieContext`) for smooth state management across views.
- **📱 Fully Responsive Design**: Sleek dark-mode aesthetic with custom CSS Grid layouts, card hover effects, and a mobile-friendly navbar.
- **⚡ Fast Development**: Built with Vite 8 for instant Hot Module Replacement (HMR).

---

## 🛠️ Tech Stack

- **Frontend Library**: [React 19](https://react.dev/)
- **Build Tool & Dev Server**: [Vite 8](https://vitejs.dev/)
- **Routing**: [React Router DOM v7](https://reactrouter.com/)
- **API**: [The Movie Database (TMDB) REST API](https://www.themoviedb.org/documentation/api)
- **Linter**: [Oxlint](https://oxc.rs/)
- **Styling**: Vanilla CSS (Modular CSS for Navbar, Cards, Pages, and Utilities)

---

## 📁 Project Structure

```text
React-Demo-Project/
├── Frontend/
│   ├── public/
│   │   ├── favicon.svg
│   │   └── icons.svg
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   │   ├── MovieCard.jsx       # Individual movie card with poster & favorite toggle
│   │   │   └── NavBar.jsx          # Top navigation bar with routing links
│   │   ├── context/
│   │   │   └── MovieContext.jsx    # React Context for managing and persisting favorites
│   │   ├── css/
│   │   │   ├── App.css             # Main container layout
│   │   │   ├── Favorites.css       # Favorites page styling and empty state
│   │   │   ├── Home.css            # Home view, search bar, and movie grid
│   │   │   ├── Index.css           # Global resets and root typography
│   │   │   ├── MovieCard.css       # Movie cards, overlay animations, and heart button
│   │   │   └── Navbar.css          # Navigation styling
│   │   ├── pages/
│   │   │   ├── Favorites.jsx       # Favorited movies view
│   │   │   └── Home.jsx            # Main view with search and popular movies
│   │   ├── services/
│   │   │   └── api.js              # TMDB API service functions (popular & search)
│   │   ├── App.jsx                 # Route definitions and provider wrapper
│   │   └── main.jsx                # Application root with BrowserRouter
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed (version 18 or higher recommended).

### 1. Clone the repository

```bash
git clone https://github.com/your-username/React-Demo-Project.git
cd React-Demo-Project/Frontend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure the TMDB API Key

The application fetches data from TMDB. The default API key is set in `src/services/api.js`.

If you want to use your own API key:
1. Sign up for a free account at [themoviedb.org](https://www.themoviedb.org/).
2. Request an API key from your account settings.
3. Replace the `API_KEY` in `src/services/api.js` or configure environment variables.

### 4. Start the development server

```bash
npm run dev
```

Open your browser and navigate to `http://localhost:5173`.

---

## 📜 Available Scripts

Inside the `Frontend` directory, you can run:

| Command | Description |
| :--- | :--- |
| `npm run dev` | Starts the Vite development server with Hot Module Replacement |
| `npm run build` | Compiles and bundles production-ready assets into `dist/` |
| `npm run preview` | Locally previews the production build |
| `npm run lint` | Runs Oxlint to check code quality and detect issues |

---

## 💡 How It Works

1. **Browsing**: When the application loads, `useEffect` in `Home.jsx` triggers `getpopularMovies()` to fetch trending titles from TMDB.
2. **Searching**: Submitting the search form triggers `searchMovies(searchQuery)` via the TMDB search endpoint.
3. **Favorites Context**:
   - `MovieContext.jsx` initializes favorites state directly from `localStorage`.
   - Clicking the heart (♥) on any card toggles its favorite status.
   - Any changes automatically sync back to `localStorage`.
4. **Favorites Page**: Navigating to `/favorites` displays all saved cards; if none are saved, it shows an empty state banner.

---

## 🔮 Future Improvements

- [ ] Add movie details page with synopsis, cast, and trailers
- [ ] Add pagination or infinite scroll for browsing more movies
- [ ] Filter by genre (Action, Comedy, Drama, Sci-Fi, etc.)
- [ ] Rating and review submissions

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
