# Business Workflow 007

# Invite Supplier

**Workflow ID:** BWF-007

**Document ID:** MIE-BWF-007

**Version:** 1.0.0

**Status:** Approved for Development

**Priority:** High

---

# Purpose

This workflow defines how suppliers are invited into an Event Workspace and become active collaborators within MiEvent.

Suppliers are fundamental to successful event delivery. Rather than sending PDFs, emails and WhatsApp messages, suppliers collaborate directly inside the Workspace using role-based permissions.

The objective is to ensure every supplier always works from the latest version of the event plan while only accessing the information required for their role.

---

# Business Objective

Reduce supplier administration while improving operational accuracy.

Every supplier should receive exactly the information required to perform their role—nothing more and nothing less.

The invitation process should take less than two minutes.

---

# Primary Persona

- Event Manager

---

# Supporting Personas

- Organisation Administrator
- Supplier
- Client (optional visibility)

---

# Trigger

A supplier has been selected for an event and requires access to the Workspace.

Typical supplier categories include:

- Caterer
- Photographer
- Videographer
- DJ
- Band
- Florist
- Cake Designer
- Transport Provider
- Production Company
- Celebrant
- Toastmaster
- Entertainment
- Security
- Hire Company

---

# Preconditions

- Workspace exists.
- Event Manager has permission to invite suppliers.
- Supplier record exists or will be created.
- Supplier has a valid email address.
- Workspace is active.

---

# Business Rules

## BR-014

Every supplier belongs to one Organisation but may work across multiple Workspaces.

---

## BR-015

A supplier only accesses Workspaces they have been explicitly invited to.

---

## BR-016

Suppliers only see modules that are relevant to their responsibilities.

---

## BR-017

Suppliers cannot access:

- Financial information
- Internal notes
- Client-only information
- Organisation settings

---

## BR-018

Every supplier action is recorded within the Workspace activity feed.

---

## BR-019

Removing a supplier immediately revokes Workspace access.

---

# Supplier Categories

The MVP includes:

- Venue
- Catering
- Photography
- Videography
- DJ
- Band
- Entertainment
- Floristry
- Decor
- Cake
- Transport
- Security
- Staffing
- Production
- Accommodation
- Celebrant
- Hair & Makeup
- Stationery
- Equipment Hire
- Other

Future versions allow organisations to create custom supplier categories.

---

# Main Success Scenario

1. Event Manager opens the Workspace.
2. Selects the **Suppliers** module.
3. Clicks **Invite Supplier**.
4. Searches existing suppliers.
5. Creates a supplier if one does not exist.
6. Selects supplier category.
7. Defines Workspace permissions.
8. Chooses which modules the supplier can access.
9. Adds an optional welcome message.
10. Sends invitation.
11. MiEvent creates an invitation.
12. Resend sends a branded invitation email.
13. Supplier authenticates with Clerk.
14. Supplier Dashboard opens.
15. Supplier confirms availability.
16. Activity is recorded.
17. Event Manager receives confirmation.

---

# Supplier Dashboard

Each supplier receives a tailored dashboard containing only relevant information.

Modules may include:

- Event Overview
- Timeline
- Arrival Schedule
- Tasks
- Messages
- Files
- Venue Information
- Contact Details
- Activity Feed

Modules not required for that supplier remain hidden.

---

# Alternative Flows

## Existing Supplier

Supplier already exists.

The existing supplier profile is linked to the Workspace.

Previous history remains available.

---

## Supplier Declines

Invitation status becomes **Declined**.

Event Manager is notified.

Replacement supplier workflow begins.

---

## Invitation Expires

Supplier receives no access.

Event Manager may resend the invitation.

---

## Supplier Requests Additional Access

Supplier submits a permission request.

Event Manager approves or rejects the request.

All actions are logged.

---

# Permissions

Possible permissions include:

- View Timeline
- View Files
- Upload Files
- View Messages
- Send Messages
- Complete Tasks
- Confirm Availability
- View Venue Information

Suppliers may never:

- Delete Workspace data
- Edit guest information
- Access financial records
- Invite other users
- Change permissions

---

# Data Created

