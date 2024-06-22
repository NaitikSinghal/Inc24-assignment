# Inc24 Media - CI/CD Pipelines and Dockerized Applications

## Objective:
This repository demonstrates the implementation of CI/CD pipelines for applications developed using Go, Next.js (TypeScript), PHP (WordPress). Each component has its own dedicated pipeline to enforce coding standards and ensure quality and efficiency.

## Project Structure:
The repository is organized into directories for each component:

- `go-app/`: Contains the Go application.
- `nextjs-app/`: Contains the Next.js application using TypeScript.
- `wordpress-plugin/`: Contains the WordPress plugin.

## Tasks Completed:
### Version Control:
- Created separate public GitHub repositories for each component.
- Initialized repositories (`go-app`, `nextjs-app`, `wordpress-plugin`) with appropriate files.

### Continuous Integration:
- Implemented CI workflows for Go, Next.js (TypeScript), and PHP (WordPress).
- Configured pipelines to trigger on pushes to main and feature branches.
- Integrated linting and unit testing for each technology to enforce coding standards.
- CI pipelines are designed to fail if coding standards or tests are not met.

### Containerization:
- Dockerized the Go application, Next.js (TypeScript) application, and WordPress plugin.
- Created Dockerfiles for each application to build Docker images.
- Pushed Docker images to a container registry (e.g., Docker Hub).

### Coding Standards Enforcement:
- Implemented PHPCS (PHP_CodeSniffer) for the WordPress plugin.
- Configured PHPCS to enforce WordPress coding standards.
- Integrated PHPCS checks into the CI pipeline for the WordPress component.
- Implemented GolangCI-Lint for the Go application.
- Configured GolangCI-Lint to enforce coding standards for Go.
- Integrated GolangCI-Lint checks into the CI pipeline for the Go component.
- Implemented ESLint and Prettier for the Next.js (TypeScript) application.
- Configured ESLint and Prettier to enforce coding standards for TypeScript.
- Integrated ESLint and Prettier checks into the CI pipeline for the Next.js (TypeScript) component.

### Orchestration:
- Updated the `docker-compose.yml` file to include services for Go, Next.js, and WordPress.
- The Docker Compose file can spin up the entire application stack locally.

### Continuous Deployment:
- Extended CI/CD pipelines to include deployment stages for Go, Next.js, and WordPress components.
- Automatic deployment to a staging environment is set up for successful builds.

## Setup Instructions:
To set up and run the extended application locally, follow these steps:

### Prerequisites:
- Docker installed on your local machine.
- GitHub Actions enabled for your repository.

### Steps:
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/NaitikSinghal/inc24-assignment.git

2. **Build Docker Images:**
   ```bash
   docker built -t username/abc:latest
   -please change the username to your own docker username and abc to your image name accordingly

4. **Run Docker Compose:**
   ```bash
   docker-compose up -d

5. **Access Applications:**
   - **Go application:** [http://localhost:8000](http://localhost:8000)
   - **Next.js (TypeScript) application:** [http://localhost:3000](http://localhost:3000)
   - **WordPress site:** [http://localhost:8080](http://localhost:80)
