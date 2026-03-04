# OpTeamUs – Full Stack Task Management System

## Overview

OpTeamUs is a full-stack project and task management platform similar to Trello or Linear.
It allows users to create workspaces, manage projects, and organize tasks using a Kanban workflow.

The system is built using modern backend and frontend technologies and is fully containerized using Docker.

---

## Tech Stack

### Backend

* ASP.NET Core 8 Web API
* Entity Framework Core
* PostgreSQL
* JWT Authentication
* Swagger API documentation

### Frontend

* React
* TypeScript
* Vite
* Tailwind CSS

### Infrastructure

* Docker
* Docker Compose
* Nginx (frontend container)

---

## Features

* User authentication (JWT)
* Workspace management
* Project management
* Task management with status workflow
* Workspace member invitations
* Kanban-style task tracking
* RESTful API

---

## System Architecture

Frontend (React + Nginx)
⬇
Backend API (ASP.NET Core)
⬇
PostgreSQL Database

All services run in Docker containers.

---

## Running the Application

### Requirements

* Docker
* Docker Compose

### Start the system

From the root project folder run:

```
docker compose up --build
```

### Access the services

Frontend

```
http://localhost:3000
```

Backend API / Swagger

```
http://localhost:8080/swagger
```

---

## Database

PostgreSQL runs in a Docker container and EF Core migrations are automatically applied when the backend starts.

---

## API Authentication

Authentication uses JWT tokens.

1. Register a user
2. Login to receive a token
3. Use the token in Swagger or the frontend

Example header:

```
Authorization: Bearer <token>
```

---

## Project Structure

```
ProjectFiles
│
├── Backend
│   └── OpTeamUs
│
├── Frontend
│   └── OpTeamUs
│
└── docker-compose.yml
```

---

## Notes

The application is designed with a modular architecture separating controllers, services, and data layers to maintain clean architecture and scalability.
