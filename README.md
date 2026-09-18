# FlowBoard — CodeAlpha Task 3

Full-stack Trello/Asana-style project management tool built with Node.js, Express.js, MongoDB, HTML, CSS, JavaScript and Socket.io.

## Features
- JWT authentication + bcrypt password hashing
- User/admin roles
- Create, edit, delete projects and manage members
- Kanban tasks: To Do, In Progress, Done
- Task assignment, priority, due date and drag-and-drop
- Task comments
- Socket.io real-time project updates
- Notifications with read/unread state
- Responsive frontend
- Automated tests and GitHub Actions CI

## Setup
```bash
npm install
cp .env.example .env
# configure MONGODB_URI and a strong JWT_SECRET
npm start
```
Open http://localhost:5000.

## API
Auth: POST /api/auth/register, POST /api/auth/login, GET /api/auth/profile
Projects: GET/POST /api/projects, PUT/DELETE /api/projects/:id, POST /api/projects/:id/members
Tasks: GET/POST /api/tasks/project/:projectId, PUT/PATCH/DELETE /api/tasks/:id
Comments: GET/POST /api/comments/task/:taskId, DELETE /api/comments/:id
Notifications: GET /api/notifications, PATCH /api/notifications/:id/read, POST /api/notifications/read-all

## Testing
```bash
npm test
```

## License
MIT