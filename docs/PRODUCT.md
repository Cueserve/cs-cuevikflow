# PRODUCT.md — Product Concept

**Owner:** Viral Parikh
**Last updated:** 2026-09-30
**Source of truth for:** what CuevikFlow is, why it exists, who it serves, and its intended scope — an
AI-assisted platform that gives small accounting and tax firms a single workspace to keep a trusted
record of each client and its jobs, deadlines, documents, and communication, so they can stop
running core work from spreadsheets, inboxes, and disconnected tools.

> Derived from: (none — starting point)
> Downstream: README.md, docs/PRD.md

---

## Contents

- [1. Overview](#1-overview)
- [2. Target Users](#2-target-users)
- [3. Features](#3-features)
- [3A. Decision Placeholders](#3a-decision-placeholders)
- [4. Scope (In / Out)](#4-scope-in-out)
- [5. Success Criteria](#5-success-criteria)
- [6. Anti-Patterns](#6-anti-patterns)
- [7. Roadmap](#7-roadmap)
- [Glossary](#glossary)

## 1. Overview

### Vision

Every small accounting and tax firm delivers every client's work on time, from
one trusted record that any staff member can pick up without a handover.

### Problem Statement

Accounting firms of 2–20 staff track their clients, the people behind those
clients, and their recurring work across spreadsheets, email inboxes, shared
drives, and staff memory. As a result:

- Owners cannot see which jobs are overdue or at risk until a client or a
  regulator raises it.
- Recurring jobs are re-created by hand each period, so a missed setup becomes
  a missed deadline.
- Staff chase clients for documents and information by email, with no record of
  what was asked, when, or what came back.
- Knowledge of which people act for which client organisations, and what was
  last discussed, sits with individual staff; absence or turnover stalls work.
- Clients receive repeated and inconsistent requests for the same information.

### Objective

CuevikFlow gives a small accounting firm one record of its leads, prospects, and
client organisations, the people linked to them, and all client work — one-off
and recurring. It MUST let the firm meet deadlines, collect what it needs from
clients, and let the owner see the state of every job without asking anyone.

### Description

The firm records each lead, prospect, and client as an organisation or an
individual and moves it through Lead → Prospect → Client → Inactive or Archived.
People link to the organisations they act for, and organisations link to related
organisations, so the firm sees a client group as a whole. An Engagement is a
one-time service contract stating which Jobs a client needs and when; Jobs
recur on a schedule, and each occurrence carries a checklist of Tasks assigned
to staff with due dates. Engagements are optional by default, and a firm MAY
require every Job to belong to one. Firms build Engagements and Jobs from their
own templates or copy and edit a Cuevik-supplied starter library. CuevikFlow
reminds assignees and escalates to managers as due dates approach or pass.
Staff email client contacts from templates and request documents and
information through links that need no client login; every exchange is logged
against the client. Artificial intelligence (AI) flags at-risk jobs, suggests
assignees, classifies client uploads, extracts client-document data into
firm-defined outputs, and summarises and drafts — staff review every AI output
before use. Dashboards show each person their work and owners firm-wide
deadlines, overdue work, and workload.

## 2. Target Users

CuevikFlow is for accounting and tax firms of 2–20 staff that deliver recurring
client work such as bookkeeping, payroll, periodic tax filings, and year-end
accounts.

- **Firm owner / partner** — cannot see which jobs are overdue or at risk, or
  which leads and prospects are going cold, without asking staff; carries the
  consequence of every missed deadline.
- **Manager** — assigns and reviews work across staff but has no single view of
  team workload or of which recurring jobs are ready for the next period, so
  rebalancing and review happen by chasing people.
- **Staff (accountant or administrator)** — does the jobs and tasks; loses time
  re-creating recurring work, chasing clients by email for documents, and
  searching inboxes for what a client sent or said.
- **Client contact** (a person acting for a client organisation, or an
  individual client) — receives repeated, scattered requests from the firm and
  answers them by email attachment; uses CuevikFlow only through emails and
  request links, with no login.

## 3. Features

- **Client relationships** — one record per lead, prospect, and client
  (organisation or individual) from first contact to Inactive or Archived,
  showing who acts for each organisation and which organisations form a group,
  so any staff member can pick up any client.
- **Engagements and recurring jobs** — service contracts that set out which jobs
  a client needs and when; jobs that recur on schedule with task checklists;
  comments, @mentions, and notifications on the work; and manager review and
  sign-off before a job is complete, so recurring work sets itself up and
  nothing is marked done unreviewed.
- **Templates** — firm-owned Engagement and Job templates plus a Cuevik starter
  library the firm copies and adapts, so every job of the same kind runs the
  same way.
- **Deadline reminders and escalation** — reminders to assignees and escalation
  to managers as due dates approach or pass, so deadlines are caught before they
  are missed.
- **Client requests and documents** — requests for documents and information
  that client contacts answer through a link without logging in, with automatic
  reminders to the client until answered and files kept against the client and
  job, replacing email chasing and scattered attachments.
- **Client communication** — templated email to client contacts, with every
  message, request, call, meeting, and note logged against the client, and later
  two-way email filed automatically by AI, so the firm's full history with a
  client is in one place.
- **Work visibility and reporting** — personal and firm-wide dashboards
  (deadlines, overdue work, at-risk jobs, team workload) plus exportable reports
  on deadline compliance, workload, and throughput over time, so owners see
  both today's state and the trend.
- **AI assistance** — at-risk job detection, assignee suggestions, classification
  of client uploads, extraction of client-document data into firm-defined
  outputs, and summaries and drafts, all reviewed by staff before use, removing
  manual sorting, re-keying, and first-draft writing.
- **Proposals** — proposals and engagement acceptance that convert a prospect
  into a client, so winning work and starting work happen in the same system.
- **Time and billing** — time logged against jobs and tasks, and invoices raised
  from jobs and time, so firms bill from the same record they work from.
- **Team, roles and access** — Owner, Manager, and Staff roles; sensitive fields
  restricted by role; and an audit trail of who changed what and when, so each
  person sees what their job needs and the firm can answer "who changed this?"
- **Firm configuration** — custom fields on clients, jobs, and tasks, and firm
  branding on client-facing emails and request links, so firms adapt CuevikFlow
  to how they work without custom builds.
- **Workflow automation** — firm-defined rules that trigger actions on events
  (document received, job completed, due date approaching), so hand-offs happen
  without someone remembering them.
- **Integrations** — connection to the firm's accounting software and two-way
  calendar sync with Google and Microsoft 365, so client records and deadlines
  stay aligned with the tools the firm already uses.
- **Mobile apps** — installable mobile apps for firm staff, so staff can check and
  update work away from a desk.
- **Firm onboarding** — guided setup and bulk import from existing
  spreadsheets, so a firm moves off spreadsheets without re-typing its client
  list.

## 3A. Decision Placeholders

## 4. Scope (In / Out)

### In scope

- Leads, prospects, and clients as organisations or individuals, moving through
  Lead → Prospect → Client → Inactive or Archived.
- People linked to the organisations they act for; organisations linked to
  related organisations.
- Engagements as one-time service contracts; one-off and recurring Jobs; Task
  checklists. Engagements are optional by default; a firm MAY make them
  mandatory.
- Firm-owned Engagement and Job templates, and a region-neutral Cuevik starter
  library that firms copy; copies are never synced after copying.
- Deadline reminders and escalation to staff and managers; automatic reminders
  to client contacts for outstanding requests.
- No-login link requests for client documents and information; basic file
  upload and download on clients and jobs.
- Templated outbound email to client contacts; a per-client communication log;
  two-way email sync with AI filing of replies.
- Comments, @mentions, and in-app notifications; manager review and sign-off on
  jobs.
- Personal and firm-wide dashboards; exportable reports on deadline compliance,
  workload, and throughput.
- AI: at-risk job detection, assignee suggestions, upload classification,
  extraction of client-document data into firm-defined outputs, and summaries
  and drafts. Staff review all AI output before use.
- Proposals and engagement acceptance that convert a prospect into a client.
- Time tracking; invoices raised from jobs and time.
- Owner, Manager, and Staff roles; role-based and field-level access; an audit
  trail.
- Custom fields; firm branding on client-facing emails and request links.
- Firm-defined workflow automation rules.
- Accounting-software integration; two-way calendar sync with Google and
  Microsoft 365.
- Installable mobile apps for firm staff.
- Guided setup and bulk import from comma-separated values (CSV) and Excel
  files.

### Out of scope

- Cuevik-maintained or jurisdiction-specific compliance templates, deadline
  libraries, or regulatory updates — the starter library is region-neutral and
  copy-on-use; Cuevik takes on no per-country content obligation.
- Tax calculations on CuevikFlow's own authority — AI extraction fills
  firm-defined outputs; the firm owns every formula.
- Client portal with a login — client contacts interact only through emails and
  request links (client mobile app: see Wish-list).
- Full document management (folders, versioning, in-app preview, retention
  policies) — files attach to clients and jobs only.
- Person-to-person and family links.
- Multi-location and branch support — firms of 2–20 staff operate as one unit.
- Internal team chat, Short Message Service (SMS) text messaging, and video calls — team discussion stays on jobs and
  tasks; client contact stays on email and links.
- Marketing: campaigns, newsletters, surveys, and referral or upsell programmes
  — CuevikFlow manages relationships and work, not marketing.
- Payment collection — CuevikFlow raises invoices; payments are handled outside
  it.
- Tax-software integration.
- White-label (custom domains, removing Cuevik branding) — firm branding on
  emails and links is in scope.
- Knowledge base, document co-editing, whiteboards, and staff training.
- Process mining and robotic process automation (RPA).
- The firm's own human resources (HR), payroll, and finances.
- Guardian, trust, and custodial workflows.
- Bookkeeping ledgers and lodging returns with tax authorities — the firm's
  accounting and tax software remain the system of record.

### Wish-list (not committed)

Each item below is out of scope until PRODUCT.md is updated to move it in.

- Client mobile app — requires a client login, which the product currently
  excludes; revisit §2 and the no-login decision first.
- E-signature.

## 5. Success Criteria

- **Time to value** — a new firm imports its client list and has its first
  recurring Job scheduled within 60 minutes of sign-up, without Cuevik help.
- **Recurrence reliability** — 100% of scheduled Job occurrences are created on
  their scheduled date; zero missed generations per month, measured from system
  records.
- **On-time delivery** — after 90 days of use, at least 95% of a firm's Jobs are
  completed on or before their due date.
- **Client request turnaround** — at least 80% of link requests are fully
  answered through the link (no email attachments); median time from sent to
  answered is 5 days or less.
- **Spreadsheet replacement** — by day 60, the firm confirms it no longer uses a
  spreadsheet or inbox to track client jobs, and at least 80% of its staff use
  CuevikFlow in any given week.
- **AI acceptance** — at least 90% of AI extraction outputs are accepted by
  staff with no field corrections, and at least 70% of assignee suggestions are
  accepted unchanged.
- **Commercial** — 10 firms on paid subscriptions within 6 months of general
  availability, with monthly firm churn at or below 3%.

## 6. Anti-Patterns

- **Features that serve a single tenant** — client-specific requests MUST ship
  as configuration of a shared capability or as a general feature; revisiting
  this requires paying demand and a PRODUCT.md update first.
- **Treating client personal data as ordinary app data** — each firm's data
  MUST be isolated from other firms, and the product MUST meet the privacy law
  of each market before firms in that market use it.
- **Forcing structure onto simple work** — a one-off Job MUST NOT require an
  Engagement, template, or extra setup unless the firm has chosen to require it;
  heavy setup drives small firms back to spreadsheets.
- **AI output that bypasses staff** — AI MUST NOT send anything to a client,
  change a record, or produce a figure the firm relies on without staff review;
  the firm carries the professional liability.
- **Changing a firm's data or templates without its action** — Cuevik MUST NOT
  alter a firm's templates, due dates, or records on its own initiative,
  including through starter-library updates; the firm must trust that what it
  set is what runs.
- **Hiding slippage** — a due date moved after a Job is created MUST remain
  visible as a change; otherwise on-time rates look healthy while deadlines
  slip.
- **Asking a client twice** — a client contact SHOULD NOT be asked for a
  document or information the firm already holds; repeated requests are the
  client-side pain this product exists to remove.
- **Reminder noise** — reminders and notifications SHOULD reach only someone who
  can act on them and stop once the action is done; alerts staff learn to
  ignore are worse than none.
- **Building one country into the core** — the core product MUST NOT hard-code
  any country's tax terms, forms, or deadlines; region-neutral is a product
  decision.

## 7. Roadmap

## Glossary
