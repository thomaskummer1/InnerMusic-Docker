# InnerMusic Deploy

This repository orchestrates deployment for the InnerMusic project using Docker and Git submodules. It includes:

- 📦 `frontend/` (React client) – Submodule of [InnerMusic-Frontend](https://github.com/thomaskummer1/InnerMusic)
- 🔧 `backend/` (Node.js server) – Submodule of [InnerMusic-Backend](https://github.com/thomaskummer1/InnerMusic-Backend)
- 🐳 `docker-compose.yml` for spinning everything up on one machine

---

## 🧱 Repo Structure

deploy/<br>
├── docker-compose.yml<br>
├── frontend/ ← React frontend (submodule)<br>
├── backend/ ← Node backend (submodule)<br>
└── .gitmodules<br>

## 🚀 Quickstart (Local or EC2)

### 1. Clone this repo with submodules

```bash
git clone --recurse-submodules https://github.com/thomaskummer1/InnerMusic-Deploy.git
cd InnerMusic-Deploy
```

Frontend env:<br>
REACT_APP_REMOTE_SERVER= backend url<br>
REACT_APP_CLIENT_ID= Spotify ID<br>
REACT_APP_CLIENT_SECRET= Spotify Secret<br>

Backend env:<br>
MONGO_CONNECTION_STRING= url for remote atlas db<br>
PORT= current running port<br>
NETLIFY_URL= frontend url<br>

```
docker-compose up --build -d
```
