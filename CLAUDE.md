# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## Project Overview

Full-stack todo app monorepo with a Go backend and Vue 3 frontend.

This project is not only for building a Todo app, but also for mastering Claude Code through real-world development and releasing a production-ready application accessible to real users.

The final goal is:
- Deploy the application to the web
- Make it publicly accessible
- Gain hands-on experience in full-stack architecture, deployment, and DevOps
- Improve English skills by using English only during development discussions

---

## Development Philosophy & Project Goals

### 🎯 Purpose

- Master Claude Code in a practical workflow
- Learn how to release a web application to production
- Improve English through technical communication
- Treat this as a real product, not a demo

### 🧠 Developer Background

- Salesforce engineer
- Native Japanese speaker
- Currently studying English (CEFR A2 → aiming for B1)
- No prior experience releasing standalone web/native apps publicly
- Budget is not a constraint (infrastructure investment is acceptable)

### 📌 Communication Rules

- All discussions must be conducted in English
- If English is incorrect, correct it before answering
- Do not provide correction and answer simultaneously
- Wait for the corrected question before answering

---

## Commands

### Backend (`backend/`)
```bash
go run ./cmd/api/main.go      # Run the API server (port 8080)
go build -o api ./cmd/api/    # Build binary
go test ./...                 # Run all tests
```

### Frontend (`frontend/`)
```bash
npm run dev       # Start Vite dev server with HMR
npm run build     # Production build
npm run preview   # Preview production build
```

---

## Architecture

- **backend/**: Go API server using standard `net/http`. Entry point at `cmd/api/main.go`. Health check endpoint at `GET /health`. Uses Go module `github.com/ey-devsf/claude-code-todo-app`.
  - `cmd/api/` — server entry point
  - `api/` — API route handlers (to be built out)
  - `internal/` — internal packages for business logic, models

- **frontend/**: Vue 3 SPA built with Vite. Uses `<script setup>` syntax and Composition API.
  - `src/main.js` — app initialization, mounts to `#app`
  - `src/App.vue` — root component

Frontend and backend are not yet connected (no API calls, no CORS configuration).

---

## Future Production Considerations

To reach production-level quality, the following must eventually be addressed:

- Environment configuration (.env management)
- CORS configuration
- Logging strategy
- Database selection and schema design
- Dockerization
- CI/CD pipeline
- Hosting (e.g., Vercel / Railway / Fly.io / VPS)
- Monitoring and error tracking
- Security best practices

This is not just a coding exercise — this repository should evolve into a real, deployable product.
