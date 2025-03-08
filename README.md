# LIPID - Modern AI Web Platform

A full-stack web platform that integrates natural language processing and image generation capabilities with a clean, responsive interface.

## Features

- Text generation using natural language models
- Image generation from text descriptions 
- Text analysis for sentiment, entities, and summarization
- Modern, responsive UI built with React
- RESTful API architecture
- Error handling and validation

## Project Structure

```
lipid/
├── src/
│   ├── backend/          # Express server, routes & controllers
│   │   ├── controllers/  # Request handlers
│   │   ├── routes/       # API route definitions
│   │   └── server.js     # Main server file
│   ├── frontend/         # React application
│   │   ├── public/       # Static assets
│   │   └── src/          # React components & styles
│   └── utils/            # Shared utilities
├── tests/                # API and component tests
├── .env                  # Environment variables
├── package.json          # Project dependencies
└── README.md             # Project documentation
```

## Installation & Setup

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Step 1: Clone the repository

```bash
git clone https://github.com/yourusername/lipid.git
cd lipid
```

### Step 2: Install backend dependencies

```bash
npm install
```

### Step 3: Configure environment variables

Create a `.env` file in the root directory:

```
PORT=3000
HUGGINGFACE_API_KEY=hf_dummy_key_for_free_endpoints
```

> Note: Most features work without authentication, but for models requiring it, get a free API key from https://huggingface.co

### Step 4: Install frontend dependencies

```bash
cd src/frontend
npm install
```

## Running the Application

### Development Mode

#### Start the backend server:

```bash
# From the root directory
npm run dev
```

#### Start the frontend development server:

```bash
# From another terminal
cd src/frontend
npm start
```

This will:
- Start the backend on http://localhost:3000
- Start the frontend on http://localhost:3001 (or another available port)
- Enable hot-reloading for both frontend and backend

### Production Mode

#### Build the frontend:

```bash
cd src/frontend
npm run build
```

#### Start the production server:

```bash
# From the root directory
npm start
```

The application will be available at http://localhost:3000.

## API Endpoints

The backend exposes the following RESTful API endpoints:

- **POST /api/ai/generate** - Generate text from a prompt
- **POST /api/ai/generate-image** - Generate an image from a text description
- **POST /api/ai/analyze** - Analyze text for sentiment, entities, and summary

## Testing

Run all tests:

```bash
npm test
```

Run a specific test:

```bash
npm test -- tests/api.test.js
```

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/awesome-feature`
3. Commit your changes: `git commit -m 'Add awesome feature'`
4. Push to the branch: `git push origin feature/awesome-feature`
5. Open a Pull Request

## Code Style

- Use 2-space indentation for JavaScript/JSX
- Group imports logically (React, third-party, local)
- Use camelCase for variables/functions, PascalCase for components
- Handle errors with specific catches in async functions

## License

MIT