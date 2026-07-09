# Business Workflow 002

# Create Event Workspace

**Workflow ID:** BWF-002

**Version:** 1.0.0

**Status:** Approved for Development

---

# Purpose

This workflow defines how a new Event Workspace is created within an Organisation.

The Workspace is the core operational unit of MiEvent.

Every event—regardless of type—is represented by a Workspace that brings together clients, venues, suppliers, guests, tasks, files, messages and planning data into a single collaborative environment.

---

# Business Goal

Allow an Event Manager to create a new event in less than five minutes.

The resulting Workspace should immediately provide a structured environment for planning and collaboration.

---

# Primary Persona

Event Manager

---

# Supporting Personas

- Organisation Owner
- Organisation Administrator

---

# Trigger

The organiser has secured a new event and is ready to begin planning.

---

# Preconditions

- User is authenticated.
- User belongs to an Organisation.
- User has permission to create Workspaces.
- Organisation has an active subscription.

---

# Inputs

Required:

- Event Name
- Event Type
- Event Date
- Time Zone

Optional:

- Venue
- Client
- Budget
- Expected Guest Count
- Internal Notes
- Template

---

# Main Success Scenario

1. User selects **Create Workspace** from the dashboard.
2. The Workspace creation wizard opens.
3. User enters event details.
4. User selects an event template or starts from scratch.
5. User submits the form.
6. MiEvent creates the Workspace.
7. Default modules are provisioned.
8. A default timeline is generated.
9. The Workspace becomes available immediately.
10. The organiser is redirected to the Workspace Overview.

---

# Default Modules Created

Every Workspace contains:

- Overview
- Timeline
- Guests
- Table Plan
- Venue
- Suppliers
- Catering
- Decor
- Files
- Tasks
- Messages
- Forms
- Activity
- Settings

These modules are provisioned automatically and remain available throughout the event lifecycle.

---

# Business Rules

- Every Workspace belongs to exactly one Organisation.
- Every Workspace has one primary Event Manager.
- Workspaces may be archived but never permanently deleted by standard users.
- Event type determines the default template.
- Workspace names must be unique within an Organisation.

---

# Alternative Flows

### Existing Template

The organiser selects a saved Workspace template.

The new Workspace inherits:

- Task lists
- Timeline structure
- Supplier categories
- Forms
- Checklists

---

### Duplicate Existing Workspace

The organiser duplicates a previous event.

Guest data is **not** copied.

Only reusable planning structures are retained.

---

### Draft Workspace

The organiser saves the Workspace as a draft.

Draft Workspaces are hidden from clients until activated.

---

# Data Created

This workflow creates:

- Workspace
- Activity Log
- Default Modules
- Timeline
- Permission Set
- Notification Preferences

---

# Events Raised

The following domain events are published:

- WorkspaceCreated
- TimelineCreated
- ModulesProvisioned
- ActivityRecorded

These events may be consumed by notifications, integrations or future automation.

---

# Notifications

Internal notifications:

- Workspace created successfully.

Optional notifications:

- Notify Organisation Admin.
- Notify assigned Event Manager.

Clients are **not** notified during Workspace creation.

---

# Failure Conditions

Workspace creation must fail if:

- Required information is missing.
- Organisation has reached Workspace limits.
- Subscription is inactive.
- Event date is invalid.

The user should receive a clear explanation and be able to correct the issue without losing progress.

---

# Success Criteria

The workflow is complete when:

- Workspace exists.
- Default modules are available.
- Timeline is created.
- Activity history records the creation.
- Organiser is redirected to the Workspace Overview.

---

# Related Requirements

- FR-002 Workspace Management
- FR-005 Event Templates
- FR-010 Permissions

---

# Related UX Screens

- Dashboard
- Create Workspace Wizard
- Workspace Overview

---

# Related Database Entities

- Organisation
- Workspace
- WorkspaceModule
- ActivityLog

---

# Related APIs

See Volume VI – API Specification.

---

# Related Tests

See Volume XI – Testing Strategy.

---

# End of Workflow
