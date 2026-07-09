# Business Workflow 008

# Guest Management

**Workflow ID:** BWF-008

**Version:** 1.0.0

**Status:** Approved for Development

**Priority:** Critical

---

# Purpose

Guest Management is one of the core capabilities of MiEvent.

Every event relies on accurate guest information. This workflow defines how guests are created, imported, managed, invited, tracked and prepared for the event.

The Guest module is the central source of truth for everyone attending an event.

It powers:

- Invitations
- RSVP tracking
- Table planning
- Dietary management
- Guest communications
- Check-in (future)
- Reporting
- Catering numbers

No other module may duplicate guest information.

---

# Business Objective

Provide organisers and clients with one collaborative guest management experience that replaces spreadsheets and eliminates duplicate data.

Guest information should always be live, accurate and immediately available to authorised users.

---

# Primary Personas

- Event Manager
- Client

---

# Supporting Personas

- Organisation Administrator
- Venue (read-only)
- Caterer (dietary information only)
- Guest (future)

---

# Trigger

Guest planning begins after the Workspace has been created.

---

# Preconditions

- Workspace exists.
- Client has accepted invitation.
- Guest permissions are enabled.
- Event date has been confirmed.

---

# Business Rules

## BR-020

Every Guest belongs to exactly one Workspace.

---

## BR-021

Guest email addresses must be unique within a Workspace.

---

## BR-022

Every Guest has an RSVP status.

---

## BR-023

Every Guest may belong to one table only.

---

## BR-024

Dietary requirements belong to the Guest.

They are never duplicated elsewhere.

---

## BR-025

Changes made by the Client are immediately visible to the Event Manager.

---

## BR-026

Every Guest update creates an Activity Log entry.

---

## BR-027

Guest information is automatically saved.

---

## BR-028

Deleted guests are soft deleted.

---

# Guest Sources

Guests may be added by:

### Manual Entry

Individual guest creation.

---

### CSV Import

Excel

Numbers

CSV

---

### Client Portal

Client adds guests directly.

---

### API

Future integrations.

---

### Template

Reuse previous event structures.

---

# Guest Record

Every Guest contains:

## Identity

- First Name
- Last Name
- Preferred Name
- Title

---

## Contact

- Email
- Mobile
- Address (optional)

---

## Attendance

- RSVP
- Plus One
- Invite Sent
- Invite Accepted
- Check-in (future)

---

## Catering

- Meal Choice
- Dietary Requirements
- Allergies

---

## Seating

- Table
- Seat Number

---

## Notes

- Internal Notes
- Client Notes

---

## Tags

Examples

VIP

Family

Bride

Groom

Supplier Guest

Child

Evening Guest

Speaker

Press

---

# Main Success Scenario

1. Event Manager opens Guest module.
2. Imports guests using CSV.
3. Reviews imported data.
4. Invites Client to review.
5. Client edits guest list.
6. Auto-save updates Workspace.
7. Event Manager reviews changes.
8. Guests receive invitations (future).
9. RSVP responses update automatically.
10. Catering numbers update.
11. Table planning begins.

---

# Alternative Flows

## Manual Guest Entry

Used for smaller events.

---

## CSV Validation Errors

Rows containing errors are highlighted.

Import continues for valid rows.

---

## Duplicate Guest

MiEvent detects duplicates.

User may:

Merge

Ignore

Replace

---

## Guest Cancels

RSVP updated.

Tables update automatically.

Catering numbers update.

Timeline updated.

---

# Guest Status

Draft

↓

Invited

↓

Awaiting RSVP

↓

Accepted

↓

Declined

↓

Checked In (Future)

↓

Archived

---

# Permissions

## Client

Create

Read

Update

Delete (optional)

---

## Event Manager

Full access.

---

## Venue

Read guest numbers only.

---

## Caterer

Read dietary information only.

---

## Supplier

No access.

---

# Data Created

Guest

RSVP

Dietary Record

Table Assignment

Invitation

Activity Log

Notification

---

# Domain Events

GuestCreated

GuestUpdated

GuestDeleted

GuestImported

RSVPUpdated

DietaryUpdated

TableAssigned

GuestMerged

---

# Notifications

Client

Guest changes saved.

RSVP reminders.

Incomplete guest list.

---

Event Manager

Guest imported.

Client updated guest list.

RSVP changed.

Dietary changes.

---

# Business Metrics

Track:

Total Guests

Accepted

Declined

Awaiting RSVP

Children

VIP Guests

Dietary Count

Average RSVP Rate

Guest Completion %

---

# Risks

Duplicate guests.

Incorrect dietary information.

Incorrect seating.

CSV formatting errors.

Late RSVP changes.

---

# Automation Opportunities

Automatically:

Send RSVP reminders.

Notify organiser of dietary changes.

Detect duplicate guests.

Suggest table assignments.

Generate catering totals.

Generate attendance reports.

---

# AI Opportunities

Suggest seating arrangements.

Predict RSVP rates.

Detect family groups.

Recommend table layouts.

Identify missing guest information.

Highlight unusual dietary requests.

---

# Future Enhancements

QR Invitations

Digital Invitations

SMS Invitations

Guest Mobile App

Live Check-In

QR Check-In

Facial Recognition Check-In

AI Seating Planner

Gift Tracking

Travel Management

Accommodation Management

---

# Related Requirements

FR-027 Guest Management

FR-028 RSVP Management

FR-029 Dietary Management

FR-030 Table Planning

---

# Related UX Screens

Guest Dashboard

Guest List

Guest Import Wizard

Guest Details

RSVP Dashboard

---

# Related Database Entities

Workspace

Guest

RSVP

DietaryRequirement

TableAssignment

ActivityLog

Notification

---

# Related APIs

See Volume VI.

Guest CRUD

CSV Import

RSVP Update

Table Assignment

Invitation

---

# Related Tests

Guest Import

Duplicate Detection

CSV Validation

Permission Validation

RSVP Workflow

Auto-save

Soft Delete

---

# Claude Code Guidance

Guest Management is one of the most important modules in MiEvent.

It should feel comparable to Airtable or Linear rather than Excel.

Large guest lists (2,000+ guests) must remain fast.

Inline editing should be available.

Filtering, searching and bulk editing are essential.

CSV import must provide intelligent validation with clear error reporting.

Every change should be optimistic, automatically saved and visible to collaborators in real time.

The Guest module will become the foundation for RSVP management, table planning, catering, invitations and future check-in features.

Optimise for performance, collaboration and scalability from the very beginning.

---

# End of Workflow
