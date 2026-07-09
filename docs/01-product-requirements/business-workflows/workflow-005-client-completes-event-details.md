# Business Workflow 005

# Client Completes Event Details

**Workflow ID:** BWF-005

**Version:** 1.0.0

**Status:** Approved for Development

---

# Purpose

This workflow defines how a client provides the information required to begin planning an event.

Rather than exchanging Word documents, PDFs or email questionnaires, MiEvent collects structured information directly inside the Workspace.

The information entered by the client immediately becomes available to authorised users.

This workflow is the foundation for planning and should eliminate the need for manual data entry by the Event Manager.

---

# Business Goal

Allow clients to complete an event questionnaire that automatically populates the Workspace.

The process should feel conversational, simple and reassuring.

Clients should always know:

- what information is required,
- why it is required,
- how much they have completed,
- what happens next.

---

# Primary Persona

Client

---

# Supporting Personas

- Event Manager
- Organisation Administrator

---

# Trigger

The client has accepted their Workspace invitation.

The Event Manager requests completion of the Event Details questionnaire.

---

# Preconditions

- Workspace exists.
- Client has accepted invitation.
- Client is authenticated.
- Questionnaire is assigned to the Workspace.

---

# Business Rules

BR-001  
Every Workspace must contain one Event Details record.

BR-002  
Clients may edit event details until the Event Manager locks the questionnaire.

BR-003  
Changes are automatically saved.

BR-004  
Every change creates an Activity Log entry.

BR-005  
The Event Manager is notified when the questionnaire is completed.

BR-006  
Questionnaires support draft progress.

BR-007  
Required questions must be completed before submission.

---

# Questionnaire Sections

The default questionnaire contains:

## Event Overview

- Event Name
- Event Type
- Event Date
- Ceremony Time
- Reception Time
- Finish Time

---

## Venue Information

- Venue Name
- Address
- Indoor / Outdoor
- Accessibility Requirements
- Parking Information

---

## Client Information

- Primary Contact
- Secondary Contact
- Mobile Numbers
- Email Addresses

---

## Guest Information

- Expected Guests
- Children
- VIP Guests
- Evening Guests

---

## Catering

- Meal Style
- Dietary Notes
- Drinks Package
- Supplier Preferences

---

## Entertainment

- Ceremony Music
- Evening Music
- First Dance
- Speeches

---

## Theme

- Colour Palette
- Style
- Inspiration
- Pinterest Links
- Mood Boards

---

## Budget

Optional

- Estimated Budget
- Priority Areas

---

## Special Requirements

- Accessibility
- Religious Requirements
- Cultural Traditions
- Special Requests

---

# Main Success Scenario

1. Client logs into MiEvent.
2. Client opens their Workspace.
3. Client selects **Complete Event Details**.
4. Questionnaire opens.
5. Progress indicator displays completion percentage.
6. Client completes each section.
7. Changes auto-save.
8. Client uploads inspiration images where appropriate.
9. Client submits the questionnaire.
10. Event Manager receives notification.
11. Activity is recorded.
12. Workspace Overview updates automatically.

---

# Alternative Flows

## Client Saves Progress

The client leaves before completion.

Progress is saved automatically.

The questionnaire resumes from the previous position.

---

## Event Manager Requests Changes

The Event Manager unlocks the questionnaire.

Client receives a notification.

Client edits and resubmits.

---

## Questionnaire Updated

If the Event Manager adds additional questions before completion, new sections appear without losing existing answers.

---

# Data Created

- Event Details
- Questionnaire Responses
- Uploaded Images
- Activity Log
- Notifications

---

# Events Raised

- QuestionnaireStarted
- QuestionnaireUpdated
- QuestionnaireCompleted
- QuestionnaireUnlocked
- ActivityRecorded

---

# Notifications

Client

- Reminder to complete questionnaire.
- Confirmation of submission.

Event Manager

- Client started questionnaire.
- Client completed questionnaire.
- Questionnaire updated.

---

# Permissions

Client

- Read
- Create
- Update

Event Manager

- Read
- Update
- Lock
- Unlock
- Approve

Organisation Admin

- Full Access

---

# Success Criteria

✓ Client completes questionnaire.

✓ Data automatically populates Workspace.

✓ Event Manager receives notification.

✓ Activity recorded.

✓ No duplicate information required.

---

# Related Requirements

- FR-016 Event Questionnaire
- FR-017 Auto Save
- FR-018 Client Portal
- FR-019 Activity History

---

# Related UX Screens

- Client Dashboard
- Event Questionnaire
- Workspace Overview
- Notifications

---

# Related Database Entities

- Workspace
- EventDetails
- Questionnaire
- QuestionnaireResponse
- ActivityLog
- Notification
- File

---

# Future Enhancements

- AI-assisted questionnaire completion.
- Conditional questions.
- Voice input.
- Multi-language support.
- Smart recommendations.
- AI event planning assistant.

---

# Claude Code Guidance

This workflow should feel closer to onboarding than completing a form.

Use progressive disclosure, auto-save, inline validation and a visible progress indicator.

Avoid long pages of inputs.

Break the questionnaire into logical steps with smooth transitions.

The experience should feel comparable to onboarding in products like Stripe, Typeform or Notion rather than filling in a government form.

---

# End of Workflow
