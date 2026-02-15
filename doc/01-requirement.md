# Requirements

## Overview

A full-stack Todo web application built with Go (backend) and Vue 3 (frontend).
The goal is to deliver a production-ready app accessible to real users.

---

## Functional Requirements

### Todo Management

| # | Feature | Description |
|---|---------|-------------|
| F-01 | Create a todo | User can create a new todo with a title |
| F-02 | View todos | User can see a list of all todos |
| F-03 | Complete a todo | User can mark a todo as done / not done |
| F-04 | Delete a todo | User can delete a todo |
| F-05 | Edit a todo | User can update the title of a todo |

### Filtering & Display

| # | Feature | Description |
|---|---------|-------------|
| F-06 | Filter by status | User can filter todos by All / Active / Completed |
| F-07 | Todo count | Display the number of remaining active todos |

---

## Non-Functional Requirements

| # | Category | Requirement |
|---|----------|-------------|
| N-01 | Performance | API response time under 200ms for normal operations |
| N-02 | Availability | Application is publicly accessible via the web |
| N-03 | Security | Input validation on both frontend and backend |
| N-04 | Usability | Responsive design, usable on mobile and desktop |

---

## API Requirements

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/health` | Health check |
| GET | `/api/todos` | Get all todos |
| POST | `/api/todos` | Create a todo |
| PUT | `/api/todos/:id` | Update a todo |
| DELETE | `/api/todos/:id` | Delete a todo |

---

## Data Model

### Todo

| Field | Type | Description |
|-------|------|-------------|
| id | string (UUID) | Unique identifier |
| title | string | Todo text content |
| completed | bool | Completion status |
| created_at | datetime | Creation timestamp |
| updated_at | datetime | Last updated timestamp |

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Go (standard `net/http`) |
| Frontend | Vue 3 + Vite |
| Database | PostgreSQL |

---

## Out of Scope (v1)

- User authentication / accounts
- Due dates and reminders
- Tags or categories
- Collaboration / sharing
