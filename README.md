
# 🎓 University-Based Smart Parking System

![University](https://img.shields.io/badge/University-Bahria%20University%20Islamabad-blue)
![Course](https://img.shields.io/badge/Course-SEN%20220%20--%20Software%20Engineering-green)
![Semester](https://img.shields.io/badge/Semester-Spring%202026-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# 📋 Table of Contents

- Project Overview
- Problem Statement
- Milestone 1: Requirements
- Milestone 2: System Modeling
- Milestone 3: Design & Architecture
- Milestone 4: Testing & Project Management
- Contributors
- References

---

# 🚗 Project Overview

The **University-Based Smart Parking System** is a comprehensive Software Engineering documentation project developed for **Bahria University Islamabad** under the **SEN 220 - Software Engineering** course.

The system is designed to digitize and streamline campus parking management through vehicle registration, parking permits, slot reservations, occupancy monitoring, QR/RFID verification, and administrative reporting.

The project focuses on **requirements engineering, system modeling, architecture design, testing plans, and project management documentation** rather than actual implementation.

---

# ✨ Key Features

## 🚘 Parking Management

- Vehicle registration system
- Parking permit management
- Slot and zone reservation
- Real-time parking availability
- Entry and exit verification

## 🔒 Security & Verification

- QR/RFID-based gate verification
- Role-based access control
- Permit validation
- Manual override logging
- Violation reporting

## 📊 Monitoring & Reporting

- Occupancy monitoring
- Parking utilization reports
- Violation reports
- Entry/exit logs
- Peak-hour analysis

## 🏫 Multi-Role System

- Students
- Faculty
- Staff
- Visitors
- Security Guards
- Parking Administrators

---

# ❗ Problem Statement

Universities face serious parking management challenges because large numbers of students, faculty members, visitors, and staff enter campus during the same time period.

Traditional parking systems suffer from:

❌ Manual permit checking  
❌ Lack of real-time slot visibility  
❌ Unauthorized parking  
❌ Parking congestion  
❌ Poor occupancy monitoring  
❌ Weak reporting and analytics  

### 🎯 Proposed Solution

The **University-Based Smart Parking System** provides a digital solution using:

- Parking permits
- QR/RFID verification
- Slot reservations
- Occupancy tracking
- Parking violation management
- Administrative dashboards

---

# 📘 Milestone 1: Requirements

## 1.1 Project Scope

### ✅ IN SCOPE

- Vehicle registration
- Parking permit management
- Slot reservation
- Parking availability tracking
- QR/RFID gate verification
- Occupancy monitoring
- Violation management
- Admin dashboards and reports
- Notifications and alerts

### ❌ OUT OF SCOPE

- Real hardware deployment
- ANPR implementation
- IoT hardware installation
- Commercial payment gateways
- Live production deployment

---

# 1.2 Functional Requirements

| FR # | Requirement | Priority |
|---|---|---|
| FR-01 | User login with role-based access | High |
| FR-02 | Vehicle registration with plate details | High |
| FR-03 | Visitor pass request management | Medium |
| FR-04 | Parking permit application | High |
| FR-05 | Permit approval/rejection by admin | High |
| FR-06 | Real-time parking availability | High |
| FR-07 | Parking slot reservation | High |
| FR-08 | QR-based digital parking pass generation | High |
| FR-09 | Gate verification using QR/RFID/Plate | High |
| FR-10 | Entry/exit logging | High |
| FR-11 | Slot occupancy status updates | High |
| FR-12 | Violation reporting by guards | Medium |
| FR-13 | Parking analytics and reporting | High |

---

# 1.3 Non-Functional Requirements

| NFR # | Category | Requirement |
|---|---|---|
| NFR-01 | Performance | Gate verification within 3 seconds |
| NFR-02 | Security | Password hashing and RBAC |
| NFR-03 | Reliability | No loss of logs or permit data |
| NFR-04 | Availability | Available during university hours |
| NFR-05 | Scalability | Support future zones and users |
| NFR-06 | Maintainability | Layered architecture support |
| NFR-07 | Compatibility | Desktop and mobile browser support |
| NFR-08 | Auditability | Log all sensitive actions |

---

# 1.4 Use Case Diagram
![Use Case Diagram](Diagrams/Use%20Case%20Diagram.jpg)

---

# 📗 Use Case Descriptions

## UC-01: Register / Login

| Field | Detail |
|---|---|
| Use Case ID | UC-01 |
| Actor(s) | Student / Faculty / Staff / Visitor / Guard / Admin |
| Goal | Secure access to the system |
| Pre-condition | Valid account exists |
| Main Flow | User enters credentials → system validates → dashboard displayed |
| Alternate Flow | Invalid credentials show error |
| Post-condition | Session created |

---

## UC-02: Register Vehicle

| Field | Detail |
|---|---|
| Use Case ID | UC-02 |
| Actor(s) | Student / Faculty / Staff |
| Goal | Add vehicle to system |
| Main Flow | Enter vehicle details → validate → save |
| Post-condition | Vehicle registered successfully |

---

## UC-03: Reserve Parking Slot

| Field | Detail |
|---|---|
| Use Case ID | UC-03 |
| Actor(s) | Authorized User |
| Goal | Reserve available parking slot |
| Main Flow | View availability → select slot → confirm reservation |
| Alternate Flow | Suggest another slot if unavailable |
| Post-condition | Reservation created with QR pass |

---

## UC-04: Gate Entry Verification

| Field | Detail |
|---|---|
| Use Case ID | UC-04 |
| Actor(s) | User / Guard / Gate Device |
| Goal | Verify authorized vehicle |
| Main Flow | Scan QR/RFID → validate permit → open gate |
| Alternate Flow | Invalid permit denies access |
| Post-condition | Entry log created |

---

# 📙 Milestone 2: System Modeling

## 2.1 Context Diagram

![Context Diagram](Diagrams/context-diagram.png)
### Description

The context diagram represents the Smart Parking System as a single process interacting with:

- Students
- Faculty
- Visitors
- Guards
- Administrators
- Gate Devices
- Notification Services

---

## 2.2 DFD Level 0

![DFD Level 0](Diagrams/dfd-level-0.png)

### Major Processes

- User Authentication
- Vehicle & Permit Management
- Slot Management
- Reservation Processing
- Gate Entry/Exit
- Occupancy Monitoring
- Reporting

---

## 2.3 Class Diagram

![Class Diagram](Diagrams/class-diagram.png)

### Core Classes

- User
- Vehicle
- ParkingPermit
- ParkingZone
- ParkingSlot
- Reservation
- EntryExitLog
- Violation
- SensorDevice
- Report

---

## 2.4 Sequence Diagram — Reserve & Enter Parking

![Sequence Diagram](Diagrams/sequence-diagram.png)

### Flow

1. User logs in
2. Selects parking zone
3. System validates permit
4. Slot reserved
5. QR generated
6. User scans QR at gate
7. System validates reservation
8. Entry recorded

---

## 2.5 Activity Diagram

![Activity Diagram](Diagrams/activity-diagram.png)

### Workflow

- Login
- Register vehicle
- Apply permit
- Reserve slot
- Verify at gate
- Park vehicle
- Exit parking

---

## 2.6 State Machine Diagram — Parking Slot

![State Diagram](Diagrams/state-diagram.png)

### Slot States

- Available
- Reserved
- Occupied
- Violation
- Maintenance
- Closed

---

# 🏗️ Milestone 3: Design & Architecture

## 3.1 Layered Architecture

![Architecture Diagram](Diagrams/architecture-diagram.png)

### Architecture Layers

```text
Presentation Layer
    ↓
Controller Layer
    ↓
Business Logic Layer
    ↓
Data Access Layer
    ↓
Database Layer
    ↓
External Device Layer
```

---

## 3.2 Database Schema

| Table | Purpose |
|---|---|
| User | Store users and roles |
| Vehicle | Registered vehicles |
| ParkingPermit | Permit information |
| ParkingZone | Parking zones |
| ParkingSlot | Individual slots |
| Reservation | Slot reservations |
| EntryExitLog | Entry/exit history |
| Violation | Parking violations |
| SensorDevice | External device data |
| Notification | Alerts and notifications |

---

## 3.3 Security Considerations

- Password hashing
- Role-based access control
- Permit validation
- Audit logs
- Secure QR verification
- Validation of user inputs

---

# 🧪 Milestone 4: Testing & Project Management

## 4.1 Test Plan

### Testing Types

| Testing | Purpose |
|---|---|
| Unit Testing | Verify individual modules |
| Integration Testing | Verify connected modules |
| System Testing | End-to-end workflows |
| Security Testing | Authentication & authorization |
| Performance Testing | Response under load |

---

## 4.2 Sample Test Cases

| TC # | Scenario | Expected Output |
|---|---|---|
| TC-01 | Valid login | Dashboard displayed |
| TC-02 | Invalid password | Access denied |
| TC-03 | Register vehicle | Vehicle saved |
| TC-04 | Duplicate plate | Validation error |
| TC-05 | Reserve slot | Reservation created |
| TC-06 | Expired QR | Entry denied |
| TC-07 | Report violation | Violation stored |

---

## 4.3 GitHub Version Control Workflow

### Repository

```text
github.com/your-username/sen220-smart-parking-system-report
```

### Branch Strategy

- `main` → Final stable version
- `develop` → Development branch
- `feature/*` → New features
- `hotfix/*` → Emergency fixes

### Commit Format

```bash
feat:
fix:
docs:
test:
chore:
```

---

## 4.4 Team Roles & Responsibilities

| Team Member | Role | Responsibilities |
|---|---|---|
| Member 1 | Requirements & Architecture Lead | Requirements, architecture, database design |
| Member 2 | Modeling & Testing Lead | UML diagrams, DFDs, testing documentation |

---

## 4.5 Project Planning — Timeline

![PERT Chart](Diagrams/pert-chart.png)

### Major Tasks

- Requirements Analysis
- Use Case Modeling
- DFD & UML Design
- Architecture Design
- Testing Documentation
- Risk Analysis
- Final Submission

---

## 4.6 Risk Analysis

| Risk # | Risk Description | Mitigation |
|---|---|---|
| R-01 | Missing assignment deliverables | Checklist validation |
| R-02 | Diagram inconsistency | Cross-check requirements |
| R-03 | Team workload pressure | Proper task division |
| R-04 | Formatting issues | Final proofreading |
| R-05 | Missing GitHub evidence | Create repository early |

---

# 👥 Contributors

| Name | Registration No. | Role |
|---|---|---|
| Your Name | FAxx-BCS-xxx | Requirements & Architecture Lead |
| Member 2 | FAxx-BCS-xxx | Modeling & Testing Lead |

### Course Information

**Course:** Software Engineering (SEN 220)  
**Instructor:** Aima Zahoor  
**Institution:** Bahria University Islamabad Campus  
**Semester:** Spring 2026  

---

# 📚 References

1. Sommerville, I. *Software Engineering*.
2. Pressman, R. S. & Maxim, B. R. *Software Engineering: A Practitioner's Approach*.
3. Fowler, M. *UML Distilled*.
4. IEEE Recommended Practice for SRS.
5. Object Management Group — UML Specification.
6. General university parking workflow analysis.

---

# ✅ Project Status

**Last Updated:** May 10, 2026  
**Status:** Complete & Ready for Submission
