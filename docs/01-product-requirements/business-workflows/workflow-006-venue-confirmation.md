# Business Workflow 006

# Venue Confirmation

**Workflow ID:** BWF-006

**Version:** 1.0.0

**Status:** Approved for Development

---

# Purpose

This workflow defines how a venue is invited into an Event Workspace and collaborates with the Event Manager throughout the planning process.

Venues are one of the most important collaborators in event delivery. They require access to operational information but should not have visibility of confidential client information or internal planning notes.

The Venue Portal provides live access to relevant information, reducing email traffic and ensuring the venue always works from the latest version of the event plan.

---

# Business Goal

Provide venues with a dedicated portal that allows them to:

- Confirm availability
- Review event requirements
- Confirm room layouts
- Review guest numbers
- Coordinate supplier access
- Review timelines
- Upload venue documentation
- Communicate with organisers

without requiring manual document exchange.

---

# Primary Persona

Venue Manager

---

# Supporting Personas

- Event Manager
- Organisation Administrator
- Client (read-only visibility for selected items)

---

# Trigger

The Event Manager has selected a venue and is ready to begin operational planning.

---

# Preconditions

- Workspace exists.
- Venue exists or is created.
- Venue contact has a valid email address.
- Event date has been confirmed.

---

# Business Rules

BR-008

Each Workspace may contain one primary venue.

BR-009

Additional venue contacts may be invited.

BR-010

Venue users may only view information relevant to venue operations.

BR-011

Venue users cannot access financial information.

BR-012

Venue users cannot edit guest information.

BR-013

Venue confirmations are timestamped.

---

# Venue Information Required

- Venue Name
- Address
- Contact Name
- Email
- Telephone
- Capacity
- Room Names
- Accessibility Facilities
- Parking Information
- Supplier Access Rules

---

# Main Success Scenario

1. Event Manager opens Workspace.
2. Selects Venue module.
3. Searches existing venues or creates a new venue.
4. Chooses primary venue.
5. Assigns venue contact.
6. Sends invitation.
7. Resend sends invitation email.
8. Venue contact authenticates through Clerk.
9. Venue Portal opens.
10. Venue confirms booking.
11. Venue reviews event details.
12. Activity recorded.
13. Event Manager notified.

---

# Venue Dashboard

The venue dashboard includes:

- Event Overview
- Arrival Schedule
- Supplier Schedule
- Room Layout
- Guest Numbers
- Event Timeline
- Messages
- Files
- Venue Tasks
- Activity

---

# Alternative Flows

## Venue Already Exists

Existing venue profile linked.

Previous venue notes remain available.

---

## Venue Declines

Event Manager notified.

Alternative venue selected.

Activity recorded.

---

## Multiple Venue Contacts

Venue manager invites additional staff.

Permissions inherited.

---

## Venue Requests Changes

Venue comments on timeline.

Requests room changes.

Suggests operational adjustments.

---

# Permissions

Venue users may:

View

Comment

Upload Files

Complete Tasks

Confirm Information

Venue users may not:

Delete information

Modify guests

Modify finances

Manage suppliers

View internal notes

---

# Data Created

Venue

VenueMembership

Invitation

VenueConfirmation

ActivityLog

Notification

Files

---

# Events Raised

VenueInvited

VenueAccepted

VenueConfirmed

VenueUpdated

VenueCommentAdded

VenueFileUploaded

---

# Notifications

Venue

Invitation

Reminder

Confirmation Received

Task Assigned

Event Manager

Venue Accepted

Venue Updated Details

Venue Uploaded Files

Venue Requested Changes

---

# Failure Conditions

Venue email invalid.

Invitation expired.

Venue already removed.

Authentication failed.

Workspace archived.

Subscription inactive.

---

# Success Criteria

✓ Venue accepts invitation.

✓ Venue accesses Workspace.

✓ Venue confirms booking.

✓ Event Manager notified.

✓ Activity recorded.

---

# Related Requirements

FR-020 Venue Portal

FR-021 Venue Management

FR-022 Permissions

---

# Related UX Screens

Venue Dashboard

Venue Module

Workspace Overview

Messages

Timeline

Files

---

# Related Database Entities

Venue

VenueContact

Workspace

Membership

ActivityLog

Notification

Files

---

# Automation Opportunities

Future versions should automatically:

- Remind venue to confirm booking.
- Request updated venue documentation.
- Alert organisers if confirmations are overdue.
- Generate supplier access schedules.

---

# AI Opportunities

Future AI features may:

Summarise venue conversations.

Suggest room layouts.

Identify scheduling conflicts.

Recommend supplier arrival times.

Predict operational issues.

---

# Business Metrics

Track:

Time to venue confirmation.

Number of venue messages.

Confirmation completion rate.

Average response time.

Venue portal engagement.

---

# Future Expansion

Multiple venues.

Ceremony + Reception.

Hotels.

Festival sites.

Conference centres.

International venue integrations.

---

# Claude Code Guidance

The Venue Portal should feel like a dedicated operational dashboard.

Venue users should immediately understand:

- what today's priorities are,
- what requires action,
- what has changed,
- what still needs confirmation.

Avoid exposing unnecessary planning complexity.

The interface should prioritise operational clarity over administrative detail.

---

# End of Workflow
