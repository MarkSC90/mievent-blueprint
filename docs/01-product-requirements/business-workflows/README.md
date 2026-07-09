# Business Workflows

**Document ID:** MIE-BWF-001

**Version:** 1.0.0

**Status:** Draft

---

# Purpose

Business Workflows define how MiEvent operates.

Rather than documenting pages or screens, this section documents the real operational processes that event businesses perform every day.

Each workflow becomes the authoritative specification for how MiEvent should behave.

Every workflow will eventually map directly to:

- User Experience
- API
- Database
- Permissions
- Notifications
- Emails
- Components
- Testing

This creates complete traceability throughout the platform.

---

# Workflow Philosophy

MiEvent is designed around workflows rather than pages.

Users do not think:

> "I need the Guest page."

Users think:

> "I need to invite my guests."

Therefore every feature should be modelled as a business process.

---

# Standard Workflow Template

Every workflow follows the same structure.

1. Objective
2. Personas
3. Trigger
4. Preconditions
5. Main Flow
6. Alternative Flows
7. Data Created
8. Permissions
9. Notifications
10. API
11. Database
12. Acceptance Criteria
13. Future Improvements

This consistency allows workflows to be implemented independently while maintaining a consistent product architecture.

---

# Workflow Catalogue

## Core Business Workflows

BWF-001 Create Organisation

BWF-002 Create Workspace

BWF-003 Invite Internal Team

BWF-004 Invite Client

BWF-005 Client Completes Event Details

BWF-006 Venue Confirmation

BWF-007 Invite Supplier

BWF-008 Guest Import

BWF-009 RSVP Management

BWF-010 Table Planning

BWF-011 Dietary Management

BWF-012 Timeline Planning

BWF-013 Task Management

BWF-014 File Management

BWF-015 Messaging

BWF-016 Final Event Review

BWF-017 Live Event Operations

BWF-018 Complete Event

BWF-019 Archive Workspace

BWF-020 Create Event Template

---

# Workflow Relationships

Most workflows depend upon previous workflows.

Example:

Create Workspace

↓

Invite Client

↓

Client Questionnaire

↓

Guest Import

↓

RSVP Collection

↓

Table Planning

↓

Timeline

↓

Live Event

↓

Archive

The Product Team should avoid introducing workflows that bypass the normal event lifecycle unless there is a clear business requirement.

---

# Design Principles

Every workflow should:

Reduce administration.

Improve collaboration.

Minimise manual data entry.

Support mobile devices.

Support permissions.

Generate an activity history.

Expose functionality through the Open API.

Remain reusable.

---

# Traceability

Every workflow must reference:

Functional Requirements

Database Entities

API Endpoints

UI Screens

Notifications

Permissions

Acceptance Tests

No workflow should exist in isolation.

---

# Claude Code Guidance

Claude Code should treat each workflow document as the authoritative implementation specification.

User interfaces, APIs, permissions, notifications and database entities should all follow the behaviour described by the workflow.

If implementation differs from the workflow, the workflow should be considered correct unless superseded by a later Product Decision Record (PDR).

---

# Next Document

Continue with:

workflow-001-create-organisation.md
