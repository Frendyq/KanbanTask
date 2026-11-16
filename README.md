# KanbanTask

Kanban board with real-time updates.

## Stack

- Frontend: Next.js 14, TypeScript, Tailwind CSS
- Backend: Node.js, Express
- Database: MongoDB
- Real-time: Socket.io
- Authentication: JWT
- File uploads: Multer
- Deployment: Docker

## Features

- User registration and login
- Boards and columns
- Drag and drop of tasks between columns
- Real-time updates
- Task comments
- File uploads
- Board members
- Task priorities and due dates

## Running

Create the backend configuration from the example and set your own JWT secret:

```bash
cp backend/.env.example backend/.env
```

With Docker:

```bash
git clone <repository-url>
cd kanbantask
docker-compose up --build
```

The frontend is available at http://localhost:3000 and the backend at http://localhost:5000.

Local development:

```bash
# backend
cd backend
npm install
npm run dev

# frontend (in a second terminal)
cd frontend
npm install
npm run dev
```

## Data model

Five collections: User, Board, Column, Task, Comment.

## Configuration

Backend settings are read from backend/.env (see backend/.env.example for the list). The frontend needs NEXT_PUBLIC_API_URL and NEXT_PUBLIC_BACKEND_URL in frontend/.env.local, pointing to the backend.

## Project structure

```
kanbantask/
  frontend/            Next.js app
  backend/             Express API
  docker-compose.yml
  README.md
```
