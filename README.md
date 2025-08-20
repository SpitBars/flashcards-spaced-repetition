# Flashcard Spaced Repetition App

A full-stack flashcard application with React frontend, Express backend, SQLite database, spaced repetition algorithm, and JWT authentication.

## Features

- **Frontend**: React with modern hooks and routing
- **Backend**: Express REST API with JWT authentication
- **Database**: SQLite with tables for users, decks, and cards
- **Spaced Repetition**: Algorithm for optimal review scheduling
- **Authentication**: JWT tokens with secure user management
- **Study Mode**: Interactive flip animations and grading system
- **Progress Tracking**: Dashboard with deck management

## Project Structure

```
flashcards-spaced-repetition/
├── client/                 # React frontend
│   ├── src/
│   │   ├── pages/         # Page components
│   │   └── providers/     # Context providers
│   ├── package.json
│   └── vite.config.js
├── server/                # Express backend
│   ├── middleware/        # Auth middleware
│   ├── db.js             # Database setup
│   ├── index.js          # Main server file
│   ├── test.js           # Test suite
│   └── package.json
└── README.md
```

## Quick Start

### Server Setup

```bash
cd server
cp .env.example .env
npm install
npm start
```

### Client Setup

```bash
cd client
npm install
npm run dev
```

### Running Tests

```bash
# Backend tests
cd server && npm test

# Frontend tests
cd client && npm test

# Build frontend
cd client && npm run build
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user

### Decks
- `GET /api/decks` - Get user decks
- `POST /api/decks` - Create new deck
- `DELETE /api/decks/:id` - Delete deck

### Cards
- `GET /api/decks/:deckId/cards` - Get cards in deck
- `POST /api/decks/:deckId/cards` - Add card to deck
- `PUT /api/cards/:id` - Update card
- `DELETE /api/cards/:id` - Delete card

### Study
- `GET /api/study/:deckId` - Get next card for study
- `POST /api/study/:cardId/grade` - Submit study grade (0-5)

## Frontend Routes

- `/` - Landing page
- `/login` - Login page
- `/register` - Registration page
- `/dashboard` - User dashboard with decks
- `/decks/new` - Create new deck
- `/decks/:deckId/cards/new` - Add new card
- `/study/:deckId` - Study mode

## Environment Variables

Copy `server/.env.example` to `server/.env` and configure:

```
JWT_SECRET=your_jwt_secret_here
DATABASE_URL=./flashcards.db
PORT=3001
```

## Deployment

This application is ready for deployment on platforms like:
- **Vercel** (recommended for frontend)
- **Railway** (for backend)
- **Netlify** (frontend alternative)
- **Render** (full-stack option)

### Vercel Deployment

1. Push code to GitHub
2. Connect repository to Vercel
3. Configure environment variables
4. Deploy!

## Test Results

✅ Backend tests passing  
✅ Frontend tests passing  
✅ Build successful  

## Technologies Used

- **Frontend**: React, Vite, CSS3
- **Backend**: Node.js, Express.js
- **Database**: SQLite
- **Authentication**: JWT
- **Testing**: Built-in test suites
- **Deployment**: Ready for Vercel/Railway/Netlify

## Live Demo

*Deployment URL will be added after successful deployment*

## License

MIT License
