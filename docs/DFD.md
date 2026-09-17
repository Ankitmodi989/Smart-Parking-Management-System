# Data Flow Diagrams (DFD)

This document describes the Data Flow Diagrams for the **Smart Parking Management System (SPMS)**. It complements the UML diagrams in `docs/uml/` by showing how data moves between external entities, processes, and data stores.

---

## Level 0 — Context Diagram

![Context Diagram](../assets/context-diagram.svg)

Treats SPMS as a single process and shows its interaction with four external entities:

| External Entity | Sends to SPMS | Receives from SPMS |
|---|---|---|
| **Driver** | Registration, login, search & booking requests | Slot availability, booking confirmation, receipts, notifications |
| **Admin** | Pricing rules, slot configurations | Occupancy & revenue reports |
| **Sensor / ANPR Camera** | Vehicle entry/exit signals | — |
| **Payment Gateway** | Payment transaction status | Payment request |

---

## Level 1 — Process Decomposition

![Level 1 DFD](../assets/level-1-dfd.svg)

Breaks the single system process into five sub-processes and four persistent data stores:

### Processes
1. **1.0 Manage Login / Registration** — Authenticates users, manages profile data in `D1 User Data`.
2. **2.0 Search & Reserve Slot** — Checks slot availability in `D2 Slot Data`, writes reservations to `D3 Booking Data`.
3. **3.0 Detect Entry / Exit** — Consumes sensor/ANPR signals, updates occupancy in `D3 Booking Data`, triggers billing.
4. **4.0 Process Payment & Billing** — Calculates parking fees, interfaces with Payment Gateway, writes to `D4 Payment Data`, delivers receipts.
5. **5.0 Notifications & Reports** — Reads `D3`/`D4` to issue driver alerts and compile admin revenue/occupancy statistics.

### Data Stores
- **D1 User Data**: Driver & Admin credentials, profiles, roles.
- **D2 Slot Data**: Slot numbers, types, pricing rates, location data.
- **D3 Booking Data**: Reservation records, entry/exit timestamps, status.
- **D4 Payment Data**: Transaction IDs, amounts, payment methods, receipts.
