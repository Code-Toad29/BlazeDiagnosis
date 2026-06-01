# Blaze Diagnostics MVP User Stories

## User Roles

- Workshop Admin: manages the workshop account and users.
- Service Advisor: creates customers, vehicles, job cards, quotes, and invoices.
- Mechanic: updates work progress and job notes.
- Customer: receives updates and approves or rejects quotes.
- System Admin: manages platform-wide support where required.

---

# Epic 1: Authentication and Access Control

## Story 1.1: User Login

As a workshop user, I want to log in securely so that I can access the correct dashboard.

### Acceptance Criteria

- User can enter email and password.
- Invalid login displays a clear error.
- Valid login stores a session safely.
- User is redirected to an appropriate dashboard.
- Passwords are not stored in plain text.

## Story 1.2: Role-Based Access

As a workshop admin, I want users to have roles so that staff only access the areas they need.

### Acceptance Criteria

- Roles are stored for users.
- Routes are protected by role or permission.
- Unauthorized users cannot access restricted data.
- Navigation only shows relevant options where possible.

---

# Epic 2: Customer and Vehicle Management

## Story 2.1: Create Customer Profile

As a service advisor, I want to create customer profiles so that vehicles and jobs can be linked to the correct client.

### Acceptance Criteria

- Customer can be created with name, mobile number, email, and notes.
- Customer can be searched.
- Customer can be edited.
- Customer can be linked to one or more vehicles.

## Story 2.2: Add Vehicle

As a service advisor, I want to add a customer's vehicle so that repair jobs can be tracked against the correct vehicle.

### Acceptance Criteria

- Vehicle is linked to a customer.
- Vehicle stores registration number, make, model, year, VIN, mileage, and notes where available.
- One customer can have multiple vehicles.

---

# Epic 3: Job Card Management

## Story 3.1: Create Job Card

As a service advisor, I want to create a job card so that work can be tracked from booking to collection.

### Acceptance Criteria

- Job card links to customer and vehicle.
- Job card stores complaint, date received, assigned mechanic, priority, and status.
- Job card has a unique reference number.
- Initial status is clear.

## Story 3.2: Update Job Status

As a mechanic or service advisor, I want to update the job status so that the customer knows what is happening.

### Acceptance Criteria

- Authorized users can update status.
- Status changes are stored with timestamp and user.
- Status history is visible internally.
- Customer-safe status updates are visible to customers.

Suggested statuses:

- Booked In
- Inspection Started
- Quote Required
- Awaiting Quote Approval
- Quote Approved
- Parts Ordered
- Awaiting Parts
- Parts Received
- In Progress
- Quality Check
- Ready for Collection
- Completed
- Cancelled

---

# Epic 4: Quote Management

## Story 4.1: Create Quote

As a service advisor, I want to create a quote so that the customer can approve work before the workshop proceeds.

### Acceptance Criteria

- Quote is linked to a job.
- Quote includes line items, labour, parts, VAT/tax, and total.
- Quote can be saved as draft.
- Quote can be sent for approval.

## Story 4.2: Customer Approves or Rejects Quote

As a customer, I want to approve or reject a quote so that the workshop knows whether to continue.

### Acceptance Criteria

- Customer can approve a quote.
- Customer can reject a quote with an optional comment.
- Approval or rejection is timestamped.
- Workshop can see the decision.

---

# Epic 5: Parts Tracking

## Story 5.1: Track Ordered Parts

As a service advisor, I want to track parts ordered for a job so that the workshop and customer know why a vehicle may be delayed.

### Acceptance Criteria

- Parts are linked to a job.
- Parts have status, supplier, quantity, and expected delivery date.
- Internal cost is not exposed to the customer unless intended.
- Customer sees clear parts progress messages.

---

# Epic 6: Mechanic Updates

## Story 6.1: Add Mechanic Progress Notes

As a mechanic, I want to add progress notes so that the workshop and customer can track work progress.

### Acceptance Criteria

- Notes include timestamp and user.
- Notes can be internal-only or customer-visible.
- Customer-visible notes are professional and clear.

---

# Epic 7: Customer Tracking Page

## Story 7.1: View Vehicle Progress

As a customer, I want to view my vehicle's progress so that I do not need to phone the workshop for updates.

### Acceptance Criteria

- Customer sees job status, quote status, parts status, and collection readiness.
- Customer only sees their own job information.
- Customer-facing language is clear.
- Access is secure.

---

# Epic 8: Notifications

## Story 8.1: Create Notification Events

As a workshop, I want notification events to be recorded so that customers can receive updates through future channels.

### Acceptance Criteria

- Events are created for quote, parts, work progress, ready-for-collection, and invoice updates.
- Notification history is stored.
- Message templates are clear and customer-friendly.

---

# Epic 9: Invoicing and Collection

## Story 9.1: Generate Invoice

As a service advisor, I want to generate an invoice from an approved quote so that the customer can be billed accurately.

### Acceptance Criteria

- Invoice links to job, customer, vehicle, and quote.
- Invoice includes line items and total.
- Invoice status can be issued or paid.

## Story 9.2: Mark Vehicle Ready for Collection

As a service advisor, I want to mark a vehicle as ready for collection so that the customer can be notified.

### Acceptance Criteria

- Job status updates to ready for collection.
- Customer-facing message is generated.
- Invoice/payment requirements are visible.

---

# Epic 10: Audit Trail and Security

## Story 10.1: Activity Log

As a workshop admin, I want important changes to be logged so that there is accountability.

### Acceptance Criteria

- Status changes are logged.
- Quote actions are logged.
- Invoice actions are logged.
- User and timestamp are recorded.

## Story 10.2: Protect Customer Data

As a workshop owner, I want customer and vehicle data protected so that private information is not exposed.

### Acceptance Criteria

- Customer access is scoped.
- Internal information is not exposed on customer pages.
- Secrets are not committed to GitHub.
- Error messages do not leak sensitive details.
