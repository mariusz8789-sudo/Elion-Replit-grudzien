AI-powered development and operations platform with chat interface, agent tools, and memory system.
Tech Stack

    Frontend: React 18 + Vite + TailwindCSS
    Backend: Express + TypeScript
    Database: PostgreSQL (Sequelize ORM)
    LLM: OpenAI GPT-5

Local Development

npm install
npm run dev

Opens frontend on http://localhost:5000 with backend API proxied from port 8080.
Production Build

npm run build
node packages/backend/dist/index.js

Deploy on Render

    Create a new Web Service connected to your GitHub repo
    Set Build Command: npm install && npm run build
    Set Start Command: node packages/backend/dist/index.js
    Add a PostgreSQL database and link it (provides DATABASE_URL)
    Add environment variables (see below)
    Deploy

Environment Variables
Variable	Required	Description
DATABASE_URL	Yes	PostgreSQL connection string
OPENAI_API_KEY	Yes	OpenAI API key for chat responses
PORT	No	Server port (default: 5000)
JWT_SECRET	No	JWT signing secret (default: dev_secret)
Authentication

Demo login password: ElionOmega1
Project Structure

packages/
├── frontend/     # React + Vite (port 5000)
└── backend/      # Express + TypeScript API
    └── src/
        ├── agent/      # AI agent with tools
        ├── chat/       # Chat service
        ├── memory/     # PostgreSQL + Sequelize
        ├── routes/     # API endpoints
        └── services/   # LLM integration
