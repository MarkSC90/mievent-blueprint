# Business Workflow 001

# Create Organisation

**Workflow ID:** BWF-001

**Document ID:** MIE-BWF-001

**Version:** 1.0.0

**Status:** Approved for Development

---

# Purpose

This workflow defines the complete lifecycle of creating a new organisation within MiEvent.

Creating an Organisation is the first action performed by every customer.

It provisions the company's digital workspace and establishes the foundation for all future events, users, branding and permissions.

The Organisation is the highest-level business entity within MiEvent.

Every Workspace belongs to exactly one Organisation.

---

# Goal

Allow a new event business to create an Organisation and immediately begin using MiEvent.

The process should require less than three minutes.

---

# Primary Persona

Organisation Owner

---

# Supporting Personas

None

---

# Success Criteria

The Organisation Owner can:

- Create their company
- Verify their email
- Configure branding
- Invite staff
- Create the first Workspace

without assistance.

---

# Trigger

A new customer registers through the MiEvent website.

---

# Preconditions

The user has:

- Internet connection
- Email address
- Clerk authentication account

---

# Inputs

Company Name

Trading Name (optional)

Business Type

Country

Timezone

Company Email

Telephone

Logo (optional)

Website (optional)

---

# Outputs

A new Organisation is created.

The Owner becomes Organisation Owner.

The default Workspace template becomes available.

Default permissions are created.

Brand settings are initialised.

Audit history begins.

---

# User Journey

## Step 1

User visits:

https://app.mievent.com

---

## Step 2

Clicks

Create Account

---

## Step 3

Clerk authentication

Options:

Google

Microsoft

Email

Apple

---

## Step 4

Email verification

Resend sends:

Verify Email

---

## Step 5

User creates Organisation

Fields:

Business Name

Business Type

Country

Timezone

Logo

---

## Step 6

Organisation saved

System generates:

Organisation ID

Slug

Default Theme

Default Roles

Workspace Template

Activity Feed

Notification Settings

---

## Step 7

User lands on

Organisation Dashboard

Empty State

"Create your first Event Workspace"

---

# Database Entities

Organisation

User

Membership

Role

Theme

Brand

Notification Preferences

Audit Log

API Key (future)

---

# API

POST /organisations

GET /organisations/{id}

PATCH /organisations/{id}

DELETE /organisations/{id}

---

# Authentication

Clerk

JWT

Session

Role

Owner

---

# Permissions Created

Organisation Owner

Organisation Admin

Event Manager

Staff

Client

Venue

Supplier

---

# Emails

Email 001

Verify Email

Resend

---

Email 002

Welcome to MiEvent

Contains

Getting Started

Documentation

Support

Create First Workspace

---

# Notifications

In-App

Welcome

Email Verified

Organisation Created

---

# Activity Feed

09:42

Organisation Created

09:42

Owner Added

09:42

Default Roles Created

09:43

Brand Initialised

---

# UI

Screen 1

Landing Page

↓

Register

↓

Email Verification

↓

Organisation Form

↓

Dashboard

---

# Components

shadcn/ui

Card

Input

Button

Select

Upload

Progress

Alert

---

# Validation

Business Name

Required

Minimum

3 characters

Maximum

120 characters

Country

Required

Timezone

Required

---

# Error Handling

Email already exists

Invalid logo

Authentication expired

Database unavailable

Slug unavailable

---

# Performance

Organisation Creation

<500ms

Dashboard Redirect

<1 second

---

# Security

Organisation ID

UUID

Every Organisation isolated

Multi-tenant

Row Level Security

Future SSO support

---

# Acceptance Criteria

Organisation created successfully.

Owner assigned.

Roles generated.

Brand created.

Workspace template generated.

Email sent.

Dashboard loaded.

Audit recorded.

---

# Future Enhancements

Stripe Billing

Teams

Departments

Multiple Brands

Custom Domains

Marketplace

Organisation AI

---

# Dependencies

Clerk

Prisma

PostgreSQL

Railway

Resend

Cloudflare R2

---

# Claude Code Implementation

## Objective

Implement complete Organisation onboarding.

## Suggested Structure

/app

/(auth)

/onboarding

/organisation

/dashboard

/components

/organisation

/forms

/layout

/lib

/actions

/prisma

---

## Required Components

CreateOrganisationForm

LogoUploader

BusinessTypeSelector

CountrySelector

TimezoneSelector

ProgressStepper

WelcomeCard

---

## Server Actions

createOrganisation()

createDefaultRoles()

createBrand()

createAuditLog()

sendWelcomeEmail()

createWorkspaceTemplate()

---

## Prisma Models

Organisation

User

Membership

Role

Brand

Theme

AuditLog

---

## Definition of Done

- [ ] Organisation can be created.
- [ ] Authentication completed.
- [ ] Email verified.
- [ ] Organisation saved.
- [ ] Default roles created.
- [ ] Branding initialised.
- [ ] Dashboard loads.
- [ ] Activity recorded.
- [ ] Welcome email sent.
- [ ] Unit tests passing.
- [ ] Accessibility verified.
- [ ] Mobile responsive.

---

# Related Documents

Product Philosophy

Problem Statement

Personas

Technical Architecture

Database Specification

API Specification

---

# End of Workflow
