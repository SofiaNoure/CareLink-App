# CareLink-App
Medical Appointment Management System
CareLink (also referred to as MediSync) is a web-based medical appointment management system built with Spring Boot and Thymeleaf.
It enables patients to easily book medical appointments and allows doctors to efficiently manage their schedules through a structured and intuitive platform.
The project follows a clean MVC architecture and focuses on clarity, maintainability, and well-defined business rules.
Data is stored using CSV files loaded into memory, making the application lightweight and suitable for academic and prototype use.
✨ Key Features
👤 Patient
Register and log in securely
Search for doctors by:
Specialty
Location (Wilaya / City)
Availability
View doctor details and available time slots
Book appointments (initial status: PENDING)
View personal appointment history
Cancel or reschedule appointments (under defined conditions)
Receive notifications when appointment status changes
Update personal profile (restricted fields)
🩺 Doctor
Access a dedicated dashboard
View all assigned appointments
Manage appointment lifecycle:
Confirm
Reschedule
Cancel
Mark as completed
Manage available time slots
View dashboard statistics
Update personal profile (restricted fields)
🔄 Appointment Lifecycle
Appointments follow a clear and controlled lifecycle to ensure consistency:
PENDING → CONFIRMED → COMPLETED
        ↘
      RESCHEDULED
        ↘
      CANCELLED
Business Rules
Appointments are created with status PENDING
Only doctors can:
Confirm appointments
Mark appointments as completed
Patients cannot cancel or reschedule an appointment while it is PENDING
Any status change triggers a notification for the patient
🧠 System Responsibilities
Validate appointment availability
Enforce appointment lifecycle rules
Manage user sessions (login / logout)
Maintain data consistency across users and appointments
Provide reference data (wilayas, cities, specialties)
🏗️ Architecture
The application is structured using the Model–View–Controller (MVC) pattern:
View
Thymeleaf HTML templates
CSS and JavaScript for dynamic interaction
Controller
Spring MVC controllers handling HTTP requests
REST endpoints for asynchronous operations
Model
Domain entities (Doctor, Patient, Appointment, etc.)
Business logic via service layer
CSV-based repository for data access
This architecture ensures separation of concerns and improves scalability and maintainability.
💾 Data Storage
The system uses CSV files as an in-memory data source:
doctors.csv
patients.csv
appointments.csv
cities.csv
specialties.csv
All files are loaded at application startup and kept in memory during execution.
🛠️ Technology Stack
Java 17+
Spring Boot
Spring MVC
Thymeleaf
HTML / CSS / JavaScript
CSV-based in-memory persistence
Maven
▶️ Getting Started
Prerequisites
Java 17 or higher
Maven
Run the Application
mvn spring-boot:run
The application will be available at:
http://localhost:8080
📈 Future Improvements
Integration with a relational database (MySQL / PostgreSQL)
Email or SMS notification system
Password recovery functionality
Dedicated administrator dashboard
Enhanced security and role management
Public REST API for mobile or third-party clients
🎓 Academic Context
This project was developed as part of a Software Engineering course within an Artificial Intelligence Engineering program.
It demonstrates:
Web application architecture
Business rule modeling
MVC-based design
Clean separation of responsibilities
Realistic healthcare workflow management
