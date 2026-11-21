# Smart Clinic Management System - Architecture Summary

## Section 1: Architecture Summary

The Smart Clinic Management System is a full-stack web application developed using Spring Boot, following a layered architecture based on Controllers, Services, and Repositories. The system supports multiple user roles including Admins, Doctors, and Patients, each with different permissions and responsibilities.

The application uses both MVC and REST architectures. MVC controllers render Thymeleaf-based pages for authentication and dashboard views, while REST controllers expose APIs for managing doctors, patients, appointments, and prescriptions. Business logic is centralized in the service layer, which acts as an intermediary between controllers and repositories.

The system uses two databases. MySQL stores structured and relational data such as users, doctors, patients, admins, and appointments using JPA entities and Hibernate. MongoDB stores prescription documents and medical notes, allowing greater flexibility for unstructured healthcare data. JWT authentication is used to secure API access and enforce role-based authorization.

Docker is used to containerize the application and its supporting services, while GitHub Actions provides continuous integration for automated build, testing, and validation.

---

## Section 2: Numbered Flow of Data and Control

1. A user (Admin, Doctor, or Patient) accesses the application through the web interface.

2. The user submits a request, such as logging in, viewing appointments, or creating a prescription.

3. The request is routed to the appropriate MVC Controller or REST Controller within the Spring Boot application.

4. The controller validates the request and sends it to the corresponding Service Layer component.

5. The service layer executes the required business logic and interacts with the appropriate repository.

6. The repository retrieves or stores data in MySQL for structured clinic data or MongoDB for prescription documents.

7. The processed result is returned from the repository to the service layer, then to the controller, and finally displayed to the user as a web page or JSON response.
