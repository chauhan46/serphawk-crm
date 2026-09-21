# SERP Hawk CRM V2

AI-Powered CRM for SEO Agencies built with Next.js, FastAPI, PostgreSQL, and Docker.

## Overview

SERP Hawk CRM V2 is a customer relationship management application designed for SEO agencies and digital marketing teams.

The application provides functionality for client management, projects, tasks, communication, email activities, SEO-related operations, document management, and reporting.

The application has been containerized using Docker and deployed on Amazon EC2.

## Live Application

Deployed Application:

http://52.207.218.248:3000

Deployment Platform: AWS EC2

Containerization: Docker and Docker Compose

Architecture:

Next.js Frontend → FastAPI Backend → PostgreSQL Database

---

## Key Features

- Role-Based Access Control
- Admin, Employee, Intern, and Client roles
- Client management
- Project management
- Task management
- AI Email Agent
- Real-Time Messaging
- Service Management
- Quotes and Invoicing
- SEO Keyword Ranking
- Competitor Analysis
- SEO Audits
- Document Management
- File Uploads
- Reporting and Dashboards

---

## Technology Stack

### Frontend

- Next.js
- React
- TypeScript
- Tailwind CSS
- Framer Motion

### Backend

- Python
- FastAPI
- SQLModel
- Uvicorn
- WebSocket

### Database

- PostgreSQL

### Containerization

- Docker
- Docker Compose

### Cloud

- Amazon EC2
- Amazon EBS
- EC2 Security Groups

### Source Control

- Git
- GitHub

---

# AWS Deployment Architecture

The application is deployed on an Amazon EC2 instance using Docker and Docker Compose.

## AWS Services Used

### Amazon EC2

Amazon EC2 is used as the compute platform for hosting the CRM application.

The EC2 instance runs the Docker containers for the frontend, backend, and PostgreSQL database.

### Amazon EBS

The EC2 instance uses Amazon EBS storage for its root volume and application storage.

### EC2 Security Group

The Security Group controls inbound network access to the EC2 instance.

The deployment uses the following ports:

- SSH - TCP 22
- Frontend - TCP 3000
- Backend - TCP 8000

### Docker

Docker is used to containerize the application components:

- Next.js frontend
- FastAPI backend
- PostgreSQL database

### Docker Compose

Docker Compose is used to create and manage the application containers and their networking.

---

## Application Architecture

```text
                         Internet
                            |
                            v
                    +---------------+
                    |   AWS EC2     |
                    |               |
                    | Security Group|
                    +-------+-------+
                            |
                            v
                  +---------------------+
                  |       Docker        |
                  |                     |
                  |  +---------------+  |
                  |  | Next.js       |  |
                  |  | Frontend      |  |
                  |  | Port 3000     |  |
                  |  +-------+-------+  |
                  |          |          |
                  |          v          |
                  |  +---------------+  |
                  |  | FastAPI       |  |
                  |  | Backend       |  |
                  |  | Port 8000     |  |
                  |  +-------+-------+  |
                  |          |          |
                  |          v          |
                  |  +---------------+  |
                  |  | PostgreSQL    |  |
                  |  | Database      |  |
                  |  | Port 5432     |  |
                  |  +---------------+  |
                  +---------------------+
                            |
                            v
                         EBS Storage