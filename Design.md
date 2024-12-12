# Software Design Description (SDD)

## 1. Introduction

### 1.1 Purpose
The purpose of this **Software Design Description (SDD)** is to provide a detailed design for the **Byju's Competitor system**, covering architecture, components, and interactions.

### 1.2 Scope
The **Byju's Competitor System** is an **online learning platform** that enables:
- **Students**: Access courses, join live classes, and track progress.
- **Tutors**: Upload content, schedule live classes, and manage Q&A.
- **Admins**: Manage users, content, and platform analytics.

---

## 2. System Overview
### 2.1 Components
- **Student App**:  
  - Registration/Login  
  - Course Access  
  - Video Playback  
  - Live Classes  
  - Payment Gateway Integration  
  - Progress Tracking  

- **Tutor Portal**:  
  - Registration  
  - Content Upload  
  - Scheduling Live Classes  
  - Managing Q&A  

- **Admin Dashboard**:  
  - User Management  
  - Content Approval  
  - Analytics and Reporting  

---

## 3. Architecture Design

### 3.1 Architecture Components
- **Student App**: Provides course catalog, live classes, and profile management.
- **Tutor Portal**: Allows content upload, class scheduling, and interactions.
- **Admin Dashboard**: Offers user management, content approval, and analytics.

### 3.2 Backend Services
- **Authentication**: Secure login and token-based user authentication.  
- **Content Management**: Upload and manage courses and study materials.  
- **Live Class Management**: Schedule classes and enable real-time interaction.  
- **Payment Integration**: Handle payments and refunds via external gateways.  
- **Notification Service**: SMS and email alerts for reminders, payments, and updates.

### 3.3 Databases
 **The Byju's Clone system uses a NoSQL database (e.g., MongoDB). Below is the database schema for major entities**.
 
![Byjus_Clone_Database_Schema (1)](https://github.com/user-attachments/assets/f0727cc8-f3f6-421a-b655-dd9f2290d2b2)
- **PostgreSQL**: For structured data like user profiles, courses, and payments.  
- **Redis**: For caching real-time data like class schedules.

### 3.4 External APIs
- **Video Conferencing API**: Enable live classes and student-tutor interaction.  
- **Payment Gateway**: Secure subscription payments and refunds.  
- **Notification Gateway**: SMS/email notifications (e.g., Twilio).

### 3.5 Infrastructure
- **Cloud Hosting**: AWS or Google Cloud for backend and content delivery.  
- **Load Balancer**: Distribute traffic and ensure availability.  
- **Monitoring Tools**: Prometheus and Grafana for performance metrics.  
- **CI/CD Pipeline**: Automated deployments using GitHub Actions or Jenkins.

---

## 4. Module Design

### 4.1 Mobile Application
- **Student App**:  
  - Course catalog, payment processing, live classes, and profile management.  
- **Tutor Portal**:  
  - Upload content, manage schedules, and interact with students.  

### 4.2 Backend System
- **API Gateway**: Manages app requests and routes them to backend services.  
- **Authentication Service**: Handles registration, login, and password recovery.  
- **Content Service**: Manages course uploads, retrieval, and student progress tracking.  
- **Live Class Service**: Schedules classes and manages real-time interaction.  
- **Payment Service**: Handles payments and transaction records.  
- **Notification Service**: Sends class reminders and updates via SMS and email.

---

## 5. Database Design
- **Users Table**: Stores details like name, email, and role (student/tutor).  
- **Courses Table**: Stores course information, study materials, and descriptions.  
- **Payments Table**: Tracks payment transactions, including subscription plans.  
- **Live Classes Table**: Stores schedules, tutor details, and attendee records.

---

## 6. Interface Design

### 6.1 API Endpoints
- **`/auth/register`**: Register a new user.  
- **`/auth/login`**: Authenticate user and issue tokens.  
- **`/courses`**: Fetch available courses.  
- **`/courses/{id}`**: Fetch course details.  
- **`/payments/subscribe`**: Initiate a subscription.  
- **`/live-classes/schedule`**: Schedule live classes (tutor only).  

### 6.2 External Interfaces
- **Video API**: For hosting live classes.  
- **Payment Gateway**: For secure transactions.  
- **Notification Gateway**: For sending reminders and updates.

---

## 7. Non-Functional Requirements
- **Performance**: Handle up to 100,000 concurrent users.  
- **Scalability**: Backend must scale horizontally to handle peak loads.  
- **Availability**: Ensure 99.9% uptime with redundancy.  
- **Security**: Use HTTPS and encrypt sensitive data.

---

## 8. Conclusion
This design ensures a **robust, scalable, and secure** system for delivering online learning experiences. Modular design and integration with external services allow effective management of courses, payments, and live classes.

