SprintLeaf – Course Management App-Full-Stack MERN Application

SprintLeaf is a full-stack productivity app built with the **MERN stack**.  
It lets users manage projects, tasks, courses, notes, and learning resources all in one place.  

Built for solo developers and small teams.

---

##  Features

###  Authentication
- Register and login securely with **JWT**
- Persistent sessions via **localStorage**
- All API routes protected

###  Project Management
- Create, edit, delete personal projects
- Invite collaborators

###  Task Management
- Add tasks with due date, status, and description
- Track status (`todo`, `in progress`, `done`)
- See task progress as a **bar chart**

###  Course Management
- Manage courses with title, description, status
- Track start/end dates

###  Notes
- Quick personal notes linked to a project or course
- Filter notes by project or course

###  Calendar
- View task due dates and course schedules

---

## 🛠 Tech Stack
- **Frontend:** React, Vite, Tailwind CSS
- **Backend:** Node.js, Express
- **Database:** MongoDB Atlas, Mongoose
- **Auth:** JWT, bcryptjs
- **Charts:** Chart.js, react-chartjs-2
- **Deployment:** Render (backend), Netlify (frontend)

---

##  Demo
-  **Frontend:** [https://hscholar-app.netlify.app](https://hscholar-app.netlify.app)  
-  **Backend:** [https://sprintleaf-backend.onrender.com](https://sprintleaf-backend.onrender.com)

---

##  Local Setup

### 1️. Clone the Repo
```bash
git clone https://github.com/YOUR_USERNAME/sprintleaf.git
cd sprintleaf
```

## 2. Backend Setup

```bash
cd backend
npm install
```

### Create a .env file:

- PORT=3000
- MONGO_URI=your_mongodb_uri
- JWT_SECRET=your_jwt_secret
- CORS_ORIGIN=http://localhost:5173

### 4. Run the backend
```bash
npm run dev
```

## 3. Frontend Setup

- cd frontend
- npm install

### Create a .env file:

- VITE_API_URL=http://localhost:3000
- Run the frontend:

- npm run dev
  
##  API Routes

All protected routes require:
Authorization: Bearer <token>

### Auth

- POST /api/auth/register
- POST /api/auth/login
- GET /api/auth/me

### Projects

- GET /api/projects
- POST /api/projects
- GET /api/projects/:id
- PATCH /api/projects/:id
- DELETE /api/projects/:id
- POST /api/projects/:id/invite

### Tasks

- GET /api/tasks
- POST /api/tasks
- PATCH /api/tasks/:id
- DELETE /api/tasks/:id

### Courses

- GET /api/courses
- POST /api/courses
- GET /api/courses/:id
- PATCH /api/courses/:id
- DELETE /api/courses/:id

### Notes

- GET /api/notes?project=ID
- GET /api/notes?course=ID
- POST /api/notes
- DELETE /api/notes/:id

###  Deployment

1. Backend (Render)

- Connect GitHub → Select backend repo
- Add environment variables:
   . MONGO_URI=your_mongo_uri
   . JWT_SECRET=your_jwt_secret
   . CORS_ORIGIN=https://hscholar-app.netlify.app
- Build command:
   . npm install
   . Start command:
        . node src/server.js
  
2. Frontend (Netlify)
   
- Connect GitHub → Select frontend repo
- Add environment variable:
       .env
             - VITE_API_URL=https://sprintleaf-backend.onrender.com
             - Build command:
                  .npm run build
                  .Publish directory:
                       nginx
                       .dist
##  Author

Built by Haida Makouangou – UNCC-perscholas – 2025 Full-Stack Capstone
