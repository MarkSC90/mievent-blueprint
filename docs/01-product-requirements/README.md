# MiEvent Product Requirements

**Document ID:** MIE-PRD-001

**Version:** 1.0.0

**Status:** In Development

**Owner:** Product Team

---

# Purpose

This section defines the product vision, business goals, user requirements and functional expectations for the MiEvent platform.

It is the primary source of truth for what MiEvent should do and why those capabilities exist.

Every technical decision, user experience, API endpoint and database entity should ultimately trace back to the requirements defined within this section.

---

# Product Vision

MiEvent is a modern, collaborative, API-first SaaS platform designed to become the operating system for professional event businesses.

Rather than relying on spreadsheets, PDFs, email chains and disconnected software, MiEvent provides one secure, real-time workspace where organisers, clients, venues and suppliers collaborate throughout the lifecycle of an event.

Every event becomes a living workspace.

Every authorised user works from the same information.

Every update happens in real time.

---

# Mission Statement

To eliminate administrative complexity from event management by providing one beautiful, collaborative platform that enables event professionals to spend less time managing documents and more time creating exceptional events.

---

# Product Principles

Every feature developed for MiEvent must support one or more of these principles.

## One Source of Truth

There must only ever be one current version of an event.

No spreadsheets.

No PDFs.

No duplicated planning documents.

The Workspace is the source of truth.

---

## Collaboration by Default

Users should collaborate inside MiEvent rather than exchanging emails and attachments.

Clients, organisers, suppliers and venues all contribute to the same workspace with permissions determining what each user can view and edit.

---

## Beautiful Software

MiEvent should feel comparable to products such as Stripe, Linear, Vercel and Notion.

The interface should be calm, modern and intuitive.

Complexity should remain hidden.

---

## API First

Every feature available through the user interface must also be available through the public API.

MiEvent is designed as an OpenAPI-first platform.

This allows future integrations with websites, CRMs, AI services, accounting software and mobile applications without redesigning the platform.

---

## White Label Ready

Every organisation should be able to customise:

- Logo
- Business name
- Colours
- Email branding
- Portal branding
- Business information

Future versions will also support:

- Custom domains
- Custom login pages
- Custom email templates

---

## Mobile First

MiEvent must work equally well on desktop, tablet and mobile devices.

Venue managers, suppliers and organisers should be able to perform their work entirely from a mobile phone during an event.

---

## Accessibility

MiEvent should target WCAG 2.2 AA compliance.

Accessibility is a product requirement rather than an enhancement.

---

# Product Goals

The primary objectives of MiEvent are:

1. Replace spreadsheets and planning documents.
2. Improve collaboration between organisers, clients and suppliers.
3. Reduce administrative effort.
4. Improve client experience.
5. Provide a scalable white-label SaaS platform.
6. Support third-party integrations through an open API.
7. Deliver a premium software experience.

---

# Product Scope

MiEvent supports the complete lifecycle of professional event management including:

- Event Workspaces
- Client Portals
- Venue Portals
- Supplier Portals
- Guest Management
- Table Planning
- Timeline Management
- Catering Management
- Decor Management
- File Management
- Messaging
- Tasks
- Forms
- Activity History
- Notifications
- Reporting

Future versions will include:

- Payments
- CRM
- AI Assistant
- Automation Engine
- Marketplace
- Mobile Applications
- Accounting Integrations

---

# Repository Structure

This Product Requirements section contains:

```text
01-product-requirements/

README.md

executive-summary.md

market-analysis.md

problem-statement.md

product-philosophy.md

personas.md

user-journeys.md

functional-requirements.md

non-functional-requirements.md

mvp.md

roadmap.md
```

---

# Related Volumes

This section is closely related to:

- Volume II – User Experience
- Volume III – Design System
- Volume IV – Technical Architecture
- Volume V – Database Architecture
- Volume VI – API Specification

---

# Claude Code Guidance

This directory defines what MiEvent should become.

Claude Code should treat every document within this folder as product requirements rather than implementation guidance.

When technical decisions are required, implementation must remain consistent with the principles defined in this volume.

Future implementation documents should reference requirement identifiers defined here whenever possible.

---

**End of Document**
