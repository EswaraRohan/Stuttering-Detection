# Stuttering Detection Platform

## Overview
The **Stuttering Detection Platform** is a web-based application aimed at detecting stuttering in speech. The project integrates Artificial Intelligence (AI) and Signal Processing techniques to analyze speech patterns. The primary goal is to provide a tool that can be used in medical settings to assist professionals in diagnosing and monitoring speech disorders.

## Features
- **Bilingual Support**: Supports both English and Kannada.
- **User-friendly Deployment**: Simplified Docker container management for non-technical users.
- **Secure and Scalable**: Uses JWT authentication and MongoDB for data management.
- **Seamless Web Interface**: Developed using React for a dynamic and responsive UI.
- **Backend Integration**: FastAPI and Flask are used to process and analyze speech data.

## Tech Stack
- **Frontend**: React.js
- **Backend**: FastAPI & Flask
- **Database**: MongoDB
- **Authentication**: JWT-based authentication
- **Containerization**: Docker

## Installation & Setup
### Prerequisites
Ensure you have the following installed:
- Docker
- Node.js & npm/yarn
- Python 3.x

### Steps to Run Locally
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/stuttering-detection.git
   cd stuttering-detection
   ```
2. Build and run the backend:
   ```sh
   cd backend
   pip install -r requirements.txt
   uvicorn main:app --reload
   ```
3. Start the frontend:
   ```sh
   cd frontend
   npm install
   npm start
   ```
4. Run the project using Docker:
   ```sh
   docker-compose up --build
   ```

## Deployment
The project has been deployed on **AIISH’s** internal server using Docker. The deployment involves:
- Setting up a **private IP** to comply with AIISH’s security policies.
- Using **Nginx** for server routing.
- **SSL Encryption** for secure communication.
- Handling **port configurations** to avoid conflicts with existing services.

## Challenges Faced
- **SSL Certificate Expiry**: The project was initially deployed with SSL but is currently running on a local server due to certificate expiration.
- **DNS Conflicts**: Encountered conflicts between Docker’s embedded DNS and AIISH’s server DNS.
- **Timeout Issues**: `yarn install` faced network timeouts during deployment, requiring network configuration fixes.

## Future Enhancements
- **Automated Test ID Generation** to uniquely identify test sessions.
- **Enhanced Search**: Implement search by patient name or ID.
- **Full SSL Integration**: Secure deployment with a persistent SSL certificate.
- **Routine Security Audits**: Implement regular security checks to ensure data safety.
