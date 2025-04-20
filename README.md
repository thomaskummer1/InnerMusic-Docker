# InnerMusic Deploy

This repository orchestrates deployment for the InnerMusic project using Docker and Git submodules. It includes:

- 📦 `frontend/` (React client) – Submodule of [InnerMusic-Frontend](https://github.com/your-username/InnerMusic-Frontend)
- 🔧 `backend/` (Node.js server) – Submodule of [InnerMusic-Backend](https://github.com/your-username/InnerMusic-Backend)
- 🐳 `docker-compose.yml` for spinning everything up on one machine

---

## 🧱 Repo Structure

deploy/
├── docker-compose.yml
├── frontend/ ← React frontend (submodule)
├── backend/ ← Node backend (submodule)
└── .gitmodules

## 🚀 Quickstart (Local or EC2)

### 1. Clone this repo with submodules

```bash
git clone --recurse-submodules https://github.com/thomaskummer1/InnerMusic-Deploy.git
cd InnerMusic-Deploy
```

Frontend env:
REACT_APP_REMOTE_SERVER= backend url
REACT_APP_CLIENT_ID= Spotify ID
REACT_APP_CLIENT_SECRET= Spotify Secret

Backend env:
MONGO_CONNECTION_STRING= url for remote atlas db
PORT= current running port
NETLIFY_URL= frontend url

```
docker-compose up --build -d
```
