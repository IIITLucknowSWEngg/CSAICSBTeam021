# Software Requirements Specification (SRS) for Byju's competitor 

## 1. Introduction

### 1.1 Purpose
This Software Requirements Specification (SRS) document provides a detailed description of the functional and non-functional requirements for the Byju's competitor  application. The document serves as a guideline for developers, testers, and stakeholders throughout the software development lifecycle, ensuring the application meets the expectations and goals defined for the project.

### 1.2 Scope
The Byju’s Competitor  application is an e-learning platform designed to offer a seamless learning experience through video-based lessons, live classes, quizzes, and progress tracking. The platform will serve students, educators, and administrators. It will allow students to enroll in courses, track progress, attend live classes, and participate in quizzes. Educators will have tools to upload content, create live sessions, and monitor student engagement. Admins will manage user accounts, courses, and the system’s overall functionality. This SRS defines the features and constraints of the application.

This document covers:
- User interfaces
- Functional requirements
- Non-functional requirements
- External interfaces and communication protocols

### 1.3 Definitions, Acronyms, and Abbreviations
- **SRS**: Software Requirements Specification
- **LMS**: Learning Management System
- **UI**: User Interface
- **API**: Application Programming Interface
- **AI**: Artificial Intelligence
- **NFT**: Non-Functional Requirement
- **GDPR**: General Data Protection Regulation
- **REST**: Representational State Transfer
- **SSL**: Secure Socket Layer
- **JWT**: JSON Web Token
- **SDK**: Software Development Kit

