# Business Workflow 004

# Invite Client

**Workflow ID:** BWF-004

**Version:** 1.0.0

**Status:** Approved for Development

---

# Purpose

This workflow defines how an Event Manager invites a client into an Event Workspace.

Unlike internal team members, clients have restricted access and are only able to view and interact with information relevant to their event.

The client portal is one of MiEvent's most important features. It replaces long email chains and document exchanges with a live collaborative workspace.

---

# Business Goal

Provide clients with a secure, branded portal where they can:

- Complete event details
- Review planning progress
- Manage guests
- Approve decisions
- Upload inspiration
- Exchange messages
- View documents
- Complete tasks

The invitation process should take less than one minute.

---

# Primary Persona

Event Manager

---

# Supporting Personas

- Client
- Organisation Administrator

---

# Trigger

An event has been created and is ready for client collaboration.

---

# Preconditions

- Workspace exists.
- Client record exists or will be created.
- Event Manager has invitation permissions.
- Client has a valid email address.

---

# Inputs

Required:

- Client Name
- Client Email

Optional:

- Mobile Number
- Preferred Name
- Portal Permissions
- Personal Welcome Message

---

# Main Success Scenario

1. Event Manager opens the Workspace.
2. Navigates to the **Client** module.
3. Clicks **Invite Client**.
4. Searches for an existing client or creates a new client record.
5. Defines client permissions.
6. Optionally customises the welcome message.
7. Sends the invitation.
8. MiEvent creates a secure invitation.
9. Resend sends the branded invitation email.
10. Client opens the invitation link.
11. Client authenticates using Clerk.
12. Client is granted access to the Workspace.
13. Client lands on the Client Dashboard.
14. Activity is recorded.

---

# Client Dashboard

The client dashboard provides access to:

- Event Overview
- Planning Progress
- Guest List
- RSVP Status
- Table Plan (optional)
- Timeline (optional)
- Files
- Messages
- Tasks
- Forms
- Inspiration Gallery
- Approvals

The Event Manager determines which modules are visible.

---

# Business Rules

- Clients only access Workspaces they are invited to.
- Clients cannot view internal notes.
- Clients cannot view financial information unless explicitly enabled.
- Clients cannot manage suppliers.
- Clients cannot modify system settings.
- Clients may upload files where permitted.
- Clients may complete forms assigned to them.
- Every action is recorded in the activity log.

---

# Alternative Flows

## Existing Client

If the client already has a MiEvent account, the Workspace is linked to the existing profile.

---

## Invitation Declined

The invitation remains pending until cancelled or resent.

---

## Invitation Expired

The Event Manager may resend the invitation.

---

## Client Requests Additional Access

The Event Manager may update permissions without sending a new invitation.

---

# Permissions

Clients may be granted access to:

- Overview
- Guest List
- RSVP Management
- Timeline
- Table Plan
- Messages
- Files
- Tasks
- Forms
- Inspiration

Each permission is configurable.

---

# Data Created

- Client
- Workspace Membership
- Invitation
- Notification
- Activity Log

---

# Events Raised

- ClientInvited
- ClientInvitationAccepted
- ClientPortalActivated
- ActivityRecorded

---

# Notifications

Email

- Invitation
- Welcome
- Invitation Accepted

In-App

- Client Joined Workspace
- Client Completed Registration

---

# Failure Conditions

The workflow fails if:

- Email is invalid.
- User lacks permission.
- Workspace is archived.
- Invitation expires.
- Authentication fails.

---

# Success Criteria

- Client receives invitation.
- Client activates account.
- Client accesses Workspace.
- Permissions applied correctly.
- Activity recorded.
- Event Manager notified.

---

# Related Requirements

- FR-013 Client Portal
- FR-014 Invitations
- FR-015 Role Permissions

---

# Related UX Screens

- Workspace Overview
- Client Module
- Client Dashboard
- Invitation Dialog

---

# Related Database Entities

- Client
- Workspace
- Invitation
- Membership
- ActivityLog

---

# Claude Code Guidance

The client portal should feel premium and simple.

Clients should never feel overwhelmed by internal planning tools.

The interface should prioritise clarity, progress tracking and collaboration rather than administration.

---

# End of Workflow
