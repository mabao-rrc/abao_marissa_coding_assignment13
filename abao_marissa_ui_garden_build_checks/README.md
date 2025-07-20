# Assignment 13 – UC Component Library

This project is a UI component library built with React and enhanced with automated code quality checks. It includes a pre-commit hook that runs Prettier, ESLint, and unit tests, as well as a GitHub Actions workflow for continuous integration.

## How to Run the App with Docker

### 1. Build the Docker image

docker build -t abao_marissa_coding_assignment13 .

### 2. Run the container

docker run -p 8018:80 abao_marissa_coding_assignment13

### 3. View in your browser

Go to: http://localhost:8018