This workflow creates:

- Supplier
- Workspace Supplier Membership
- Invitation
- Permission Set
- Activity Log
- Notification
- Conversation Thread
- Availability Status

---

# Domain Events

- SupplierInvited
- SupplierInvitationSent
- SupplierAccepted
- SupplierDeclined
- SupplierAvailabilityConfirmed
- SupplierUploadedFile
- SupplierCommentAdded
- SupplierRemoved

---

# Notifications

## Supplier

- Invitation Received
- Reminder
- Event Updated
- Task Assigned
- Timeline Changed

## Event Manager

- Supplier Accepted
- Supplier Declined
- Supplier Uploaded File
- Supplier Completed Task
- Supplier Posted Comment

## Client (Optional)

- Supplier Confirmed

---

# Failure Conditions

The workflow fails if:

- Email address is invalid.
- Invitation has expired.
- Authentication fails.
- Workspace is archived.
- Supplier has been removed.
- User lacks permission.

The Event Manager receives a clear explanation of the failure.

---

# Success Criteria

- Supplier receives invitation.
- Supplier authenticates successfully.
- Supplier accesses the Workspace.
- Permissions are correctly applied.
- Supplier confirms participation.
- Activity is recorded.
- Event Manager is notified.

---

# Business Metrics

Track:

- Invitation acceptance rate
- Average response time
- Supplier portal usage
- Task completion rate
- File upload completion
- Response SLA

---

# Automation Opportunities

Automatically:

- Send reminder if invitation not accepted within 48 hours.
- Request insurance certificates before the event.
- Remind suppliers to confirm arrival time.
- Send final event pack 7 days before the event.
- Send thank-you email after event completion.
- Archive supplier access after the event.

---

# AI Opportunities

Future AI capabilities:

- Detect scheduling conflicts.
- Recommend preferred suppliers.
- Suggest arrival times.
- Summarise supplier conversations.
- Flag missing documentation.
- Predict supplier delays using historical data.
- Recommend replacement suppliers.

---

# Risks

Potential risks:

- Incorrect permissions.
- Duplicate supplier records.
- Outdated contact details.
- Supplier ignores invitation.
- Conflicting event timelines.

Mitigation:

- Role-based permissions
- Duplicate detection
- Automated reminders
- Audit history
- Activity logging

---

# Future Enhancements

- Supplier Marketplace
- Supplier CRM
- Availability Calendar
- Digital Contracts
- Invoice Submission
- Payment Tracking
- Insurance Verification
- Performance Ratings
- AI Supplier Recommendations

---

# Related Requirements

- FR-023 Supplier Management
- FR-024 Supplier Portal
- FR-025 Supplier Permissions
- FR-026 Notifications

---

# Related UX Screens

- Suppliers Module
- Invite Supplier Dialog
- Supplier Dashboard
- Workspace Overview
- Timeline
- Tasks
- Files
- Messages

---

# Related Database Entities

- Supplier
- SupplierCategory
- WorkspaceSupplier
- Invitation
- Membership
- Permission
- Notification
- ActivityLog
- Conversation
- File

---

# Related APIs

See **Volume VI – API Specification**.

Expected endpoints include:

- Create Supplier
- Invite Supplier
- Update Supplier
- Remove Supplier
- List Suppliers
- Supplier Availability
- Supplier Documents

---

# Related Tests

Required automated tests:

- Supplier invitation
- Duplicate detection
- Permission validation
- Portal login
- Invitation expiry
- Reminder automation
- Activity logging
- Notification delivery

---

# Claude Code Guidance

The Supplier Portal should be operationally focused.

A supplier logging in on the morning of an event should immediately understand:

- Where they need to be.
- When they should arrive.
- Who they should contact.
- Which documents they require.
- What tasks remain outstanding.
- What has changed since their previous login.

Every unnecessary click increases operational risk.

Optimise the experience for:

- Mobile devices
- Fast loading
- Clear task completion
- Live collaboration
- Real-time updates

The Supplier module should be designed to support thousands of suppliers across multiple organisations while maintaining strict permission boundaries and excellent performance.

---

# End of Workflow
