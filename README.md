# TaskDesk Frontend

Modern Angular (v22) Task Management Web Application.

Companion backend repository: [TaskDesk-backend](https://github.com/Anchal82-del/TaskDesk-backend)

---

## Features

- **Task List Page & Dynamic Table**: Responsive task list with fields: ID, Title, Priority, Status, Reviewer, and Assignee.
- **Dynamic Filters & Search**: Real-time filtering by status (`todo`, `progress`, `done`), priority (`high`, `medium`, `low`), project, and instant search across titles and descriptions.
- **Pagination & Sorting**: Configurable entries per page (5, 10, 15, 20), dynamic sorting by ID, status, or priority with ascending/descending order toggle.
- **Task Creation & Editing Form**: Reactive form with validation for title, description, priority, status, reviewer, assignee, and project.
- **Full Row Actions**:
  - **View**: Modal showing comprehensive task details, badges, and project information.
  - **Edit**: Modal pre-populated with task data for updating fields.
  - **Delete**: Confirmation dialog with permanent delete action.
- **Angular Services**: `TaskService` communicates with the Express backend via `HttpClient`, providing optimistic UI updates and reactive state streams.
- **Template Control Flow**: Modern Angular `@if`, `@for`, and `@empty` control flows.
- **Export to CSV**: Instant client-side CSV export of filtered tasks.
- **In-App Toast Notifications (Top Right)**: Immediate visual feedback for create, update, delete, CSV export, sign-in, and error events.
- **User Scoping**: Authenticated users only see tasks where they are the Assignee or Reviewer.
- **Reviewer !== Assignee Constraint**: Dropdown restrictions and form validation guarantee that the reviewer and assignee for any task are never the same person.
- **Admin Access Requests & Role-Based Navigation**: Non-admin users can submit admin access requests; admins can review, approve, or decline them.
- **CSV & Excel User Import**: Admin interface with live client-side validation, duplicate detection, preview table, and bulk upload.

---

## Getting Started

### Prerequisites
- Node.js (v20+ recommended)
- npm

### 1. Install Dependencies
```bash
npm install
```

### 2. Start the Frontend Development Server
```bash
npm start
```
Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

### 3. Backend Companion
Make sure your backend API is running at `http://localhost:3000` from the [TaskDesk-backend](https://github.com/Anchal82-del/TaskDesk-backend) repository:
```bash
# In the TaskDesk-backend terminal:
npm start
```

---

## Running Tests

Run unit tests via Vitest:
```bash
npm test
```

## Linting
```bash
npm run lint
```
