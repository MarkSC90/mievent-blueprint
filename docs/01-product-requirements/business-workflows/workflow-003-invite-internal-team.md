# Business Workflow 003

# Invite Internal Team

**Workflow ID:** BWF-003  
**Version:** 1.0.0  
**Status:** Approved for Development  

---

# Purpose

This workflow defines how Organisation Owners and Organisation Administrators invite internal team members into MiEvent.

Internal team members may include event managers, coordinators, administrators, assistants, operations staff, sales staff and venue-side internal users.

Team invitations are fundamental to collaboration because MiEvent is designed as a shared operational platform rather than a single-user planning tool.

---

# Business Goal

Allow authorised users to invite internal team members, assign roles and provide immediate access to the correct Organisation and Workspaces.

The invitation process should be simple enough to complete in under two minutes.

---

# Primary Persona

Organisation Owner

---

# Supporting Personas

- Organisation Administrator
- Event Manager
- Staff Member

---

# Trigger

An Organisation needs to add another internal user to MiEvent.

Common triggers include:

- New employee joins the business.
- Existing employee needs MiEvent access.
- Temporary staff member supports an event.
- Admin wants to assign a Workspace to a colleague.
- Business scales beyond one organiser.

---

# Preconditions

- User is authenticated.
- User belongs to an Organisation.
- User has permission to invite team members.
- Organisation subscription allows additional users.
- Invitee has a valid email address.

---

# Inputs

Required:

- Email address
- Role

Optional:

- Full name
- Job title
- Assigned Workspaces
- Permission overrides
- Invitation message

---

# Main Success Scenario

1. User opens Organisation Settings.
2. User selects Team.
3. User clicks Invite Team Member.
4. User enters invitee email address.
5. User selects role.
6. User optionally assigns Workspaces.
7. User sends invitation.
8. MiEvent creates an invitation record.
9. Resend sends invitation email.
10. Invitee opens invitation link.
11. Invitee creates or signs into Clerk account.
12. MiEvent links the authenticated user to the Organisation.
13. Role permissions are applied.
14. Invitee lands on their dashboard.
15. Activity is recorded.

---

# Roles Available

Initial internal roles:

- Organisation Owner
- Organisation Administrator
- Event Manager
- Staff Member

Only an Organisation Owner can assign another Organisation Owner.

Organisation Administrators can invite:

- Event Managers
- Staff Members

Event Managers cannot invite Organisation-level users unless explicitly granted permission.

---

# Business Rules

- Every user must authenticate through Clerk.
- A user may belong to multiple Organisations in future versions.
- An invitation must expire after a configurable period.
- Expired invitations may be resent.
- Pending invitations should be visible in Team Settings.
- Revoked invitations cannot be used.
- Users cannot invite team members with greater permissions than their own.
- Organisation Owners cannot remove themselves if they are the only Owner.

---

# Alternative Flows

## Invitee Already Has Account

If the invitee already has a MiEvent account, the invitation links the existing account to the Organisation after acceptance.

## Invitation Expired

If the invitation has expired, the invitee sees a clear message and may request a new invitation.

## Invitation Revoked

If the invitation has been revoked, the invitee cannot join and must contact the Organisation.

## Subscription Limit Reached

If the Organisation has reached its user limit, the inviter is prompted to upgrade or remove inactive users.

---

# Data Created

This workflow creates or updates:

- Invitation
- User
- Membership
- Role Assignment
- Activity Log
- Notification

---

# Events Raised

The following domain events are published:

- TeamInvitationCreated
- TeamInvitationSent
- TeamInvitationAccepted
- MembershipCreated
- RoleAssigned
- ActivityRecorded

---

# Notifications

Email notifications:

- Team invitation email
- Invitation accepted confirmation to inviter

In-app notifications:

- Invitation sent
- New team member joined

Activity feed entries:

- User invited team member
- Invitee accepted invitation
- Role assigned

---

# Failure Conditions

The workflow must fail gracefully if:

- Email address is invalid.
- User lacks permission to invite.
- Organisation subscription limit is reached.
- Invitation token is invalid.
- Invitation has expired.
- Clerk authentication fails.
- Database write fails.

The user should receive a clear, non-technical explanation.

---

# Success Criteria

The workflow is complete when:

- Invitation is sent.
- Invitee can authenticate.
- Membership is created.
- Correct role is applied.
- Dashboard access reflects assigned permissions.
- Activity history records the process.

---

# Related Requirements

- FR-003 Team Management
- FR-010 Permissions
- FR-011 Invitations
- FR-012 Notifications

---

# Related UX Screens

- Organisation Settings
- Team Management
- Invite Team Member Dialog
- Invitation Acceptance Page
- Dashboard

---

# Related Database Entities

- Organisation
- User
- Membership
- Role
- Invitation
- ActivityLog
- Notification

---

# Related APIs

See Volume VI – API Specification.

Expected API capabilities:

- Create invitation
- Accept invitation
- Revoke invitation
- Resend invitation
- List team members
- Update role
- Remove member

---

# Related Tests

See Volume XI – Testing Strategy.

Required tests include:

- Owner can invite admin.
- Admin can invite staff.
- Staff cannot invite users.
- Expired invitations fail.
- Revoked invitations fail.
- Role assignment is enforced.
- User cannot assign higher permission than their own.

---

# Claude Code Implementation Guidance

Claude Code should implement this workflow as a secure team onboarding process.

The UI must not be the only permission boundary.

Every invitation, role assignment and membership creation must be validated server-side.

Use Resend for invitation emails and Clerk for authentication.

Do not create duplicate users when the invitee already has a Clerk account.

---

# End of Workflow
