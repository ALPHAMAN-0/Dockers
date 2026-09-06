# CLAUDE.md — Dockers

## Build / run (from README.md — no npm/test/lint scripts observed)
- Angular 19: `cd "Angular 19/angular-docker-app" && docker-compose up --build`
- React: `cd React/myapp && docker build -t react-app . && docker run -p 3000:3000 react-app`
- V8 Engine: `cd "V8 Engine" && docker-compose up --build` (then `ssh vscode@localhost -p 2222`)
- Test Linux OS Connect With VS Code: `cd "Test Linux OS Connect With VS code" && docker-compose up --build`
- No test or lint commands found in any file read for this repo.

## Rules
- Several top-level folder names contain spaces ("Angular 19", "Test Linux OS Connect With VS code") — always quote these paths in shell commands.
- Each example folder is self-contained (own Dockerfile / docker-compose.yml); no shared root-level manifest or config.

## Read first
- README.md
- ARCHITECTURE.md
- Angular 19/angular-docker-app/README.md

Architecture: see ARCHITECTURE.md — read before structural changes
