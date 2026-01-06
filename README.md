# CareLink-App

---

## Business Rules

- Appointments are created with status **PENDING**
- Only doctors can:
  - Confirm appointments
  - Mark appointments as completed
- Patients cannot cancel or reschedule an appointment while it is **PENDING**
- Any status change triggers a notification to the patient

---

## System Responsibilities

- Validate appointment availability
- Enforce appointment lifecycle rules
- Manage user sessions (login / logout)
- Maintain data consistency across users and appointments
- Provide reference data:
  - Wilayas
  - Cities
  - Specialties

---

## Architecture

The application follows the **Model–View–Controller (MVC)** pattern:

- **View**
  - Thymeleaf HTML templates
  - CSS and JavaScript for dynamic interaction
- **Controller**
  - Spring MVC controllers
  - Handle HTTP requests and REST endpoints
- **Model**
  - Domain entities (Doctor, Patient, Appointment, etc.)
  - Business logic implemented in a service layer
  - CSV-based repository for data access

This architecture ensures a clear separation of concerns and improves scalability and maintainability.

---

## Data Storage

The system uses CSV files as an in-memory data source:

- doctors.csv
- patients.csv
- appointments.csv
- cities.csv
- specialties.csv

All files are loaded at application startup and kept in memory during execution.

---

## Technology Stack

- Java 17+
- Spring Boot
- Spring MVC
- Thymeleaf
- HTML / CSS / JavaScript
- Maven
- CSV-based in-memory persistence

---

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven

### Run the Application

```bash
mvn spring-boot:run

