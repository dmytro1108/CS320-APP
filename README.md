Project Overview:
We aim to build a Kanban workflow board implemented either as a web application or a desktop app. This document specifies the core requirements and outlines each application. Going forward, we will make a more rigid specification after we decide which platform we prefer to build on. 

Core requirements:
	User Accounts
	Create/delete boards
	Add/edit/delete columns
	Add/edit/delete cards
	Move cards between columns
	Persist data in a SQL database (SQLite3)


Stack: 
  TypeScript Desktop UI + Python Backend API
Desktop UI:
	Electron		Desktop App Shell
	React			UI Components
	TypeScript		Language
	Vite			Dev Server and Build Tooling
Backend:
	Python FastAPI		Backend REST API
	Uvicorn		Server to run FastAPI
	Database:
		SQLite3		Simple Persistent Database for Backend
	Communication:
		Local HTTP/JSON between Electron UI and FastAPI (127.0.0.1:<port>)
