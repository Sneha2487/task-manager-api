# Task Manager API

Task Manager API is a backend REST service built using Spring Boot.
It supports CRUD operations for tasks and uses PostgreSQL for persistence.
The project follows a clean layered architecture.

---

## Tech Stack

- Java 17
- Spring Boot 3
- Spring Data JPA
- PostgreSQL
- Maven
- REST APIs

---

## Features

- Create new tasks
- Update existing tasks
- Delete tasks
- Fetch all tasks
- Fetch task by ID
- Track task status (PENDING, COMPLETED)
- Due date support
- Clean layered architecture

---

## API Endpoints

Base URL: http://localhost:8080

| Method | Endpoint           | Description     |
|--------|--------------------|-----------------|
| POST   | /api/tasks         | Create task     |
| GET    | /api/tasks         | Get all tasks   |
| GET    | /api/tasks/{id}    | Get task by ID  |
| PUT    | /api/tasks/{id}    | Update task     |
| DELETE | /api/tasks/{id}    | Delete task     |

---

## Sample Request (Create Task)

```json
{
  "title": "Complete backend project",
  "description": "Finish Task Manager API",
  "status": "PENDING",
  "dueDate": "2026-02-28"
}
```
---

## Sample Response

```json
{
  "id": 1,
  "title": "Complete backend project",
  "description": "Finish Task Manager API",
  "status": "PENDING",
  "dueDate": "2026-02-28"
}
```
---

## Project Structure

src/main/java/com/sneha/taskmanager
├── controller
│   └── TaskController.java
├── service
│   ├── TaskService.java
│   └── impl
│       └── TaskServiceImpl.java
├── repository
│   └── TaskRepository.java
├── entity
│   └── Task.java
└── TaskManagerApiApplication.java

---

## Getting Started

### Prerequisites
- Java 17
- Maven
- PostgreSQL

---

## Database Configuration

Configure PostgreSQL in `src/main/resources/application.properties`:

spring.datasource.url=jdbc:postgresql://localhost:5432/task_manager_db  
spring.datasource.username=your_username  
spring.datasource.password=your_password

---

### Run Locally

1. Clone the repository

```bash
git clone https://github.com/Sneha2487/task-manager-api.git
cd task-manager-api 
```
2. Configure PostgreSQL database

3. Run the application
```bash
./mvnw spring-boot:run
```
4. Access API

http://localhost:8080/api/tasks
