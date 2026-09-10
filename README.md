# Smart Parking Management System (SPMS)

A software solution for automating the discovery, reservation, monitoring, and billing of parking spaces in a parking facility — built as a Software Engineering course project.

## Team Members

| Name | Role |
|---|---|
| Anubhav Mittal | Team Lead / Documentation & Testing |
| Amit Kumar | Backend Developer |
| Ankit Modi | Frontend Developer |
| Arpit Gupta | Database & System Design |


*(Roles are suggested placeholders — update them to match actual responsibilities.)*

## Project Overview

Manual parking management leads to wasted driver time, underutilized parking spaces, revenue leakage, and poor visibility for facility administrators. SPMS solves this by giving drivers real-time slot availability, online reservation, and automated entry/exit detection, while giving administrators a dashboard to manage slots, pricing, and reports.

### Key Features
- Driver registration, login, and profile management
- Real-time parking slot search and availability display
- Advance slot reservation and cancellation
- Automatic vehicle entry/exit detection (IoT sensors / ANPR camera)
- Duration-based fee calculation and online payment processing
- Digital receipts and booking history
- Notifications for booking confirmation, payment status, and slot expiry
- Admin dashboard for slot inventory, pricing rules, and occupancy/revenue reports

### Actors
- **Driver** — searches, books, and pays for parking slots
- **Admin** — manages slot inventory, pricing, and views reports
- **Sensor / Camera (IoT/ANPR)** — detects vehicle entry and exit
- **Payment Gateway** — processes online payments

## Tech Stack

> Update this section with your team's actual chosen technologies.

| Layer | Technology |
|---|---|
| Frontend (Driver app) | e.g. React Native / Flutter |
| Frontend (Admin dashboard) | e.g. React.js |
| Backend | e.g. Node.js / Express or Spring Boot |
| Database | e.g. MySQL / PostgreSQL |
| Hardware | IoT sensors / ANPR camera module |
| Payment Integration | e.g. Razorpay / Stripe API |
| Version Control | Git & GitHub |

## Project Documentation

| Document | Description |
|---|---|
| `docs/SPMS_Requirement_Report.docx` | Elicited stakeholder requirements, FR/NFR list, constraints, MoSCoW prioritization |
| `docs/SPMS_SRS.docx` | Software Requirements Specification (IEEE 830 format) |
| `docs/uml/` | Use Case, Class, Sequence, State Chart, Activity, and Component diagrams |

## Repository Structure

```
smart-parking-management-system/
├── README.md
├── docs/
│   ├── SPMS_Requirement_Report.docx
│   ├── SPMS_SRS.docx
│   └── uml/
│       ├── use-case-diagram.png
│       ├── class-diagram.png
│       ├── sequence-diagram.png
│       ├── state-diagram.png
│       ├── activity-diagram.png
│       └── component-diagram.png
├── frontend/
│   └── (driver app / admin dashboard source code)
├── backend/
│   └── (API server source code)
├── database/
│   └── (schema, migrations, seed data)
└── tests/
    └── (unit and integration tests)
```

## Getting Started

> Fill in once the codebase is set up.

### Prerequisites
- Node.js (or relevant runtime) vX.X+
- MySQL/PostgreSQL vX.X+
- Git

### Installation
```bash
git clone https://github.com/<org>/smart-parking-management-system.git
cd smart-parking-management-system
# install backend dependencies
cd backend && npm install
# install frontend dependencies
cd ../frontend && npm install
```

### Running the Project
```bash
# start backend server
cd backend && npm start
# start frontend
cd frontend && npm start
```

### Environment Variables
Create a `.env` file in `backend/` with:
```
DB_HOST=
DB_USER=
DB_PASSWORD=
DB_NAME=
PAYMENT_GATEWAY_API_KEY=
JWT_SECRET=
```

## Contribution Guidelines
1. Create a feature branch from `main`: `git checkout -b feature/<name>`
2. Commit with clear messages describing the change
3. Push and open a Pull Request for review
4. At least one team member must review before merging
5. Keep documentation (`docs/`) updated when requirements or design change

## Project Status
🚧 In Development — Requirement Analysis and Design (UML) phases complete. Implementation in progress.

## License
This project is developed for academic purposes as part of a Software Engineering course.