### 1.4 References
- [Stakeholders.md](https://github.com/IIITLucknowSWEngg/CSAICSBTeam021/edit/main/Stakeholders.md)
- [User Requirements Document](https://github.com/IIITLucknowSWEngg/CSAICSBTeam021/edit/main/URD.md)
- IEEE Std 830-1998, IEEE Recommended Practice for Software Requirements Specifications
- SWEBOK v3.0, Software Engineering Body of Knowledge

### 1.5 Overview
This document is organized into the following sections:
- Section 1: Introduction
- Section 2: Overall Description of the system
- Section 3: Detailed System Features
- Section 4: External Interface Requirements
- Section 5: Non-Functional Requirements (NFRs)
- Section 6: Other Requirements (Localization, Ethical)

---

## 2. Overall Description

### 2.1 Product Perspective
The Byju's Competitor  application is designed to be a standalone platform that operates across both mobile and web devices. The application will interface with third-party services for payment processing, video hosting, and live class streaming. The system will be designed with modular architecture to support scalability and ease of maintenance. The backend will be hosted on cloud servers to ensure high availability.

### 2.2 Product Functions
The application will provide the following functions:
- User registration and authentication
- Course browsing, enrollment, and management
- Video-based learning and live classes
- Quiz creation and performance tracking
- Payment processing for course subscriptions
- Progress tracking and analytics for both students and educators
- In-app communication between students and educators
- Personalized recommendations powered by AI

### 2.3 User Classes and Characteristics
The Byju’s Competitor  application will support the following user roles:
- **Students**: Individuals who use the platform to access educational content and track their learning progress.
- **Educators**: Teachers or instructors who create and manage courses, quizzes, and live classes.
- **Admins**: Users who oversee the entire system, manage courses, users, and monitor system performance.

### 2.4 Operating Environment
The Byju’s Competitor  application will operate on Android and iOS mobile platforms as well as web browsers. The system will require an active internet connection for video streaming, live sessions, payment processing, and real-time updates. The backend will be hosted on cloud infrastructure (e.g., AWS, Google Cloud) to provide scalability and high availability.

### 2.5 Design and Implementation Constraints
- The system must comply with data protection regulations, including **GDPR**.
- The application will need to function on mobile devices with varying hardware and software specifications.
- Integration with third-party services for payment gateways, video hosting, and live class streaming.
- The initial version will support English and a limited set of course categories.

### 2.6 Assumptions and Dependencies
- Users are assumed to have access to smartphones or computers with stable internet connections.
- The system will be dependent on third-party APIs for live class streaming, video hosting, and payment processing.
- Initial language support will be English, with plans to localize for other languages in future versions.

---

## 3. System Features

### 3.1 User Registration and Authentication
#### Description:
Users (students and educators) can register on the platform using their email, phone number, or social media accounts (e.g., Google, Facebook). The system will support secure login and password recovery features.

#### Functional Requirements:
- The system shall allow users to register using email or phone number.
- The system shall send a verification code to the user for account activation.
- The system shall allow users to reset their password via email or SMS.
- The system shall store passwords securely using encryption (e.g., bcrypt).

### 3.2 Course Management
#### Description:
Students will be able to browse, search, and enroll in courses, while educators can create and manage their courses.

#### Functional Requirements:
- The system shall allow students to search and filter courses by subject, category, or instructor.
- The system shall display detailed course information, including syllabus, lessons, and quizzes.
- The system shall allow educators to upload course materials (videos, PDFs, assignments) and create quizzes.
- The system shall enable students to track their progress in each course.

### 3.3 Video-Based Learning & Live Classes
#### Description:
The system will provide students with video-based learning resources and enable live classes hosted by educators.

#### Functional Requirements:
- The system shall stream video lessons with adaptive quality based on the user’s internet speed.
- The system shall allow educators to host live classes with video/audio streaming.
- The system shall allow students to ask questions during live sessions via chat.
- The system shall record live sessions for later access by students.

### 3.4 Quiz Creation and Performance Tracking
#### Description:
Educators can create quizzes for their courses, and students can take quizzes to assess their learning.

#### Functional Requirements:
- The system shall allow educators to create quizzes with multiple question types (e.g., multiple-choice, short answer).
- The system shall automatically grade quizzes and display results to students.
- The system shall allow students to review their quiz performance, including correct/incorrect answers.
- The system shall store student quiz results and track progress over time.

### 3.5 Payment Processing
#### Description:
Students can purchase courses via various payment methods, and the system will process payments and maintain transaction history.

#### Functional Requirements:
- The system shall support multiple payment methods, including credit/debit cards, wallets, and subscriptions.
- The system shall automatically process payments after course enrollment.
- The system shall maintain a payment history for students and educators.
- The system shall generate invoices for each successful transaction.

### 3.6 Personalized Recommendations (AI)
#### Description:
The system will use AI to provide personalized course recommendations based on students' preferences, learning behavior, and past activity.

#### Functional Requirements:
- The system shall track student activity and learning preferences.
- The system shall suggest courses based on past enrollments, progress, and quiz performance.
- The system shall allow students to opt-in to receive personalized recommendations.

### 3.7 Rating and Review System
#### Description:
Students can rate and review courses and educators based on their experience.

#### Functional Requirements:
- The system shall allow students to rate courses on a 5-star scale.
- The system shall allow students to leave reviews for courses and instructors.
- The system shall allow educators to view ratings and feedback on their courses.

---

## 4. External Interface Requirements

### 4.1 User Interfaces
- **Mobile Application (Android & iOS)**: The UI will be responsive, with easy-to-navigate sections for course browsing, video learning, live classes, and profile management.
- **Admin Panel**: A web-based admin dashboard for managing courses, users, payments, and generating reports.

### 4.2 Hardware Interfaces
- **Mobile Devices**: The system will interact with device hardware, including cameras for profile photos and microphone/speakers for live class participation.
- **Internet Connectivity**: Required for streaming videos, live classes, and real-time updates.

### 4.3 Software Interfaces
- **Third-Party APIs**: The system will integrate with APIs for video hosting (e.g., YouTube, Vimeo), payment gateways (e.g., Stripe, Razorpay), and SMS services (e.g., Twilio).
- **Database**: The application will use a NoSQL database (e.g., MongoDB) to store course information, user profiles, and transactional data.

### 4.4 Communication Interfaces
- **HTTPS**: All communications between the app and backend will be secured using HTTPS.
- **WebSocket**: Real-time updates for live classes, quiz results, and chat will be handled via WebSocket.

---

## 5. Non-Functional Requirements (NFRs)

### 5.1 Performance Requirements
- The system must load the homepage within 3 seconds on stable internet connections.
- Video streaming must be seamless, with adaptive quality to match user bandwidth.
- Ride requests should be processed in less than 5 seconds.

### 5.2 Security Requirements
- All user data shall be encrypted both at rest and in transit using SSL/TLS.
- The system shall support multi-factor authentication for users and educators.
- Regular security audits shall be conducted to ensure system integrity.

### 5.3 Availability and Reliability
- The system must have an uptime of 99.7%, excluding scheduled maintenance.
  <img width="809" alt="Screenshot 2024-12-04 at 7 31 31 PM" src="https://github.com/user-attachments/assets/cdd2e89e-ead6-47ec-abf0-ab1b193df3c5">

- The system must handle up to 50,000 concurrent users without performance degradation.
- Data backups shall be taken every 24 hours to ensure data recovery.

### 5.4 Scalability
- The system architecture shall support horizontal scaling for future growth in user base and features.
- The system shall support the addition of new course categories, languages, and payment options.

### 5.5 Usability
- The user interface shall be intuitive, with a focus on ease of navigation for students and educators.
- The app shall support accessibility features, following WCAG 2.1 guidelines.

### 5.6 Maintainability
- The system codebase shall be modular, supporting easy updates and bug fixes.
- The system shall support automated testing to catch issues early.

---

## 6. Other Requirements

### 6.1 Localization
The application will support localization to enable use in different regions with minimal changes, allowing for future language and regional currency support.

### 6.2 Ethical Requirements
The system will include features to prevent misuse, such as content moderation and reporting mechanisms for inappropriate behavior by educators or students.

---

# Use-Case Diagram for Byju's Competitor

The following diagram represents the primary use cases and interactions in the Byju's Competitor application. The main actors (Students, Educators, and Admins) interact with various use cases to perform their roles in the system.

## Actors

1. **Student**: A user who uses the app to access educational content, track their progress, and engage in learning activities.
2. **Educator**: A user who creates and manages courses, conducts live classes, and evaluates student performance.
3. **Admin**: A user who manages the overall platform, including users, courses, and system performance.

---

## Use Cases

### 1. **Student Use Cases**
- **Register and Authenticate**: The student registers on the platform using their email, phone number, or social accounts. They can log in and recover their password.
- **Browse and Enroll in Courses**: The student can browse available courses, search for specific subjects, and enroll in the courses of their choice.
- **Watch Video Lessons**: The student watches pre-recorded video lessons as part of the course content.
- **Attend Live Classes**: The student can attend live classes conducted by educators for real-time learning.
- **Take Quizzes**: The student can take quizzes related to the courses they have enrolled in to assess their understanding.
- **View Progress**: The student can track their progress in terms of completed lessons, quiz scores, and course milestones.
- **Make Payments**: The student can make payments for the courses they have enrolled in using different payment methods.

### 2. **Educator Use Cases**
- **Register and Authenticate**: The educator registers and logs into the platform, with the option to reset their password if necessary.
- **Create and Manage Courses**: The educator creates new courses, adds video lessons, quizzes, and other materials, and manages existing courses.
- **Host Live Classes**: The educator can set up and conduct live classes for students.
- **Create and Grade Quizzes**: The educator designs quizzes for students, grades them, and provides feedback based on their performance.
- **Monitor Student Progress**: The educator can view the performance of students in their courses, including quiz results, participation in live classes, and overall progress.

### 3. **Admin Use Cases**
- **Manage Users**: The admin manages student and educator accounts, including registration, profile updates, and user status (active/inactive).
- **Manage Courses**: The admin oversees the courses available on the platform, approving or rejecting courses created by educators.
- **Monitor System Performance**: The admin tracks the overall health of the platform, including performance metrics, user activity, and system load.
- **Generate Reports**: The admin generates various reports related to user activity, course enrollments, payment history, and system performance.

### Relationships Between Use Cases

- **Includes**: 
  - "Register and Authenticate" includes "Browse and Enroll in Courses", "Watch Video Lessons", and "Take Quizzes" as they require authentication to access content.
  - "Watch Video Lessons" includes "Attend Live Classes" as both are part of the student’s learning journey.
  - "Take Quizzes" includes "View Progress", as quizzes are an integral part of tracking student progress.

- **Extends**: 
  - "Attend Live Classes" extends "Watch Video Lessons" because live classes are an optional form of content delivery that supplements video lessons.

## Use Case Diagram Summary

- **Students** primarily interact with features that help them access educational content, track progress, and pay for courses.
- **Educators** focus on course creation, content management, and student assessment.
- **Admins** have administrative control over user management, course oversight, and system health monitoring.

<img width="1512" alt="Screenshot 2024-12-04 at 7 04 03 PM" src="https://github.com/user-attachments/assets/b22defa5-c4c5-4a14-aa11-5ae7e46790f5">

```
const useCaseDiagram = `
@startuml
actor Student
actor Educator
actor Admin

Student -> (Register and Authenticate)
Student -> (Browse and Enroll in Courses)
Student -> (Watch Video Lessons)
Student -> (Attend Live Classes)
Student -> (Take Quizzes)
Student -> (View Progress)
Student -> (Make Payments)

Educator -> (Register and Authenticate)
Educator -> (Create and Manage Courses)
Educator -> (Host Live Classes)
Educator -> (Create and Grade Quizzes)
Educator -> (Monitor Student Progress)

Admin -> (Manage Users)
Admin -> (Manage Courses)
Admin -> (Monitor System Performance)
Admin -> (Generate Reports)

(Register and Authenticate) --> (Browse and Enroll in Courses)
(Register and Authenticate) --> (Watch Video Lessons)
(Register and Authenticate) --> (Take Quizzes)

(Watch Video Lessons) --> (Attend Live Classes)
(Take Quizzes) --> (View Progress)

@enduml
`;

describe('Use-Case Diagram for Byju\'s Competitor', function() {
  it('should generate use case diagram code', function() {
    const expectedUseCaseDiagram = `
@startuml
actor Student
actor Educator
actor Admin

Student -> (Register and Authenticate)
Student -> (Browse and Enroll in Courses)
Student -> (Watch Video Lessons)
Student -> (Attend Live Classes)
Student -> (Take Quizzes)
Student -> (View Progress)
Student -> (Make Payments)

Educator -> (Register and Authenticate)
Educator -> (Create and Manage Courses)
Educator -> (Host Live Classes)
Educator -> (Create and Grade Quizzes)
Educator -> (Monitor Student Progress)

Admin -> (Manage Users)
Admin -> (Manage Courses)
Admin -> (Monitor System Performance)
Admin -> (Generate Reports)

(Register and Authenticate) --> (Browse and Enroll in Courses)
(Register and Authenticate) --> (Watch 
```

---

# Error Case Diagram for Byju's Competitor

The following error case diagram describes potential error scenarios and interactions in the Byju's Competitor application. These error cases represent situations where a user’s action or the system's behavior leads to an error. The system is designed to handle these errors and provide appropriate feedback to users.

## Actors

1. **Student**: A user who encounters various error cases when interacting with the platform, such as during registration, login, course enrollment, or payments.
2. **Educator**: A user who may also encounter error cases related to course creation, managing content, or interacting with students.
3. **Admin**: A user who may experience error cases related to user management or system performance.

## Error Cases

### 1. **Student Error Cases**

- **Invalid Registration Details**
    - **Description**: The student enters incorrect or incomplete details during registration (e.g., invalid email, weak password).
    - **Error Message**: "Invalid email format" or "Password must be at least 8 characters long."
    - **Resolution**: Prompt the user to correct the input and submit again.

- **Failed Login Attempt**
    - **Description**: The student enters incorrect login credentials (wrong email or password).
    - **Error Message**: "Invalid username or password. Please try again."
    - **Resolution**: Allow the student to retry with the correct credentials or reset the password.

- **Course Enrollment Failure**
    - **Description**: The student attempts to enroll in a course that is no longer available or full.
    - **Error Message**: "This course is no longer available or is at full capacity."
    - **Resolution**: Provide an option to view similar courses or join a waitlist.

- **Payment Failure**
    - **Description**: The student’s payment is unsuccessful due to network issues, invalid payment method, or insufficient funds.
    - **Error Message**: "Payment could not be processed. Please check your payment details or try again later."
    - **Resolution**: Suggest the student to verify payment details or try using a different payment method.

### 2. **Educator Error Cases**

- **Course Creation Failure**
    - **Description**: The educator attempts to create a course but misses required fields like course title or description.
    - **Error Message**: "Please fill in all required fields."
    - **Resolution**: Prompt the educator to complete the missing details and submit again.

- **Live Class Scheduling Conflict**
    - **Description**: The educator tries to schedule a live class at the same time as another class or when no available slots exist.
    - **Error Message**: "The selected time slot is unavailable. Please choose another time."
    - **Resolution**: Provide available time slots for scheduling.

- **Failed Quiz Submission**
    - **Description**: The educator tries to submit a quiz with missing questions or incomplete settings.
    - **Error Message**: "Please ensure all questions are completed before submitting."
    - **Resolution**: Prompt the educator to fill in missing information.

### 3. **Admin Error Cases**

- **User Account Management Failure**
    - **Description**: The admin tries to deactivate or delete a user account, but the operation fails due to system errors.
    - **Error Message**: "An error occurred while deactivating or deleting the account. Please try again."
    - **Resolution**: Provide an option to retry or contact support for assistance.

- **Course Approval Failure**
    - **Description**: The admin attempts to approve a course but the system cannot process due to validation issues or a missing course file.
    - **Error Message**: "Course approval failed. Please check the course details."
    - **Resolution**: Prompt the admin to review course details or contact the educator for missing information.

- **Report Generation Failure**
    - **Description**: The admin tries to generate a report, but the system fails due to data inconsistency or network issues.
    - **Error Message**: "Report generation failed due to an error. Please try again later."
    - **Resolution**: Suggest the admin retry or use a different report format.

## Error Handling Strategy

- **System Feedback**: The application provides clear and concise error messages to guide the users in resolving issues.
- **Retry Mechanism**: For critical actions like payments or registration, users are given options to retry the operation.
- **Support Integration**: In cases of persistent errors, users can access customer support directly through the application for resolution.

## Error Case Diagram Summary

- **Students** encounter errors related to registration, login, course enrollment, and payment.
- **Educators** face errors when creating or managing courses, scheduling live classes, or grading quizzes.
- **Admins** handle system-level errors related to user management, course approval, and report generation.

  
<img width="1512" alt="Screenshot 2024-12-04 at 7 15 03 PM" src="https://github.com/user-attachments/assets/7a241f66-207b-4a9f-9f19-2aac4d2268f1">

```
@startuml

actor Student
actor Educator
actor Admin

Student --> (Login Error)
Student --> (Payment Failure)
Student --> (Video Streaming Failure)

Educator --> (Course Upload Failure)
Educator --> (Live Class Connection Failure)
Educator --> (Quiz Creation Error)

Admin --> (User Deletion Failure)
Admin --> (Database Connection Error)

(Login Error) ..> (Register and Authenticate) : includes
(Payment Failure) ..> (Make Payments) : includes
(Video Streaming Failure) ..> (Watch Video Lessons) : includes

@enduml
```

---

# Abuse Case Diagram for Byju's Competitor

The following abuse case diagram describes potential abusive scenarios and interactions within the Byju's Competitor application. These abuse cases represent malicious or harmful behaviors from users that could affect the system's integrity, user experience, or platform safety. The system is designed to handle and prevent these abuse cases through preventive measures and reporting mechanisms.

## Actors

1. **Student**: A user who may engage in abusive behavior such as cheating, harassment, or spamming, affecting other users or the system.
2. **Educator**: A user who might engage in harmful activities like sharing inappropriate content, exploiting students, or abusing their privileges.
3. **Admin**: A user responsible for managing and addressing abuse cases, monitoring the platform, and enforcing rules.

## Abuse Cases

### 1. **Student Abuse Cases**

- **Cheating During Quizzes**
    - **Description**: A student attempts to cheat during a quiz by using unauthorized resources or collaborating with others.
    - **Preventive Measures**: Randomized quiz questions, time limits, and browser lockdowns to prevent cheating.
    - **Resolution**: The system detects unusual behavior and flags the student for manual review. Repeated offenses may result in account suspension or banning.
    
- **Harassing Other Students or Educators**
    - **Description**: A student engages in harassment by sending inappropriate messages, threats, or offensive comments to other students or educators.
    - **Preventive Measures**: Reporting mechanisms, keyword filters for abusive language, and user behavior monitoring.
    - **Resolution**: The system notifies the admin of the reported abuse, and the user’s actions are reviewed. Appropriate action is taken (e.g., warning, suspension, or banning).

- **Spamming the Discussion Forums**
    - **Description**: A student floods discussion forums with irrelevant or promotional content, disrupting the learning environment.
    - **Preventive Measures**: Limit the number of posts per student in a set time period and implement a flagging system for suspicious posts.
    - **Resolution**: Admin receives a report of spam activity. The student may be issued a warning or temporarily suspended from participating in forums.

### 2. **Educator Abuse Cases**

- **Sharing Inappropriate Content**
    - **Description**: An educator uploads content that is offensive, irrelevant, or violates platform policies (e.g., offensive language, inappropriate images, or videos).
    - **Preventive Measures**: Content moderation, manual review of new courses, and flagged content by students or other educators.
    - **Resolution**: The content is flagged for review. If the educator is found violating platform policies, the content is removed, and the educator may be penalized (e.g., course removal, account suspension, or banning).

- **Exploiting Students for Personal Gain**
    - **Description**: An educator encourages or pressures students to purchase personal products, services, or external services unrelated to the platform.
    - **Preventive Measures**: Monitoring and flagging communications between educators and students for inappropriate behavior or marketing.
    - **Resolution**: If the educator is found exploiting students, their account is suspended, and they may face a ban from the platform.

- **Manipulating Course Reviews**
    - **Description**: An educator submits fake reviews or pressures students to leave positive reviews to artificially inflate the course ratings.
    - **Preventive Measures**: Review authenticity checks, flagging suspicious review patterns, and requiring user verification for reviews.
    - **Resolution**: The educator’s account is flagged, and the reviews are reviewed for authenticity. If the behavior is confirmed, the educator faces penalties, including course removal and account suspension.

### 3. **Admin Abuse Cases**

- **Misuse of Admin Privileges**
    - **Description**: The admin accesses or modifies user data without authorization or uses admin privileges for personal gain.
    - **Preventive Measures**: Role-based access controls, audit trails for admin actions, and limiting access to sensitive data.
    - **Resolution**: If abuse is detected, the admin’s access is revoked, and the incident is reported to the higher authorities. Legal action may be taken depending on the severity.

- **Ignoring Abuse Reports**
    - **Description**: An admin ignores reported abuse cases or fails to take appropriate action against abusive users, which can lead to further harm.
    - **Preventive Measures**: Set clear response timelines for abuse reports and an automated escalation process if the admin fails to act within a set period.
    - **Resolution**: If the admin consistently ignores reports, their actions are reviewed, and they may be removed from their role. The incident is escalated to a higher-level admin or governance board.

## Abuse Handling Strategy

- **Automated Detection**: The system incorporates various automated tools to detect and flag abusive behavior, such as cheating, harassment, or spamming.
- **Reporting Mechanism**: Users can report abuse cases via built-in reporting features in the application. Each abuse case is reviewed by an admin or moderator.
- **Manual Review**: Suspected abuse cases are escalated for manual review by admins. A thorough investigation is conducted before any actions are taken.
- **Suspension and Banning**: Users who violate platform policies are subject to warnings, account suspension, or permanent bans, depending on the severity of the abuse.

## Abuse Case Diagram Summary

- **Students** may abuse the system by cheating, harassing other users, or spamming discussion forums.
- **Educators** can engage in inappropriate behaviors such as sharing offensive content, exploiting students, or manipulating course reviews.
- **Admins** can abuse their privileges by mishandling user data or ignoring abuse reports.
  
<img width="1512" alt="Screenshot 2024-12-04 at 7 24 30 PM" src="https://github.com/user-attachments/assets/997a48ca-0cff-42e2-9e36-a35a01228862">

```
@startuml

actor MaliciousStudent
actor MaliciousEducator
actor MaliciousAdmin

MaliciousStudent --> (Fake Enrollment)
MaliciousStudent --> (Manipulate Quiz Results)
MaliciousStudent --> (Access Unauthorized Courses)

MaliciousEducator --> (Upload Inappropriate Content)
MaliciousEducator --> (Manipulate Student Results)
MaliciousEducator --> (Create Fake Courses)

MaliciousAdmin --> (Delete User Accounts)
MaliciousAdmin --> (Access Private User Data)

(Fake Enrollment) ..> (Make Payments) : includes
(Upload Inappropriate Content) ..> (Create and Manage Courses) : includes

@enduml


```

---




