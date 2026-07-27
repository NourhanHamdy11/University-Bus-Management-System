<div align="center">

# 📋 Software Requirements Specification
### University Bus Management System

*Extracted and formatted from the original project specification (February 2025)*

</div>

---

## Table of Contents

- [1. Functional Requirements](#1-functional-requirements)
- [2. Non-Functional Requirements](#2-non-functional-requirements)
- [3. Requirement Traceability](#3-requirement-traceability)

---

## 1. Functional Requirements

Thirteen functional requirements were defined, grouped into six capability areas. Each requirement is assigned an ID (`FR-XX`) used throughout this repository — including in the sequence-diagram explanations in [`SYSTEM_DESIGN.md`](SYSTEM_DESIGN.md) — for traceability.

### 1.1 Trip Management — Assigning Drivers and Buses

| ID | Requirement |
|----|-------------|
| **FR-01** | The system allows the Bus Coordinator to assign a driver to each scheduled trip. |
| **FR-02** | The system allows the Bus Coordinator to assign a specific bus to each scheduled trip. |

### 1.2 System Management — System Control and Updates

| ID | Requirement |
|----|-------------|
| **FR-03** | The system allows the Administrator to control system settings. |
| **FR-04** | The system shall allow the Administrator to update trip schedules and user information. |

### 1.3 Booking a Trip — Selecting Trip Time and Route

| ID | Requirement |
|----|-------------|
| **FR-05** | The system allows the Student to select a route. |
| **FR-06** | The system allows the Student to select a going and return trip. |
| **FR-07** | The system allows the Student to select a time slot for each trip, either going or return. |

### 1.4 Generating QR Code

| ID | Requirement |
|----|-------------|
| **FR-08** | The system should generate a unique QR code for the Student after booking a trip. |

### 1.5 Cancelling a Booking

| ID | Requirement |
|----|-------------|
| **FR-09** | The system shall allow the Student to cancel a previously booked trip. |

### 1.6 Bus Tracking — Driver Starts Trip Tracking / Real-Time Tracking for Students

| ID | Requirement |
|----|-------------|
| **FR-10** | The system should allow the Bus Driver to start trip tracking when the journey begins. |
| **FR-11** | The system will notify students when the bus driver reaches the first station. |
| **FR-12** | The system shall allow the Student to view the real-time location of the bus. |

### 1.7 QR Code Validation — Student Identity Verification

| ID | Requirement |
|----|-------------|
| **FR-13** | The system allows the Bus Driver to scan and validate the student's QR code before allowing them to board. |

---

## 2. Non-Functional Requirements

### 2.1 Performance

- The system's user interface should load in **less than 3 seconds**.
- Response time for any operation should be **less than 2 seconds** under normal conditions.
- The system should support **at least 500 concurrent users** without significant delays.

### 2.2 Scalability

- The system should scale to accommodate more users and buses **without requiring major infrastructure changes**.
- The system should support **adding new routes and stations** easily.

### 2.3 Security

- All data transmitted between the client and server should be **encrypted using SSL/TLS**.
- A strong authentication system (**Two-Factor Authentication**) should be implemented for drivers and administrators.
- Each trip must have a **unique QR Code** to prevent misuse.
- Access to trip and driver data should be **role-based** (Role-Based Access Control — RBAC).

### 2.4 Reliability & Availability

- The system should maintain an **uptime of 99.9%** throughout the year.
- There should be an **automatic backup system every 24 hours** to ensure data safety.
- The system should be **recoverable within 30 minutes** in case of failure.

### 2.5 Usability

- The system should be simple and user-friendly, allowing users to navigate it **without prior training**.
- All key functions should be accessible **within three clicks or fewer**.
- The system should support **both Arabic and English** languages.

### 2.6 Compatibility

- The system should be compatible with all modern browsers (**Chrome, Firefox, Edge, Safari**).
- It should function properly on **both Android and iOS** devices.

### 2.7 Maintainability & Updates

- The code should be **well-structured and documented** for easy maintenance.
- The system should support **adding new features** without requiring major modifications to the core code.

### 2.8 Interoperability

- The system should be able to integrate with **online payment systems** and **university student registration systems**.
- It should support **APIs** for potential future integrations with other systems.

### 2.9 Legal & Compliance

- All transactions and user data must be **stored securely** and only accessible by authorized personnel.
- The system must follow **transportation safety regulations** for tracking and student validation.
- QR Code validation must **prevent fraudulent use or duplication**, ensuring only authorized students board the buses.

---

## 3. Requirement Traceability

Mapping from functional requirement to the diagram(s) in [`diagrams/`](diagrams/) that model its behavior:

| Requirement | Modeled In |
|---|---|
| FR-01, FR-02 | `sequence-5-assigning-drivers-buses.png`, `collaboration-2.png` |
| FR-03, FR-04 | `sequence-6-system-update.png` |
| FR-05, FR-06, FR-07 | `sequence-1-booking-a-trip.png`, `collaboration-3.png`, `activity-1.png`, `state-1.png` |
| FR-08 | `sequence-1-booking-a-trip.png`, `state-1.png` |
| FR-09 | `activity-1.png`, `state-1.png` |
| FR-10, FR-12 | `sequence-2-realtime-tracking.png`, `collaboration-1.png`, `activity-2.png` |
| FR-11 | `sequence-3-first-station-notification.png`, `activity-2.png` |
| FR-13 | `sequence-4-qr-code-validation.png`, `state-2.png`, `activity-2.png` |

> 📎 Full use-case-level detail (actors, pre-conditions, actions, post-conditions) lives in [`USE_CASES.md`](USE_CASES.md). Architectural context lives in [`SYSTEM_DESIGN.md`](SYSTEM_DESIGN.md).
