# Kanban Desktop App

A desktop Kanban board application built with Electron, React, and TypeScript.

## Features
- User account management
- Create and delete boards
- Add, edit, and delete columns
- Add, edit, and delete cards
- Move cards between columns
- Local SQLite database for data persistence

## Technologies

### Frontend
- **Electron** — Desktop application framework
- **React** — UI component library
- **TypeScript** — Type-safe JavaScript
- **Vite** — Build tool and dev server

### Database
- **SQLite3** — Embedded SQL database (via better-sqlite3)

## Project Structure
```
src/
├── main/               # Electron main process (Node.js environment)
│   ├── main.ts         # Application entry point, window management
│   ├── database.ts     # SQLite database operations
│   └── ipc-handlers.ts # IPC message handlers
│
├── renderer/           # React UI (Browser environment)
│   ├── App.tsx         # Root React component
│   ├── components/     # Board, Column, Card components
│   └── index.html      # HTML entry point
│
└── preload/            # Security bridge
    └── preload.ts      # Exposes safe IPC APIs to renderer
```

## Architecture

The app uses Electron's multi-process architecture with IPC communication:
```
React UI (renderer process)
        ↓ IPC
Electron Main Process
        ↓
SQLite Database
        ↑
Electron Main Process
        ↑ IPC
React UI (renderer process)
```

## Getting Started

[Installation and development instructions to be added]
