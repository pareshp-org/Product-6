# UAT Runbook — Product-6 (Security & Compliance Auditing)

## Feature
Immutable audit log trail and compliance event capture

## Preconditions
- Service is configured with valid environment (`.env.local` or `.env.example`).
- Database migrations have been applied via `make migrate`.
- Required port is free and accessible.

## Steps
1. Start Product-6 on port 8086
2. Record audit event via POST /api/v1/audit
3. Query audit events via GET /api/v1/audit

## Expected Results
- Audit event is logged with actor, action, timestamp, and metadata
- Query returns complete audit trail matching recorded event

---
*Author: QA & Primary Owner (MasterSpec Section 31.1, Section 33.1)*
*Verification Contract: `verification/contract.yaml`*
