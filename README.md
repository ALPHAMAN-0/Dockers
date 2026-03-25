# Dockers

A collection of Docker examples for containerizing different frameworks and environments. Each subfolder demonstrates how to write a Dockerfile and docker-compose configuration for a specific technology.

## Examples

### 1. Angular 19

A Dockerized Angular 19 application using a multi-stage build. The first stage builds the Angular app with Node 18, and the second stage serves the production build with Nginx.

- **Build:** `Dockerfile` (multi-stage: Node 18 + Nginx Alpine)
- **Orchestration:** `docker-compose.yml`
- **Run:** `cd "Angular 19/angular-docker-app" && docker-compose up --build`

### 2. React

A Dockerized React application (Create React App) running on Node 20.

- **Build:** `Dockerfile` (Node 20)
- **Run:** `cd React/myapp && docker build -t react-app . && docker run -p 3000:3000 react-app`

### 3. V8 Engine

An Ubuntu-based Docker container configured for V8 JavaScript engine development. Sets up SSH access so you can connect from VS Code via Remote-SSH.

- **Base image:** Ubuntu (latest)
- **Includes:** Git, SSH server, build-essential, Python 3, curl, wget
- **SSH Port:** 2222
- **Run:** `cd "V8 Engine" && docker-compose up --build`, then SSH with `ssh vscode@localhost -p 2222`

### 4. Test Linux OS Connect With VS Code

An Ubuntu-based Docker container designed for remote development with VS Code. Similar to the V8 Engine setup but intended as a general-purpose Linux development environment.

- **Base image:** Ubuntu (latest)
- **SSH Port:** 2223
- **Run:** `cd "Test Linux OS Connect With VS code" && docker-compose up --build`

## Prerequisites

- [Docker](https://www.docker.com/get-started) installed
- [Docker Compose](https://docs.docker.com/compose/install/) installed

## Getting Started

```bash
# Clone the repository
git clone <repo-url>
cd Dockers

# Pick an example and build
cd "Angular 19/angular-docker-app"
docker-compose up --build
```
