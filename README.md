# Airbnb Clone Project

A full-stack Airbnb-like platform simulating a robust booking system.  
This project focuses on backend development, database design, API security, and CI/CD integration to provide a real-world software development experience.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Team Roles](#team-roles)
3. [Technology Stack](#technology-stack)
4. [Database Design](#database-design)
5. [Feature Breakdown](#feature-breakdown)
6. [API Security](#api-security)
7. [CI/CD Pipeline](#cicd-pipeline)

---

## Project Overview
The Airbnb Clone Project replicates the core functionalities of Airbnb, allowing users to book properties, leave reviews, and make secure payments.  
**Project Goals:**
- Build a scalable backend system for property listings, bookings, and payments.  
- Implement secure APIs and database management.  
- Apply CI/CD pipelines for automated testing and deployment.  
- Integrate Django, MySQL, and GraphQL for a full-stack solution.

**Tech Stack:** Django, MySQL, GraphQL, Docker, GitHub Actions.

---

## Team Roles
- **Backend Developer:** Builds API endpoints, business logic, and server-side functionalities.  
- **Database Administrator (DBA):** Designs relational database schemas, ensures data integrity, and manages migrations.  
- **Frontend Developer:** Creates the user interface and integrates it with the backend APIs.  
- **DevOps Engineer:** Implements CI/CD pipelines, Docker containerization, and deployment automation.  
- **QA Engineer:** Tests features, verifies functionality, and ensures quality and compliance with project standards.

---

## Technology Stack
- **Django:** A Python web framework for building RESTful APIs and server-side logic.  
- **MySQL:** A relational database for storing users, properties, bookings, reviews, and payments.  
- **GraphQL:** Provides flexible API queries to fetch only the necessary data for frontend components.  
- **Docker:** Containerizes applications to create consistent development and production environments.  
- **GitHub Actions:** Automates testing and deployment pipelines to ensure faster, reliable, and repeatable workflows.

**Contribution to Project Goals:** Each technology ensures a scalable, secure, and maintainable system: Django and GraphQL handle data flow; MySQL stores structured data reliably; Docker ensures environment consistency; GitHub Actions streamlines CI/CD automation.

---

## Database Design

### Entities and Fields
1. **Users**
   - `user_id`: Primary identifier
   - `name`: Full name
   - `email`: Unique email address
   - `password`: Hashed password
   - `role`: Role in system (user, host, admin)

2. **Properties**
   - `property_id`: Primary identifier
   - `title`: Property name
   - `description`: Property details
   - `price`: Price per night
   - `host_id`: User ID of the host

3. **Bookings**
   - `booking_id`: Primary identifier
   - `user_id`: ID of booking user
   - `property_id`: ID of booked property
   - `check_in`: Start date
   - `check_out`: End date

4. **Reviews**
   - `review_id`: Primary identifier
   - `booking_id`: Associated booking
   - `rating`: Numeric rating (1-5)
   - `comment`: Optional text feedback
   - `created_at`: Timestamp

5. **Payments**
   - `payment_id`: Primary identifier
   - `booking_id`: Associated booking
   - `amount`: Paid amount
   - `status`: Payment status (pending, completed, failed)
   - `payment_date`: Timestamp

### Relationships
- A **User** can have multiple **Bookings**.  
- Each **Booking** belongs to one **Property**.  
- A **Property** can have multiple **Reviews**.  
- **Payments** are linked to individual **Bookings**.

---

## Feature Breakdown
- **User Management:** Users can sign up, log in, and manage profiles securely.  
- **Property Management:** Hosts can create, edit, and list properties for booking.  
- **Booking System:** Users can book properties with selectable dates and receive confirmation.  
- **Payment Processing:** Payments are handled securely, linking transactions to bookings.  
- **Review System:** Users leave ratings and feedback for properties after their stay.  

---

## API Security
- **Authentication:** Ensures only registered users can access protected endpoints.  
- **Authorization:** Restricts actions based on user roles (e.g., host, admin, guest).  
- **Rate Limiting:** Protects against abuse by limiting requests per user/IP.  
- **Data Encryption:** Encrypts sensitive data such as passwords and payment information to prevent unauthorized access.

**Importance:** These measures protect user privacy, secure payments, and maintain system integrity.

---

## CI/CD Pipeline
Continuous Integration and Deployment automate testing and deployment to ensure fast, reliable, and consistent development.

**Benefits:**
- Detect issues early through automated testing.  
- Ensure reliable deployment to staging and production environments.  
- Maintain consistent environments with containerization.  

**Tools Used:**
- **GitHub Actions:** Automates testing and deployment workflows.  
- **Docker:** Ensures applications run consistently across environments.  

By integrating CI/CD, the project achieves higher quality, faster delivery, and reduced human errors.

---

© 2025 ALX, All rights reserved.
