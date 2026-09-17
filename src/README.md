# Smart Parking Management System — Source Code (`src/`)

This directory contains the application source code structure for the **Smart Parking Management System (SPMS)**.

## Module Architecture

The system follows a standard 3-tier software architecture:

```
src/
├── backend/            # Express.js / Node.js API Service
│   ├── controllers/    # Request handlers (Auth, Slot, Reservation, Payment)
│   ├── models/         # Database models & ORM entities
│   ├── routes/         # REST API endpoint definitions
│   └── services/       # Business logic (Fee calculation, ANPR/Sensor event handler)
├── frontend/           # React.js Web Application
│   ├── components/     # UI components (Slot grid, Search bar, Receipt modal)
│   ├── pages/          # Application views (Driver Dashboard, Admin Dashboard)
│   └── services/       # API client & HTTP service handlers
└── database/           # Relational schema & migration scripts
    ├── schema.sql      # Database tables (Users, Slots, Reservations, Payments, Logs)
    └── seed.sql        # Initial parking slot data & test users
```

## Software Scope & Hardware Interface Simulation

As specified in the **Requirement Report** and **SRS**:
- The software system provides API endpoints to receive vehicle entry/exit signals from IoT sensors or ANPR cameras (`POST /api/events/entry` and `POST /api/events/exit`).
- In environments without physical hardware attached, these endpoints can be triggered via simulated webhook calls or administrator controls.
