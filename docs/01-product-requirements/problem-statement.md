# Problem Statement

**Document ID:** MIE-PRD-004  
**Version:** 1.0.0  
**Status:** Draft  

---

# Purpose

This document defines the core problems MiEvent exists to solve.

It translates the market opportunity into specific user, business and operational problems that the product must address.

Every feature in MiEvent should solve one or more of the problems described in this document.

---

# Primary Problem

Professional event businesses do not currently have one reliable, real-time source of truth for managing events.

Instead, event information is spread across spreadsheets, Word documents, PDFs, emails, WhatsApp messages, file storage platforms and individual staff members.

This creates unnecessary administration, version control issues, poor collaboration and operational risk.

MiEvent exists to replace fragmented event planning with a single collaborative Workspace.

---

# The Current Reality

A typical event may involve:

- An organiser
- A client
- A venue
- Caterers
- Florists
- Photographers
- DJs
- Entertainment suppliers
- Production teams
- Accommodation providers
- Transport providers
- Staff members
- Guests

Each stakeholder needs accurate information.

However, information is usually distributed manually.

Example documents include:

- Event brief
- Running order
- Guest list
- Seating plan
- Menu
- Dietary requirements
- Supplier list
- Venue access notes
- Contracts
- Invoices
- Risk assessments
- Floor plans
- Decor briefs

Each document changes repeatedly before the event.

Every change creates risk.

---

# Problem 1: Version Control

## Description

Event information changes constantly.

Guest numbers change.

Menus change.

Suppliers change.

Timings change.

Venue requirements change.

When these updates are stored in separate documents, nobody can be fully confident they are working from the latest version.

## Impact

Version control issues can cause:

- Incorrect guest numbers
- Wrong meal counts
- Supplier arrival mistakes
- Outdated timelines
- Incorrect table plans
- Missed client requests
- Poor event-day execution

## MiEvent Requirement

MiEvent must ensure that each event has one live Workspace where the latest information is always available to authorised users.

---

# Problem 2: Excessive Manual Administration

## Description

Event organisers spend too much time updating documents and sending information manually.

Administrative work often includes:

- Updating spreadsheets
- Exporting PDFs
- Sending revised documents
- Copying information between systems
- Chasing suppliers
- Confirming attendance
- Checking dietary details
- Updating timelines
- Sending reminders

## Impact

This reduces profitability and limits how many events a business can manage.

It also distracts organisers from higher-value work such as client experience, creative planning and supplier coordination.

## MiEvent Requirement

MiEvent must reduce repetitive administration through structured data, auto-save, notifications, reusable templates and live collaboration.

---

# Problem 3: Communication Overload

## Description

Event communication is often spread across:

- Email
- Phone calls
- WhatsApp
- SMS
- Social media messages
- PDFs
- Shared folders

Important decisions become buried in conversations.

Different stakeholders may receive different information.

## Impact

Communication overload creates:

- Missed updates
- Repeated questions
- Confusion over responsibilities
- Slow decision making
- Increased organiser workload

## MiEvent Requirement

MiEvent must centralise event communication inside the Workspace through messages, comments, mentions, notifications and activity history.

---

# Problem 4: Poor Client Visibility

## Description

Clients often do not have a clear view of planning progress.

They may need to ask:

- What information is still needed?
- Has the venue confirmed?
- Have suppliers received the running order?
- Is the guest list complete?
- Has the seating plan been updated?
- What tasks are outstanding?

## Impact

Poor visibility reduces confidence and increases support requests.

The organiser becomes the single point of information.

## MiEvent Requirement

MiEvent must provide clients with a secure portal where they can view event progress, complete required actions and collaborate with the organiser.

---

# Problem 5: Supplier Coordination

## Description

Suppliers often need only a small part of the full event plan.

For example:

A DJ may need:

- Venue address
- Arrival time
- Setup access
- Performance time
- Contact person
- Power requirements

A caterer may need:

- Guest count
- Dietary requirements
- Service time
- Menu
- Table plan

Currently these details are usually extracted manually and sent by email.

## Impact

Manual supplier coordination creates duplicated work and increases the chance of suppliers receiving incomplete or outdated information.

## MiEvent Requirement

