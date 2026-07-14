# OTM Exception Resolution Copilot

## Project Goal

Build a web application that connects to Oracle Transportation Management (OTM) and helps transportation planners identify and resolve shipment exceptions faster.

The first version will be read-only and will not make changes to Oracle OTM.

---

## Users

- Transportation Planner
- Operations Manager
- Logistics Analyst

---

## MVP Features

### 1. Retrieve shipment data
- Read shipment information from Oracle OTM (or mock data initially).
- Normalize shipment data into a common internal model.

### 2. Detect exceptions

Initially support:

- Late Delivery Risk
- Missing Delivery Appointment
- Tender Rejected
- Unplanned Order

### 3. Display exceptions

For every exception show:

- Shipment ID
- Carrier
- Origin
- Destination
- ETA
- Severity
- Exception Type

### 4. AI Recommendation

Generate:

- Summary
- Probable Cause
- Suggested Next Action

The AI must never determine whether an exception exists.
Exception detection is performed only by business rules.

### 5. Planner Workflow

Planner can:

- View exceptions
- Assign exceptions
- Add notes
- Mark resolved

No updates are written back to Oracle OTM in Version 1.

---

## Technical Stack

Backend

- Python
- FastAPI
- Pydantic

Frontend

- React
- TypeScript

Database

- PostgreSQL

AI

- IBM watsonx.ai or approved enterprise LLM

---

## Security

- Read-only Oracle OTM access
- No credentials stored in Git
- Environment variables for secrets
- Role-based access
- Audit logging

---

## Success Criteria

The application can:

1. Read one shipment.
2. Detect a late delivery.
3. Display the exception.
4. Show an AI explanation.
5. Record planner resolution.
