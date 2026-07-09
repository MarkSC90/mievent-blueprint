# Product Philosophy

**Document ID:** MIE-PRD-005  
**Version:** 1.0.0  
**Status:** Draft  

---

# Purpose

This document defines the guiding philosophy behind MiEvent.

While the Product Requirements describe **what** MiEvent should do, this document defines **how** it should think.

Every design decision, engineering decision and product decision should align with the principles contained within this document.

The philosophy is intended to remain stable as the platform evolves.

---

# Introduction

MiEvent is not simply another event management application.

It is designed to become the operating system for professional event businesses.

Most software attempts to digitise existing paperwork.

MiEvent aims to eliminate paperwork altogether.

Rather than storing documents, MiEvent stores structured information.

Rather than sending updated files, users collaborate on live data.

The platform should continuously reduce friction while increasing visibility and collaboration.

---

# Core Philosophy

The following principles are considered fundamental.

Every new feature should reinforce one or more of these principles.

---

# Principle 1 — One Workspace

Every event exists within one Workspace.

Everything associated with that event belongs inside that Workspace.

This includes:

- Client information
- Venue details
- Suppliers
- Guest lists
- Seating plans
- Timelines
- Tasks
- Files
- Contracts
- Messages
- Notes
- Activity

Users should never need to search outside the Workspace for event information.

---

# Principle 2 — One Source of Truth

MiEvent replaces duplicated documents with structured, shared information.

There should never be multiple "current" versions of:

- Guest lists
- Timelines
- Seating plans
- Supplier details
- Running orders
- Venue notes

Every authorised user should see the same information in real time.

---

# Principle 3 — Collaboration Over Communication

Traditional event management relies on communication.

MiEvent prioritises collaboration.

Instead of emailing revised documents, users update the Workspace.

Instead of asking for the latest version, users open the Workspace.

Instead of distributing information, the platform shares information automatically.

Communication becomes contextual rather than administrative.

---

# Principle 4 — Simplicity Creates Confidence

Professional software should reduce cognitive load.

MiEvent should never overwhelm users with unnecessary options.

Interfaces should present only the information required to complete the current task.

Advanced functionality should appear progressively as required.

Every interaction should feel intentional.

---

# Principle 5 — Beautiful Software Matters

Design is not decoration.

Design communicates quality.

Users should immediately feel confident when using MiEvent.

The interface should feel:

- Calm
- Spacious
- Fast
- Professional
- Trustworthy

Design inspiration includes:

- Stripe
- Linear
- Vercel
- Notion
- Revolut

MiEvent should never resemble traditional enterprise software.

---

# Principle 6 — API First

Every capability available through the user interface should also be available programmatically.

This allows organisations to integrate MiEvent with:

- Websites
- CRM platforms
- Accounting software
- AI assistants
- Mobile applications
- Automation platforms

The API is considered a first-class product.

---

# Principle 7 — Permissions by Default

Every user should only access the information they require.

Permissions are applied to:

- Organisations
- Workspaces
- Modules
- Records
- Actions

Security should never depend solely upon interface restrictions.

Authorisation must be enforced throughout the platform.

---

# Principle 8 — White Label by Design

MiEvent is designed to power many independent event businesses.

Each organisation should feel as though it owns the platform.

Supported branding includes:

- Logo
- Business details
- Colours
- Email branding
- Portal branding

Future releases should support:

- Custom domains
- Custom login experiences
- Organisation-specific templates

---

# Principle 9 — Live by Default

MiEvent is a collaborative platform.

Changes should be visible immediately.

Examples include:

- Guest RSVP updates
- Timeline changes
- Supplier confirmations
- Task completion
- Seating plan adjustments
- File uploads

Users should never manually refresh data.

---

# Principle 10 — Modular Architecture

Every major feature should exist as an independent module.

Examples include:

- Guest Management
- Table Planning
- Venue Management
- Supplier Management
- Catering
- Timeline
- Messaging
- Tasks

Future functionality should integrate without redesigning the application.

---

# Principle 11 — Accessibility is a Requirement

Accessibility is not an enhancement.

MiEvent should target WCAG 2.2 AA compliance from the beginning.

The platform should support:

- Keyboard navigation
- Screen readers
- High contrast
- Reduced motion
- Accessible forms
- Clear focus indicators

---

# Principle 12 — Mobile Enables Operations

Many users operate while travelling or working on-site.

The mobile experience must support:

- Guest check-in
- Timeline viewing
- Supplier updates
- Venue communication
- Task management
- File access

Mobile users should not receive a reduced experience.

---

# Product Decision Framework

Before introducing a new feature, the following questions should be asked.

1. Does this reduce administration?
2. Does this improve collaboration?
3. Does this strengthen the Workspace?
4. Does this simplify the user experience?
5. Can this be exposed through the API?
6. Does this support future scalability?
7. Can this be reused across event types?

If the answer to most questions is "no", the feature should be reconsidered.

---

# Success Statement

If MiEvent succeeds:

- Event organisers stop using spreadsheets.
- Clients collaborate rather than email.
- Suppliers rely on their portal instead of PDFs.
- Venues trust live Workspace information.
- Every stakeholder works from one source of truth.

The software becomes invisible because it simply works.

---

# Philosophy Summary

MiEvent is built on a simple belief:

> **People should spend their time creating memorable events, not managing documents.**

Every future product decision should reinforce that belief.

---

# Related Documents

- Executive Summary
- Market Analysis
- Problem Statement
- Personas
- User Journeys
- Functional Requirements

---

# Used By

This document directly influences:

- User Experience
- Design System
- Technical Architecture
- Database Design
- API Design
- Feature Specifications

---

# Claude Code Guidance

This document is the philosophical foundation of MiEvent.

When implementation decisions involve trade-offs, prefer the option that:

- reduces complexity,
- improves collaboration,
- maintains a single source of truth,
- and keeps the Workspace at the centre of the experience.

---

# Next Document

`personas.md`
