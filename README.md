# 😂 XMeme – Full Stack Meme Sharing Platform

**XMeme** is a full-stack meme-sharing application built using **React** (frontend) and **Spring Boot** (backend), featuring **MongoDB** for storage, **Redis** caching, **Docker** containerization, and **infinite scroll pagination** for a modern user experience.  

This project is designed to showcase **full-stack development, REST API integration, state management, responsive UI, caching, and containerization**

---

## Table of Contents

- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Architecture](#architecture)  
- [Setup Instructions](#setup-instructions)  
- [Usage](#usage)  
- [Docker Deployment](#docker-deployment)    
- [Future Enhancements](#future-enhancements)  

---

## Features

- **Meme Management**
  - Post memes with name, caption, and image URL  
  - View latest memes with infinite scroll  
  - View individual memes by ID  
- **Caching Optimization**
  - Redis caching for frequently accessed memes  
  - Faster response time and reduced DB hits  
- **Professional UI**
  - Responsive design with **React Bootstrap**  
  - Navbar, card-based meme feed, and alert notifications  
- **Routing**
  - Smooth client-side navigation with **React Router DOM**  
- **Validation & Error Handling**
  - Form validations and proper HTTP status codes  

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React.js, React Bootstrap, React Router DOM, Axios |
| Backend | Java, Spring Boot, Spring MVC, Spring Data MongoDB, Spring Cache |
| Database | MongoDB |
| Caching | Redis |
| Containerization | Docker, Docker Compose |
| Testing | Mockito (backend) |
| API Docs | Swagger (OpenAPI) |

---

## Architecture

```
Frontend (React) <--> Backend (Spring Boot REST APIs) <--> MongoDB & Redis
```

- **Frontend**
  - SPA using React  
  - Components: Navbar, MemeCard, MemeForm  
  - Pages: Home (latest memes), Create Meme  
  - Infinite scroll for meme feed  
- **Backend**
  - MVC layered architecture: Controller → Service → Repository → Model  
  - REST APIs: POST /memes, GET /memes, GET /memes/{id}  
  - Redis caching at service layer  
- **Database**
  - MongoDB stores meme documents (name, caption, URL, timestamp)  
- **Containerization**
  - Dockerized frontend and backend  
  - Orchestrated via Docker Compose with MongoDB and Redis  

---

## Setup Instructions

### Prerequisites

- Java 17+  
- Node.js 18+  
- MongoDB  
- Redis  
- Docker & Docker Compose  

### Backend Setup

1. Navigate to backend folder:
```bash
cd backend
```
2. Build the Spring Boot app:
```bash
./gradlew build
```
3. Run the backend:
```bash
./gradlew bootRun
```
4. Backend will be available at:
```
http://localhost:8080
```

### Frontend Setup

1. Navigate to frontend folder:
```bash
cd xmeme-frontend
```
2. Install dependencies:
```bash
npm install
```
3. Run the frontend:
```bash
npm start
```
4. Frontend will be available at:
```
http://localhost:3000
```

---

## Docker Deployment

All components (frontend, backend, MongoDB, Redis) are containerized.

1. Navigate to project root:
```bash
docker-compose up --build
```
2. Access services:
- Frontend → `http://localhost:3000`  
- Backend → `http://localhost:8080`  
- MongoDB → `localhost:27017`  
- Redis → `localhost:6379`  

---

## Usage

- **Home Page** → Browse latest memes (infinite scroll)  
- **Create Meme** → Submit a new meme with name, caption, and image URL  
- **Meme Details** → Click a meme (if implemented) to view details  

---

## Future Enhancements

- JWT-based authentication  
- Like/Comment system for memes  
- Pagination with page numbers  
- Image upload support instead of URLs  
- Deployment on cloud (AWS/GCP/Azure)  

---

### Developed by

**Prathamesh Kumbhar**  
Java Full Stack Web Developer
