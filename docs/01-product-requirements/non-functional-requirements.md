# Non-Functional Requirements

**Document ID:** MIE-PRD-008

**Version:** 1.0.0

**Status:** Approved for Development

---

# Purpose

This document defines the quality attributes and operational standards that MiEvent must achieve.

Unlike Functional Requirements, which describe **what** the platform does, Non-Functional Requirements (NFRs) define **how well** it must perform.

These requirements are mandatory across every module, workflow and API.

---

# Scope

This document applies to:

- Web Application
- Public API
- Authentication
- Mobile Experience
- Admin Portal
- Client Portal
- Venue Portal
- Supplier Portal
- Infrastructure
- Integrations

---

# Performance

## NFR-001

Page loads should complete in under **2 seconds** on a standard broadband connection.

---

## NFR-002

Interactive actions should respond in under **300ms** wherever possible.

---

## NFR-003

Real-time updates should propagate to connected users within **1 second**.

---

## NFR-004

The platform shall support at least **500 concurrent users** in the MVP, with an architecture capable of scaling to **50,000+ users**.

---

# Availability

## NFR-005

Target uptime:

**99.9%**

excluding planned maintenance.

---

## NFR-006

Deployments must occur without extended downtime.

---

## NFR-007

Automatic monitoring and health checks shall be enabled.

---

# Scalability

## NFR-008

The application shall support horizontal scaling.

---

## NFR-009

All uploaded files shall use scalable object storage.

Cloudflare R2 is the preferred storage provider.

---

## NFR-010

The database shall support millions of records without architectural redesign.

---

# Security

## NFR-011

Authentication shall be provided exclusively by Clerk.

---

## NFR-012

All API endpoints require authentication unless explicitly public.

---

## NFR-013

Role-Based Access Control (RBAC) is mandatory.

---

## NFR-014

Row-Level Security principles shall be enforced throughout the application.

---

## NFR-015

Passwords are never stored by MiEvent.

Authentication is delegated to Clerk.

---

## NFR-016

Sensitive information must be encrypted in transit using TLS.

---

## NFR-017

Sensitive data at rest shall be encrypted where supported.

---

# Privacy

## NFR-018

MiEvent shall support GDPR compliance.

---

## NFR-019

Users shall be able to export their personal data.

---

## NFR-020

Users shall be able to request deletion of personal data.

---

# Accessibility

## NFR-021

The platform shall target **WCAG 2.2 AA** compliance.

---

## NFR-022

Keyboard navigation is mandatory.

---

## NFR-023

Screen readers must be supported.

---

## NFR-024

Colour contrast must meet WCAG standards.

---

# Reliability

## NFR-025

Auto-save is mandatory.

Users should never lose work due to accidental refresh or navigation.

---

## NFR-026

Soft delete shall be used for business-critical entities.

---

## NFR-027

Activity history shall provide a complete audit trail.

---

# User Experience

## NFR-028

The interface should feel comparable to:

- Stripe
- Linear
- Notion
- Revolut
- Vercel

---

## NFR-029

No screen should require training to understand.

---

## NFR-030

Progressive disclosure should be used to reduce complexity.

---

## NFR-031

Dark Mode shall be supported.

---

## NFR-032

Responsive layouts shall support:

- Desktop
- Laptop
- Tablet
- Mobile

---

# API

## NFR-033

Every major feature shall be accessible through the Public API.

---

## NFR-034

OpenAPI documentation shall be automatically generated.

---

## NFR-035

API responses shall follow a consistent schema.

---

# Infrastructure

## NFR-036

Primary Hosting:

Railway

---

## NFR-037

Primary Database:

PostgreSQL

---

## NFR-038

ORM:

Prisma

---

## NFR-039

Email Delivery:

Resend

---

## NFR-040

Authentication:

Clerk

---

## NFR-041

File Storage:

Cloudflare R2

---

## NFR-042

Frontend:

Next.js (App Router)

---

## NFR-043

Language:

TypeScript

Strict Mode enabled.

---

## NFR-044

UI Library:

shadcn/ui

---

## NFR-045

Components:

21st.dev

---

# Logging

## NFR-046

Every critical action shall generate an audit log.

---

## NFR-047

Application errors shall be logged with sufficient diagnostic information.

---

# Maintainability

## NFR-048

Code shall follow a modular architecture.

---

## NFR-049

Business logic shall not exist inside React components.

---

## NFR-050

Reusable components shall be prioritised.

---

# Testing

## NFR-051

Critical workflows require automated tests.

---

## NFR-052

All APIs require integration tests.

---

## NFR-053

Accessibility testing forms part of CI.

---

# Deployment

## NFR-054

Deployment must be automated using GitHub Actions.

---

## NFR-055

Every deployment must support rollback.

---

# Monitoring

## NFR-056

Application monitoring shall detect:

- Downtime
- Failed jobs
- Slow responses
- API failures

---

# Future Requirements

Future versions should support:

- Multi-region deployment
- AI Copilot
- Offline mode
- Native mobile apps
- Enterprise SSO
- Webhooks
- GraphQL API
- Marketplace

---

# Success Criteria

MiEvent shall be:

- Fast
- Secure
- Reliable
- Accessible
- Scalable
- Beautiful
- API-first
- Mobile-first
- White-label
- Easy to maintain

---

# Related Documents

- Functional Requirements
- Product Philosophy
- Technical Architecture
- Security Specification
- Deployment Guide

---

# Traceability

Every architecture, deployment and engineering decision must reference one or more NFRs.

Examples:

API-014 → NFR-033

DB-021 → NFR-010

UX-005 → NFR-030

ADR-004 → NFR-040

---

# Claude Code Guidance

These Non-Functional Requirements are mandatory.

If implementation choices conflict with these requirements, Claude Code should favour compliance with the NFRs unless a newer Architecture Decision Record supersedes them.

Performance, accessibility, maintainability and security are not optional enhancements—they are core product requirements.

---

# End of Document
