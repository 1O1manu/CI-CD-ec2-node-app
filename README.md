🚀 CI/CD Pipeline: Node.js Application Deployment to AWS EC2

This project demonstrates a production-style CI/CD pipeline that automates the deployment of a Node.js application to an AWS EC2 instance using GitHub Actions and Docker.

📌 Overview

This system implements a fully automated deployment workflow where every push to the main branch triggers a CI/CD pipeline that builds, transfers, and deploys the application to a remote EC2 server.

The goal is to eliminate manual deployment steps, reduce human error, and ensure consistent and repeatable releases.

🏗️ Architecture
GitHub Repository
        │
        ▼
GitHub Actions (CI/CD Pipeline)
        │
        ├── Build & Test Stage
        ├── Package Application
        │
        ▼
AWS EC2 Instance (Ubuntu Server)
        │
        ├── SSH Deployment
        ├── Docker Build / Node Runtime Execution
        │
        ▼
Running Node.js Application

🧰 Tech Stack
Node.js (Backend runtime)
GitHub Actions (CI/CD automation)
AWS EC2 (Ubuntu Linux server)
Docker (Containerization)
SSH (Secure remote deployment)

✨ Key Features
Fully automated CI/CD pipeline triggered on main branch push
Secure SSH-based deployment to EC2 instance
Docker support for consistent and portable runtime environment
Automated dependency installation and application restart
Production-style deployment workflow
Scalable structure for future enhancements (e.g. testing, staging environments)

📁 Project Structure
client/               # Frontend application (if applicable)
server/               # Node.js backend service
.github/workflows/    # GitHub Actions CI/CD pipeline
Dockerfile            # Container configuration
package.json          # Project dependencies and scripts

🔄 CI/CD Workflow
1. Code Push

A developer pushes changes to the main branch.

2. GitHub Actions Trigger

GitHub Actions automatically triggers the CI/CD pipeline.

3. Build Stage
Dependencies are installed
Application is prepared for deployment
Optional tests can be executed (if configured)

4. Deployment Stage
GitHub Actions connects to the EC2 instance via SSH
Latest code is transferred or pulled on the server
Docker image is built (or Node process prepared)

5. Application Restart
Existing process is stopped
New version is started using Docker or Node runtime (e.g. PM2 or node)

6. Live Deployment

The updated application becomes accessible on the EC2 server endpoint.

▶️ Running Locally
# Clone repository
git clone https://github.com/1O1manu/CI-CD-ec2-node-app.git


# Navigate into project
cd your-repo


# Install dependencies
npm install


# Start server
node server/server.js

☁️ Deployment Details
Hosting Platform: AWS EC2 (Ubuntu)
Deployment Method: GitHub Actions + SSH
Execution Environment: Docker or Node.js runtime
Security: SSH key-based authentication (no password login)

 Deployment Evidence
GitHub Actions successful workflow screenshot: <img width="1152" height="621" alt="Screenshot 2026-05-03 at 09 03 02" src="https://github.com/user-attachments/assets/571c09d0-3259-4f08-a283-7c1e9972c6dd" />

EC2 instance running application
Live endpoint response (optional)

🔧 Potential Improvements (Future Scope)
Add automated testing stage (Jest / Mocha)
Implement staging and production environments
Add rollback strategy for failed deployments
Introduce Nginx reverse proxy for production setup
Add monitoring (PM2 logs / CloudWatch integration)


Built and deployed a fully automated CI/CD pipeline using GitHub Actions and Docker to deploy a Node.js application to AWS EC2 via SSH, enabling zero-manual deployment and production-style release automation.