MiEvent must allow suppliers to access role-specific portals showing only the information relevant to them.

---

# Problem 6: Venue Management

## Description

Venues need accurate, up-to-date information to prepare for events.

They may need:

- Arrival times
- Room layouts
- Guest counts
- Catering requirements
- Supplier access times
- Risk information
- Setup notes
- Event schedule

Without direct access to current information, venues rely on organisers to send updates manually.

## Impact

Venue teams may work from outdated schedules or miss critical changes.

## MiEvent Requirement

MiEvent must provide venue users with controlled access to relevant Workspace information.

---

# Problem 7: Lack of Audit Trail

## Description

When event information changes through email or documents, it is difficult to understand:

- Who changed something
- When it changed
- What the previous value was
- Whether the change was approved
- Who was notified

## Impact

Without an audit trail, disagreements and mistakes become harder to resolve.

## MiEvent Requirement

MiEvent must automatically log important changes inside each Workspace activity feed.

---

# Problem 8: Poor Scalability

## Description

Manual event management workflows may work for a small number of events.

However, they do not scale well when a business grows.

As volume increases, businesses require:

- Standardised templates
- Reusable workflows
- Role-based permissions
- Automation
- Reporting
- Multi-user collaboration
- Consistent client experience

## Impact

Without scalable systems, growth increases complexity rather than profitability.

## MiEvent Requirement

MiEvent must be designed as a scalable SaaS platform from day one.

---

# Problem 9: Lack of Integration

## Description

Event businesses already use websites, CRMs, accounting platforms, payment systems, email tools and file storage services.

Most event data is difficult to integrate with these systems.

## Impact

Teams duplicate data entry across multiple platforms.

Future automation becomes harder.

## MiEvent Requirement

MiEvent must be API-first and expose major platform capabilities through a documented OpenAPI interface.

---

# Problem 10: Inconsistent Client Experience

## Description

Without a structured platform, each event may be managed differently.

Different staff may use different documents.

Different clients receive different levels of communication.

Branding may be inconsistent.

## Impact

This makes the business harder to scale and weakens the client experience.

## MiEvent Requirement

MiEvent must provide configurable templates and white-label branding to ensure consistent delivery across all events.

---

# Problem Summary

| Problem | User Impact | MiEvent Response |
|---|---|---|
| Version control | Users work from outdated documents | Live Workspace |
| Manual admin | Time wasted updating documents | Structured data and automation |
| Communication overload | Updates are missed | Centralised messages and activity |
| Poor client visibility | Clients chase organisers | Client portal |
| Supplier coordination | Suppliers receive outdated info | Supplier portal |
| Venue coordination | Venues lack current details | Venue portal |
| No audit trail | Changes are hard to verify | Activity history |
| Poor scalability | Growth increases admin | SaaS architecture |
| Lack of integrations | Duplicate data entry | Open API |
| Inconsistent experience | Service quality varies | Templates and white labelling |

---

# Product Implications

The problem analysis creates the following product requirements:

1. MiEvent must be Workspace-first.
2. MiEvent must support live collaboration.
3. MiEvent must include role-based permissions.
4. MiEvent must include client, supplier and venue portals.
5. MiEvent must support reusable event templates.
6. MiEvent must provide a full activity history.
7. MiEvent must be API-first.
8. MiEvent must support white-label branding.
9. MiEvent must work across desktop, tablet and mobile.
10. MiEvent must reduce manual administration.

---

# Related Requirements

- FR-001 Workspace Creation
- FR-002 Event Templates
- FR-003 Client Portal
- FR-004 Supplier Portal
- FR-005 Venue Portal
- FR-006 Guest Management
- FR-007 Timeline Management
- FR-008 Activity History
- FR-009 Open API
- FR-010 White Labelling

---

# Used By

This document informs:

- User Experience Specification
- Technical Architecture
- Database Architecture
- API Specification
- Feature Specifications
- Security Model
- Roadmap

---

# Claude Code Guidance

Claude Code should treat this document as the problem foundation for MiEvent.

When implementing any feature, Claude Code should ensure the feature directly reduces one of the problems identified here.

Features that do not reduce fragmentation, administration, communication overhead or collaboration risk should be considered lower priority.

---

# Next Document

Continue to:

`product-philosophy.md`
