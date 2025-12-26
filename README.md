# Project Scoring, Evaluation & Management System (PSEMS)

## 📌 Overview

The **Project Scoring, Evaluation & Management System (PSEMS)** is a medium enterprise-grade, web-based platform designed to manage the **entire lifecycle of academic and competitive projects** across faculties and departments.

The system supports **customizable workflows**, **flexible evaluation rubrics**, **multi-role user interactions**, and **robust data management**, making it suitable for:

* Software engineering projects
* Design and research projects
* Faculty-wide innovation challenges
* Open university competitions

PSEMS is developed as a **Data Management module project (two-semester scope)** and is designed to be deployable at **faculty or university level**.

---

## 🎯 Objectives

* Eliminate inconsistencies and delays in manual project evaluation
* Provide a centralized and transparent evaluation platform
* Support multiple departments, courses, and competitions
* Enable supervisor-driven and student-driven project models
* Ensure scalability, security, and data integrity
* Demonstrate enterprise-grade data modeling and workflow design

---

## 👥 User Roles & Types

### User Types

| Type       | Description                                                          |
| ---------- | -------------------------------------------------------------------- |
| Student    | Enrolled in a course/module                                          |
| Competitor | University student not enrolled in the course (external participant) |

### System Roles

| Role                  | Description                                                   |
| --------------------- | ------------------------------------------------------------- |
| Student / Competitor  | Submits or applies for projects, uploads deliverables         |
| Supervisor (Lecturer) | Publishes projects, supervises student groups                 |
| Evaluator             | Evaluates projects using defined rubrics                      |
| **Head Judge**        | Senior evaluator who reviews and approves evaluator scores    |
| Course Coordinator    | Manages courses, rubrics, and evaluator assignments           |
| System Admin          | Manages users, departments, competitions, and system settings |

> **Note:** A *Head Judge* is an evaluator with additional approval privileges.

---

## 🔄 Project Origination Models

### 1️⃣ Supervisor-Published Projects

* Supervisors publish project ideas
* Students / competitors apply
* Supervisor selects a group
* Supervisor is **automatically assigned**

### 2️⃣ Student / Competitor-Published Projects

* Students or competitors submit project proposals
* Projects remain **pending** until a supervisor selects them
* Supervisor assignment activates the project

Both models coexist within the same system.

---

## 🧑‍🤝‍🧑 Student & Competitor Groups

* Groups can be created by students or competitors
* Group size configurable per course or competition
* Groups apply or submit projects as a unit
* No mixing of student and competitor groups (fairness rule)

---

## 🔄 Complete Project Lifecycle

1. Project published (Supervisor / Student / Competitor)
2. Project open for applications or supervisor selection
3. Supervisor assigned
4. Proposal submission
5. Proposal evaluation
6. Development phase
7. Final submission
8. Evaluator scoring
9. **Head Judge review & approval**
10. Final score aggregation & ranking
11. Reporting & analytics

---

## ⚙️ Key Features

### 📂 Project Management

* Supervisor-published & student-published projects
* Course-based and competition-based projects
* Multiple submission stages
* Versioned submissions

### 📊 Evaluation & Rubrics

* Fully configurable rubrics per course/competition
* Multiple evaluators per project
* Weighted, numeric, or grade-based scoring
* **Head Judge approval workflow**
* Automatic score aggregation

### 🧑‍💼 User & Role Management

* Role-Based Access Control (RBAC)
* User type separation (Student / Competitor)
* Secure authentication & authorization

### 📈 Reports & Analytics

* Project rankings (course / competition)
* Department-level analytics
* Export reports (CSV / PDF)

### 🔔 Notifications

* Submission deadline reminders
* Evaluation status notifications
* Score publication alerts

### 🔐 Security & Audit

* JWT-based authentication
* Secure file uploads
* Input validation
* Full audit logs for critical actions

---

## 🧱 System Architecture

```
Frontend (React)
   │
   ▼
Backend API (Node.js + TypeScript)
   │
   ▼
Relational Database (PostgreSQL)
```

* Layered architecture (UI, API, Data)
* RESTful API design
* Dockerized for portability and scalability

---

## 🛠️ Technology Stack

### Frontend

* React
* Tailwind CSS / Material UI

### Backend

* Node.js
* TypeScript
* Express.js

### Database

* PostgreSQL

### Authentication

* JWT / OAuth2

### DevOps

* Docker
* Docker Compose
* Git & GitHub

### Testing

* Jest / Mocha (Backend)
* React Testing Library (Frontend)

---

## 🗃️ Database Design (Core Entities)

* User
* Department
* Course
* Competition
* Project
* ProjectApplication
* StudentGroup
* ProjectSubmission
* Rubric
* RubricItem
* Evaluation
* EvaluationReview (Head Judge)
* AuditLog

The relational database ensures **ACID compliance**, **normalization**, and **data integrity**.

---

## 🔌 API Overview (Sample Endpoints)

### Authentication

* `POST /auth/login`
* `POST /auth/register`

### Projects

* `POST /projects`
* `GET /projects/{id}`
* `POST /projects/{id}/apply`
* `POST /projects/{id}/assign-supervisor`

### Submissions

* `POST /submissions`
* `GET /submissions/{id}`

### Evaluations

* `POST /evaluations`
* `POST /evaluations/{id}/review` *(Head Judge)*

### Reports

* `GET /reports/course/{courseId}`
* `GET /reports/competition/{competitionId}`

---

## 🧪 Testing Strategy

* Unit tests for business logic
* Integration tests for API and database
* End-to-end testing for workflows
* Concurrency and multi-user validation

---

## 🚀 Deployment Strategy

### Development

* Local deployment using Docker Compose

### Production (Faculty / University Level)

* Cloud deployment (AWS / Azure / GCP)
* Containerized services
* Automated database backups
* Log monitoring

---

## 🗓️ Project Timeline (Two Semesters)

### Semester 1 – Core System & Data Management

* Requirements analysis
* ER modeling & schema design
* Backend API development
* Project & evaluation workflows

### Semester 2 – Frontend & Enterprise Features

* Role-based dashboards
* Head Judge workflow
* Reporting & analytics
* Notifications
* Deployment & documentation

---

## 📚 Academic Value

This project demonstrates:

* Advanced relational data modeling
* Multi-user database interactions
* Enterprise-grade RBAC
* Approval-based evaluation workflows
* Scalable system architecture

It is suitable for **faculty-wide adoption** and future expansion.

---

## ✅ Future Enhancements

* GraphQL API support
* Advanced analytics dashboards
* Plagiarism detection
* External examiner access
* Mobile application support
* Inter-university competitions

---

**PSEMS – A scalable, transparent, and enterprise-ready academic project evaluation system.**

---
