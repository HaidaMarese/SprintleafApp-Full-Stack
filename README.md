# SprintLeaf – MERN Course & Course Management App

SprintLeaf is a full-stack productivity app built with the MERN stack. It lets users manage projects, tasks, courses, notes, and learning resources — all in one place. Built for solo devs and small teams.

---

##  Features

### Authentication
- Register and login securely with JWT
- Persistent sessions via `localStorage`
- All API routes protected

### Project Management
- Create, edit, delete personal projects
- Invite collaborators

###  Task Management
- Add tasks with due date, status, and description
- Track status (`todo`, `in progress`, `done`)
- See task progress as a bar chart

###  Course Management
- Manage courses with title, description, status
- Track start/end dates

### Notes
- Quick personal notes linked to project or course
- Filter notes

### Calendar
- View task due dates and course schedules

---

##  Tech Stack

- **Frontend**: React, Vite, Tailwind CSS
- **Backend**: Node.js, Express
- **Database**: MongoDB Atlas, Mongoose
- **Auth**: JWT, bcryptjs
- **Charts**: Chart.js, react-chartjs-2
- **Deployment**: Render (backend), Netlify (frontend)

---

##  Local Setup

1. Clone the Repo
```bash
git clone https://github.com/YOUR_USERNAME/sprintleaf.git
cd sprintleaf
```

2. Backend Setup

``` bash
cd backend
npm install
Create a .env file
```

## env

- PORT=3000
- MONGO_URI=your_mongodb_uri
- JWT_SECRET=your_jwt_secret
- CORS_ORIGIN=http://localhost:5173

## Run:

bash
npm run dev

3. Frontend Setup

``` bash
cd frontend
npm install
Create a .env:
```
env:
- VITE_API_URL=http://localhost:3000

Run:
- npm run dev

##  API Routes

All protected routes require:

- Authorization: Bearer <token>

## Auth

- POST /api/auth/register
- POST /api/auth/login
- GET /api/auth/me

## Projects

- GET /api/projects
- POST /api/projects
- GET /api/projects/:id
- PATCH /api/projects/:id
- DELETE /api/projects/:id
- POST /api/projects/:id/invite

## Tasks

- GET /api/tasks
- POST /api/tasks
- PATCH /api/tasks/:id
- DELETE /api/tasks/:id

## Courses

- GET /api/courses
- POST /api/courses
- GET /api/courses/:id
- PATCH /api/courses/:id
- DELETE /api/courses/:id

## Notes

- GET /api/notes?project=ID
- GET /api/notes?course=ID
- POST /api/notes
- DELETE /api/notes/:id

## Deployment

- Backend (Render)
- Connect GitHub -> Select backend
- Add .env vars
- Build command: npm install
- Start command: node server.js

## Frontend (Netlify)

- Connect GitHub -> Select frontend
- Build command: npm run build
- Publish dir: dist
- Add: VITE_API_URL=https://your-backend-url.onrender.com

##  Author
Built by Haida Makouangou – PER-SCHOLAS- 2025 Full-Stack Capstone