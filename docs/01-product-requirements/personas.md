# User Personas

**Document ID:** MIE-PRD-006

**Version:** 1.0.0

**Status:** Draft

---

# Purpose

This document defines the primary user personas for MiEvent.

Unlike traditional marketing personas, these personas describe operational users of the platform.

Each persona directly influences:

- User Experience
- Navigation
- Permissions
- Database Design
- API Security
- Feature Development
- Mobile Experience

Every feature within MiEvent should have at least one primary persona.

---

# User Hierarchy

```text
Organisation

├── Organisation Owner

├── Organisation Admin

├── Event Manager

├── Staff

├── Client

├── Venue

├── Supplier

└── Guest (Future)
```

---

# Persona 01

# Organisation Owner

## Description

The business owner.

Usually owns the event company.

Responsible for growth, staff and overall delivery.

Examples include:

- Wedding Company Owner
- Events Agency Director
- Funeral Company Owner
- Hospitality Business Owner

---

## Responsibilities

Create organisation

Manage branding

Invite staff

Create workspaces

Manage subscriptions

View reporting

Manage templates

Approve major changes

---

## Goals

Grow the business

Reduce administration

Increase profitability

Standardise operations

Improve client experience

---

## Frustrations

Too much administration

Staff inconsistency

Multiple software systems

Difficult reporting

Too many spreadsheets

---

## Permissions

Full system access.

Can access every workspace.

Can manage billing.

Can manage branding.

Can manage API keys.

Can manage templates.

---

## Primary Screens

Dashboard

Reports

Templates

Organisation Settings

Team

Workspace Overview

---

## Mobile Usage

Medium

Mostly desktop.

---

# Persona 02

# Organisation Administrator

## Description

Responsible for day-to-day administration.

Usually office based.

Supports multiple Event Managers.

---

## Responsibilities

Manage staff

Manage templates

Manage clients

Manage suppliers

Manage events

Review activity

Support planners

---

## Permissions

Everything except:

Billing

Organisation ownership

Subscription

---

## Primary Screens

Dashboard

Calendar

Workspaces

Clients

Suppliers

Reports

---

# Persona 03

# Event Manager

## Description

The primary operational user.

Creates and manages events.

Owns client relationships.

Coordinates suppliers.

Uses MiEvent every day.

This is the most important persona.

---

## Responsibilities

Create event

Invite client

Invite suppliers

Manage guest list

Manage timeline

Manage venue

Manage catering

Assign tasks

Upload files

Approve changes

Complete planning

---

## Success Measures

Happy clients

Delivered events

Reduced administration

No missed updates

Accurate timelines

---

## Permissions

Full access to assigned Workspaces.

Cannot manage organisation settings.

---

## Primary Screens

Workspace

Timeline

Guests

Tables

Suppliers

Tasks

Messages

Files

Venue

---

## Mobile Usage

Very High

Uses MiEvent throughout live events.

---

# Persona 04

# Client

## Description

Pays for the event.

Collaborates with organiser.

Should feel involved without being overwhelmed.

---

## Responsibilities

Complete forms

Review plans

Approve decisions

Manage guests

Update RSVP

Review seating

Communicate

Upload inspiration

---

## Permissions

Own Workspace only.

Cannot view internal notes.

Cannot manage suppliers directly.

Cannot access reporting.

---

## Goals

Understand progress.

Feel informed.

Avoid chasing organisers.

---

## Primary Screens

Overview

Timeline

Guests

Messages

Files

Approvals

---

# Persona 05

# Venue Manager

## Description

Represents the venue hosting the event.

Needs operational information.

---

## Responsibilities

Confirm setup

Confirm access

Review timeline

Review suppliers

Review guest numbers

Manage venue requirements

---

## Permissions

Venue module

Timeline

Guest numbers

Supplier arrivals

Files

Messages

---

# Persona 06

# Supplier

## Description

External supplier delivering services.

Examples

DJ

Florist

Photographer

Caterer

Celebrant

Entertainment

Production

Transport

---

## Responsibilities

Accept invitation

Confirm availability

Upload documents

Review timeline

Communicate

Complete tasks

---

## Permissions

Own assignments only.

Cannot view financial information.

Cannot edit guest lists.

Cannot edit seating plans.

---

## Primary Screens

Supplier Dashboard

Timeline

Messages

Tasks

Files

---

## Mobile Usage

Extremely High

---

# Persona 07

# Staff Member

## Description

Internal employee.

Supports Event Manager.

---

## Responsibilities

Guest management

Setup

Supplier coordination

Tasks

File uploads

Venue support

---

## Permissions

Assigned Workspaces only.

Limited administration.

---

# Persona 08

# Guest (Future)

## Description

Attendee.

Future versions.

May receive:

Digital invitation

RSVP

Table

Directions

Schedule

QR check-in

Dietary form

---

# Persona Relationships

```text
Owner

↓

Organisation

↓

Event Manager

↓

Workspace

↓

Client

↓

Venue

↓

Suppliers

↓

Guests
```

---

# Design Implications

Organisation Owners require dashboards.

Event Managers require speed.

Clients require simplicity.

Suppliers require clarity.

Venues require operational information.

Guests require minimal interaction.

Every interface should prioritise the needs of its primary persona.

---

# Permission Philosophy

Permissions should always follow least privilege.

Users only access information necessary for their role.

No user should ever see information unrelated to their responsibilities.

---

# Future Personas

Future releases may introduce:

Accountant

Sales

CRM User

Marketing

Inventory Manager

Volunteer

Temporary Staff

Sponsor

Partner

API Consumer

AI Agent

---

# Success Criteria

MiEvent should allow every persona to complete their work without training.

Every role should have a tailored experience.

No persona should feel overwhelmed by features intended for another role.

---

# Related Documents

- Executive Summary
- Product Philosophy
- User Journeys
- UX Specification
- Permissions Model
- Database Design

---

# Used By

This document directly influences:

- Authentication
- Authorisation
- Navigation
- UI Design
- API Security
- Database Relationships
- Notifications
- Mobile Design

---

# Claude Code Guidance

These personas are authoritative.

When implementing any screen, determine the primary persona first.

Every interface should be optimised for the user who performs that task most frequently.

Role-specific dashboards, permissions and navigation should be generated from this document rather than hard-coded independently.

---

# Next Document

`user-journeys.md`
