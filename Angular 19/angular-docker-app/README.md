# Angular Docker Application

This project is an Angular application configured to run in a Docker container. Below are the instructions for setting up and running the application.

## Prerequisites

- Docker installed on your machine
- Docker Compose installed on your machine
- Node.js and npm (for local development)

## Project Structure

The project consists of the following main directories and files:

- `src/`: Contains the source code of the Angular application.
  - `app/`: Contains the main application components and routing.
  - `assets/`: Contains static assets like images and fonts.
  - `environments/`: Contains environment-specific configuration files.
  - `index.html`: The main HTML file for the application.
  - `main.ts`: The entry point for bootstrapping the Angular application.
  - `styles.css`: Global styles for the application.
  
- `.vscode/`: Contains configuration files for the development environment.
  
- `Dockerfile`: Instructions for building the Docker image.
  
- `docker-compose.yml`: Configuration for running the application in Docker.
  
- `package.json`: Lists dependencies and scripts for the application.
  
- `README.md`: Documentation for the project.

## Getting Started

1. Clone the repository:
   ```
   git clone <repository-url>
   cd angular-docker-app
   ```

2. Build the Docker image:
   ```
   docker build -t angular-docker-app .
   ```

3. Run the application using Docker Compose:
   ```
   docker-compose up
   ```

4. Access the application in your browser at `http://localhost:4200`.

## Development

To run the application locally without Docker, follow these steps:

1. Install dependencies:
   ```
   npm install
   ```

2. Start the development server:
   ```
   ng serve
   ```

3. Open your browser and navigate to `http://localhost:4200`.

## Testing

To run unit tests, use the following command:
```
ng test
```

## Build

To build the application for production, run:
```
ng build --prod
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.