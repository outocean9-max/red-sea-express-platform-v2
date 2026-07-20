```markdown
# Red Sea Express Setup Guide

## Requirements
Install:
- Docker
- Docker Compose
- Git

## Project Structure

```

red-sea-express/
├── backend/
├── frontend/
├── docs/
├── docker-compose.yml
└── .env.example

```

## Installation

Clone project:
```

git clone YOUR_REPOSITORY_URL

```

Enter folder:
```

cd red-sea-express

```

Create environment:
```

cp .env.example .env

```

Start system:
```

docker compose up

```

## Access
Frontend: `http://localhost:3000`
Backend: `http://localhost:8000`
Database: PostgreSQL Port: 5432

## Troubleshooting

Restart containers:
```

docker compose restart

```

Stop system:
```

docker compose down

```

## Development Rules
- Do not delete existing modules
- Keep frontend independent from backend
- Use migrations for database changes
- Keep AI assistant configuration centralized

## Project Name
Red Sea Express
AI Assistant: Aisha AI Assistant
