# Employee Management System - Backend

A Spring Boot REST API for managing employees, built using **Java 17**, **Spring Boot**, **JPA**, and **PostgreSQL**. The application is deployed on **Render** with secure, environment-based configuration.

---

## 🚀 Live API Base URL
**Base URL:** https://ems-backend-zapm.onrender.com

All endpoints are prefixed with: `/api/employees`

---

## ✨ Features
* **RESTful APIs:** Full CRUD operations for employee management.
* **ORM:** Spring Data JPA with Hibernate ORM.
* **Database:** Managed PostgreSQL instance on Render.
* **Secure Config:** Environment variable-based configuration.
* **Database Automation:** Automatic table creation using Hibernate.
* **Cloud Ready:** Production-ready deployment on the Render platform.

---

## 🛠 Tech Stack
| Component | Technology |
| :--- | :--- |
| **Language** | Java 17 |
| **Framework** | Spring Boot 3.3.2 |
| **ORM** | Spring Data JPA (Hibernate) |
| **Database** | PostgreSQL |
| **Build Tool** | Maven |
| **Deployment** | Render |

---

## 🛣 API Endpoints

| Action | Method | Endpoint |
| :--- | :--- | :--- |
| **Create Employee** | `POST` | `/api/employees` |
| **Get All Employees** | `GET` | `/api/employees` |
| **Get Employee by ID** | `GET` | `/api/employees/{id}` |
| **Update Employee** | `PUT` | `/api/employees/{id}` |
| **Delete Employee** | `DELETE` | `/api/employees/{id}` |

### Request Body Format (POST/PUT)
```json
{
  "firstName": "Manas",
  "lastName": "Madhukar",
  "email": "manas@example.com"
}

```
## ⚙️ Configuration

The application uses environment-based configuration to keep sensitive credentials secure.

### Spring Properties
In your `src/main/resources/application.properties`, the following properties are used:

* `spring.application.name=ems-backend`
* `spring.datasource.url=${DB_URL}`
* `spring.datasource.username=${DB_USERNAME}`
* `spring.datasource.password=${DB_PASSWORD}`
* `spring.jpa.hibernate.ddl-auto=update`

### Environment Variables
For the application to connect to the database, ensure these variables are set in your local environment or Render dashboard:

* **`DB_URL`**: `jdbc:postgresql://<internal-host>:5432/<database-name>`
* **`DB_USERNAME`**: `<database-username>`
* **`DB_PASSWORD`**: `<database-password>`

---

## 💻 Running Locally
Ensure you have Maven and Java 17 installed. To start the application, run:

```bash
mvn spring-boot:run
```
---

## ☁️ Deployment
The application is deployed on **Render** as a Web Service and utilizes **Render PostgreSQL**. **Hibernate** is configured to automatically create and update database tables on startup.

---

## 🧠 Key Learnings
Through the development of this project, the following concepts were explored and implemented:

* **PostgreSQL integration** using Spring Data JPA.
* Understanding the **JDBC and Hibernate startup lifecycle**.
* **Debugging** production database connectivity issues.
* Executing **secure cloud deployment** using Render.

---

## 👤 Author
**Manas Madhukar**




