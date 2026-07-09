# Functional Requirements

**Document ID:** MIE-PRD-007

**Version:** 1.0.0

**Status:** Approved for Development

---

# Purpose

This document defines the functional capabilities that MiEvent must provide.

Functional Requirements (FRs) describe **what the platform must do**.

These requirements are implementation independent and will be referenced throughout the MiEvent Engineering Blueprint.

Every workflow, UX specification, API endpoint, database entity and automated test should trace back to one or more Functional Requirements.

---

# Requirement Structure

Each requirement has:

- Unique Identifier
- Name
- Description
- Priority
- Related Workflows
- Acceptance Criteria

Priority Levels:

- Critical
- High
- Medium
- Low

---

# Organisation

## FR-001

### Organisation Management

**Priority:** Critical

The platform shall allow organisations to be created, updated, archived and managed.

Related Workflows:

- BWF-001

---

## FR-002

### Multi-Tenant Isolation

**Priority:** Critical

Every organisation shall have isolated data.

No organisation shall access another organisation's data.

---

## FR-003

### Organisation Branding

**Priority:** High

Each organisation shall support:

- Logo
- Colours
- Business Details
- Email Branding
- White-labelled Client Portal

---

## FR-004

### Team Management

Organisation Owners and Administrators shall manage team members.

Includes:

- Invite
- Remove
- Change Role
- Suspend Access

Related Workflow:

- BWF-003

---

# Authentication

## FR-005

Authentication

Users shall authenticate using Clerk.

Supported methods:

- Email
- Google
- Microsoft
- Apple

Future:

- Passkeys

---

## FR-006

Role-Based Access

Every authenticated user shall receive permissions based upon:

Organisation

Workspace

Role

Custom Permission

---

# Workspace

## FR-007

Workspace Creation

Users shall create unlimited Event Workspaces.

Related Workflow:

- BWF-002

---

## FR-008

Workspace Templates

Users shall create reusable Workspace templates.

---

## FR-009

Workspace Lifecycle

Every Workspace shall progress through:

Draft

Planning

Confirmed

Live Event

Completed

Archived

---

# Clients

## FR-010

Client Portal

Clients shall receive a dedicated portal.

Related Workflow:

- BWF-004

---

## FR-011

Client Questionnaires

Clients shall complete dynamic questionnaires.

Related Workflow:

- BWF-005

---

## FR-012

Approvals

Clients shall approve:

- Timelines
- Guest Lists
- Seating Plans
- Supplier Choices

---

# Venues

## FR-013

Venue Portal

Venue users shall receive a dedicated operational portal.

Related Workflow:

- BWF-006

---

## FR-014

Venue Confirmation

Venues shall confirm:

Availability

Access

Room Layout

Supplier Access

---

# Suppliers

## FR-015

Supplier Management

The platform shall manage suppliers.

Related Workflow:

- BWF-007

---

## FR-016

Supplier Portal

Every supplier shall receive role-specific access.

---

## FR-017

Supplier Availability

Suppliers shall confirm:

Availability

Arrival

Completion

---

# Guests

## FR-018

Guest Management

The platform shall manage guests.

Related Workflow:

- BWF-008

---

## FR-019

CSV Import

Users shall import guests using CSV.

Validation required.

---

## FR-020

RSVP Management

Guests shall support:

Pending

Accepted

Declined

Maybe

Future:

QR RSVP

---

## FR-021

Dietary Requirements

Each Guest shall store:

Dietary Requirements

Meal Choice

Allergies

---

## FR-022

Guest Tags

Guests shall support unlimited tags.

Examples:

VIP

Family

Bride

Groom

Child

Press

---

# Table Planning

## FR-023

Table Planning

Users shall visually assign guests to tables.

---

## FR-024

Seat Assignment

Guests shall occupy one seat.

---

## FR-025

Capacity Validation

Tables shall validate capacity automatically.

---

# Timeline

## FR-026

Timeline Management

Users shall create event timelines.

---

## FR-027

Timeline Notifications

Relevant users shall receive timeline updates.

---

# Tasks

## FR-028

Task Management

Users shall:

Create

Assign

Complete

Comment

Track

---

## FR-029

Task Notifications

Task assignments generate notifications.

---

# Messaging

## FR-030

Workspace Messaging

Every Workspace includes messaging.

Supports:

Comments

Mentions

Attachments

Threads

---

# Files

## FR-031

File Management

Users shall upload:

Images

PDF

Documents

Videos

---

## FR-032

File Versioning

Future release.

---

# Notifications

## FR-033

Notification Centre

In-app notifications.

---

## FR-034

Email Notifications

Resend handles email delivery.

---

# Search

## FR-035

Global Search

Search:

Events

Guests

Suppliers

Clients

Messages

Files

Tasks

---

# Reporting

## FR-036

Dashboard Reporting

Organisation dashboards include:

Upcoming Events

Tasks

Guest Counts

Supplier Status

Revenue (future)

---

# API

## FR-037

OpenAPI

Every major platform capability shall be available via REST API.

---

## FR-038

API Authentication

JWT

API Keys

OAuth (future)

---

# Audit

## FR-039

Activity History

Every important action shall be recorded.

---

# White Labelling

## FR-040

Organisation Branding

The platform shall support:

Logo

Colours

Business Details

Emails

Portal Branding

Future:

Custom Domains

---

# General Acceptance Criteria

The platform shall:

- Support unlimited organisations.
- Support unlimited Workspaces.
- Support real-time collaboration.
- Auto-save changes.
- Operate on desktop, tablet and mobile.
- Maintain WCAG 2.2 AA accessibility.
- Support OpenAPI.
- Maintain full audit history.
- Support white labelling.
- Be deployable on Railway.

---

# Traceability

Every future document should reference these requirement IDs.

Examples:

UX-014 references FR-018.

API-032 references FR-018.

DB-011 references FR-018.

TEST-007 validates FR-018.

This provides full traceability throughout the MiEvent Engineering Blueprint.

---

# Related Documents

Business Workflows

Personas

Problem Statement

Product Philosophy

---

# Next Document

Continue to:

non-functional-requirements.md
