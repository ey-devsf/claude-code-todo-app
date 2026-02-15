# Frontend Design

## Screen Overview

The app is a single-page application (SPA) with one main screen — the Todo list view.

No routing is needed for v1. All functionality lives on a single page.

---

## Component Structure

```
App
├── TodoInput        # Text input + add button
├── TodoFilter       # Filter tabs: All / Active / Completed
├── TodoList         # Container for todo items
│   └── TodoItem     # Single todo (checkbox, title, edit, delete)
└── TodoCount        # "X items left" counter
```

---

## Layout

- Centered single-column layout (max-width ~640px)
- Mobile-first responsive design
- Input at the top, list below, filter and count at the bottom

---

## Tech Choices

| Category | Choice |
|----------|--------|
| Framework | Vue 3 (Composition API, `<script setup>`) |
| Build tool | Vite |
| Styling | Tailwind CSS |
| State management | Vue `ref` / `reactive` (no Pinia needed for v1) |
| HTTP client | `fetch` API |

---

## UI Flow

1. User types a todo title in the input and presses Enter or clicks Add
2. The new todo appears in the list
3. User clicks the checkbox to mark a todo as completed
4. User can edit the title by double-clicking
5. User can delete a todo with the delete button
6. User can filter the list by All / Active / Completed
7. The counter shows the number of remaining active todos
