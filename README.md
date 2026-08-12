⚖️ PrimeLegal - Legal Consultation Platform
Welcome to PrimeLegal, a comprehensive, secure, and intuitive web application designed to bridge the gap between legal professionals and clients seeking legal advice.

This repository contains the complete source code for both the Spring Boot Backend and the React + Vite Frontend.

🌟 Project Overview
PrimeLegal modernizes the legal consultation process. It replaces fragmented emails and phone calls with a centralized portal where clients can find specialized attorneys, book appointments, securely exchange messages, and manage legal documents. The platform features a strict Role-Based Access Control (RBAC) system, ensuring customized and secure experiences for Clients, Lawyers, and Administrators.

✨ Key Features
👤 For Clients (Users)
Lawyer Directory: Search and filter attorneys by specialization, minimum rating, and maximum hourly fee.

Appointment Booking: Schedule consultations picking available dates, times, and providing case notes.

Secure Messaging: Real-time chat interface to communicate directly with connected lawyers.

Document Management: Upload and store case-related files securely.

Account Settings: Manage profile details, notifications, and preferred consultation modes (Video, Phone, In-Person).

💼 For Lawyers
Practice Dashboard: View upcoming consultations, pending requests, and unread messages at a glance.

Schedule Management: Accept, reject, or mark appointments as completed with one click.

Client Directory: Access a consolidated list of active clients and case purposes.

Practice Settings: Dynamically update hourly rates, specializations, and automated notification preferences.

🛡️ For Administrators
System Controls: Configure platform-wide rules, commission rates, and maintenance modes.

User Management: Suspend, activate, or remove user and lawyer accounts.

Lawyer Onboarding: Manually add verified attorneys to the platform directory.

🎨 Global Features
Dynamic Theme: Seamless Dark/Light mode toggle that remembers user preferences via local storage.

Responsive Design: Fully mobile-optimized interface using Tailwind CSS.

Real-time Notifications: Polling-based notification system to alert users of status changes and new messages.

🛠️ Technology Stack
Frontend (Client-Side)
Framework: React 18 with Vite for blazing-fast builds.

Styling: Tailwind CSS (with native Dark Mode support).

Routing: React Router v6 for Single Page Application (SPA) navigation.

State Management: React Context API (AuthContext, ThemeContext).

HTTP Client: Axios for API requests.

Backend (Server-Side)
Framework: Java 21 & Spring Boot 3.2.0.

Data Access: Spring Data JPA & Hibernate.

Security: Spring Security & Custom CORS Configuration.

Database: MySQL (Cloud-hosted via Aiven).

Build Tool: Maven.

Deployment Architecture
Frontend Hosting: Netlify (with custom _redirects for SPA routing).

Backend Hosting: Render (Containerized via Docker, utilizing Debian/Ubuntu base images for network stability).

🚀 Getting Started (Local Development)
To run PrimeLegal on your local machine, follow these steps:

Prerequisites
Node.js (v18+)

Java Development Kit (JDK 21)

MySQL Server (Local or Cloud)

1. Database Setup
Create a new MySQL database for the project:

SQL
CREATE DATABASE primelegal_db;
2. Backend Setup
Navigate to the backend directory and configure your environment variables. You can set these in your IDE or add them directly to src/main/resources/application.properties for local testing:

Properties
# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/primelegal_db
spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# Hibernate Configuration
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect
spring.jpa.hibernate.ddl-auto=update

# Server Port
server.port=8080
Run the application using Maven:

Bash
./mvnw spring-boot:run
3. Frontend Setup
Navigate to the frontend directory (frontend/). Create a .env file in the root of the frontend folder:  

Code snippet
VITE_API_URL=http://localhost:8080/api
Install dependencies and start the development server:  

Bash
npm install
npm run dev
Access the application at http://localhost:5173.
