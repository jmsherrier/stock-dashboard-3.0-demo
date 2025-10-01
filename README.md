# Multi-Strategy Trading Analysis Platform

## Overview
A full-stack trading analysis platform for screening, scoring, and managing stocks using customizable strategies. Built with React and Express, it features a modular, drag-and-drop interface, real-time data integration, and a robust scoring system.

## Features
- **2D Grid System:** Organize stocks in a flexible, expandable grid. Add/remove rows and columns, auto-sort, and zoom.
- **Drag-and-Drop:** Move, swap, and reorder stocks anywhere in the grid with smooth drag-and-drop.
- **Custom Strategies:** Create, configure, and apply multiple trading strategies (momentum, growth, value, or custom).
- **Modular Components:** Each metric (price, volume, news, etc.) is a standalone, configurable component.
- **Real-Time Data:** Live stock data via Alpha Vantage API, with fallback demo data for reliability.
- **Advanced Scoring:** Color-coded, real-time scoring with custom ranges and bonus checks.
- **Settings & Presets:** User-friendly settings modal for theme, auto-save, auto-sort, and more.
- **Authentication:** Secure, multi-user support with email/password login and developer access mode.
- **Responsive UI:** Works on desktop and mobile, with a modern dark theme.

## Demo
![Platform Demo](./Demo3.0.gif)

## Codebase Structure
```
whiteboard/
├── momentum-tracker/
│   ├── src/
│   │   ├── App.js            # Main React app, grid logic, drag-and-drop
│   │   ├── App.css           # Styling (CSS Grid, Flexbox, dark theme)
│   │   ├── components/       # Modular UI components (StockPaper, Modals, Editors)
│   │   ├── api/              # API client for backend communication
│   │   ├── services/         # Stock data and scoring logic
│   │   ├── constants/        # Scoring and config constants
│   │   ├── hooks/            # Custom React hooks (e.g., useStocks)
│   │   ├── utils/            # Utility functions
│   │   └── ...
│   ├── server/
│   │   ├── server.js         # Express backend
│   │   ├── routes/           # API endpoints (auth, stocks, strategies)
│   │   ├── db/               # SQLite database logic
│   │   ├── middleware/       # Auth, error handling, logging
│   │   └── ...
│   └── ...
└── PortfolioREADME.md        # Portfolio showcase (this file)
```

## Tech Stack
- **Frontend:** React 19.1.1, @dnd-kit, CSS Grid/Flexbox
- **Backend:** Express.js, SQLite, bcrypt
- **APIs:** Alpha Vantage (real-time stock data)
- **Other:** LocalStorage, modular component pattern

## Example API Endpoints
```
POST /api/auth/login         # User login
GET  /api/stocks             # Fetch user’s stocks
POST /api/stocks/save        # Save stock data
GET  /api/stocks/quote/:ticker # Real-time quote
```

## Database Schema (Excerpt)
```sql
users (id, email, password_hash, ...)
user_stocks (id, user_id, stocks_data, ...)
strategies (id, user_id, name, config, ...)
```

## How It Works
1. **Sign Up / Login:** Secure authentication for each user.
2. **Add Stocks:** Quickly add stocks to the grid, edit data, and fetch real-time prices.
3. **Drag & Drop:** Reorder, swap, or move stocks anywhere in the grid.
4. **Configure Strategies:** Choose or create strategies, set scoring rules, and apply presets.
5. **Analyze & Score:** Instantly see color-coded scores and rankings for all stocks.

---



