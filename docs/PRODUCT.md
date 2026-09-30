# PRODUCT.md — Product Concept

**Owner:** Viral Parikh
**Last updated:** 2026-09-30
**Source of truth for:** what CuevikFlow is, why it exists, who it serves, and its intended scope — an
AI-assisted platform that gives accounting and tax firms a single workspace to keep a trusted
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

Every accounting and tax firm delivers every client's work on time, from
one trusted record that any staff member can pick up without a handover.

### Problem Statement

Small accounting and tax firms struggle because their client records and
operational work are fragmented across spreadsheets, email threads, shared
drives, and staff memory. Deadlines are tracked manually, recurring work is
rebuilt every cycle, and client documents arrive inconsistently as email
attachments or ad-hoc uploads. Owners and managers lack visibility into
workload, overdue work-items, bottlenecks and at-risk jobs.

A small firm has no spare capacity to model workflows, build templates,
or retrain the team before a tool pays back, so practice-management software
that front-loads that setup gets abandoned for the spreadsheet. Small firms
need operational control without heavyweight process.

Closing those gaps has to be backed by software the team can trust —
specifically:

- One complete record — every request, reply, and document is logged against
  the client, so any staff member can pick up the work without a handover.
- Recurring jobs and their deadlines appear on schedule every time, without
  anyone remembering to set them up.
- What the firm sets is what runs — templates, due dates, and records change
  only by the firm's own action, and every change shows who made it and when.
- AI assists but never acts alone — nothing reaches a client, changes a record,
  or becomes a figure the firm relies on without staff review.

### Objective

CuevikFlow must let an accounting or tax firm:

- **Deliver client work on time** — Jobs are completed on or before their due dates
  (§5: On-time delivery).
- **Get what it needs from clients without chasing** — documents and information come back
  through request links, not email attachments (§5: Client request turnaround).
- **See every job without asking** — the owner sees the state of every job, deadline, and
  person's workload on the firm-wide dashboard (§5: Owner visibility).
- **Leave the spreadsheet behind** — the firm sets itself up without Cuevik help and runs
  its client work in CuevikFlow alone (§5: Time to value, Spreadsheet replacement).

### Description

A firm keeps every Lead, Prospect, and Client in CuevikFlow and runs its client work as
Jobs — one-off, or recurring on a schedule with a Task checklist on each Occurrence. Staff
collect documents and information through Requests that client contacts answer without
logging in, and every email, Request, and note is logged against the Client. Reminders and
escalation keep each deadline in front of the person who owns it, and dashboards give the
owner the state of every Job. AI flags risk, sorts and extracts client uploads, and drafts;
staff review every output before use.

## 2. Target Users

CuevikFlow is for accounting and tax firms that deliver recurring client work — bookkeeping,
payroll, periodic tax filings, and year-end accounts. It starts with small firms, which have
the least capacity for heavy setup; firm size is the starting point, not the limit.

> These are roles, not headcount: in a small firm one person may be owner, manager, and staff
> at once. Owner, Manager, and Staff are CuevikFlow's three role-based access control (RBAC)
> roles; a client contact has no role and never logs in.

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

> Features describe the full product model, including roadmap intent. Only §4 "In scope —
> thin-core release" is committed. Each feature is tagged: _Thin-core_ is committed in full,
> _Thin-core (partial)_ is committed only in the part §4 states, and _Roadmap_ is not
> committed.

- **Client relationships** _(Thin-core)_ — one record per lead, prospect, and client
  (organisation or individual) from first contact to Inactive or Archived,
  showing who acts for each organisation and which organisations form a group,
  so any staff member can pick up any client.
- **Engagements and recurring jobs** _(Thin-core)_ — service contracts that set out which jobs
  a client needs and when; jobs that recur on schedule with task checklists; and
  comments, @mentions, and notifications on the work, so recurring work sets itself
  up and the team discusses it where it happens.
- **Review and sign-off** _(Thin-core)_ — manager review and sign-off before a job is complete, so
  nothing is marked done unreviewed.
- **Templates** _(Thin-core)_ — firm-owned Engagement and Job templates plus a Cuevik starter
  library the firm copies and adapts, so every job of the same kind runs the
  same way.
- **Deadline reminders and escalation** _(Thin-core)_ — reminders to assignees and escalation
  to managers as due dates approach or pass, so deadlines are caught before they
  are missed.
- **Client requests and documents** _(Thin-core)_ — requests for documents and information
  that client contacts answer through a link without logging in, with automatic
  reminders to the client until answered and files kept against the client and
  job, replacing email chasing and scattered attachments.
- **Client communication** _(Thin-core (partial))_ — templated email to client contacts, with every
  message, request, call, meeting, and note logged against the client, and
  two-way email with replies filed automatically by AI, so the firm's full history with a
  client is in one place.
- **Work visibility and reporting** _(Thin-core (partial))_ — personal and firm-wide dashboards
  (deadlines, overdue work, at-risk jobs, team workload) plus exportable reports
  on deadline compliance, workload, and throughput over time, so owners see
  both today's state and the trend.
- **AI assistance** _(Roadmap)_ — at-risk job detection, assignee suggestions, classification
  of client uploads, extraction of client-document data into firm-defined
  outputs, and summaries and drafts, all reviewed by staff before use, removing
  manual sorting, re-keying, and first-draft writing.
- **Team, roles and access** _(Thin-core)_ — Owner, Manager, and Staff roles; sensitive fields
  restricted by role; and an audit trail of who changed what and when, so each
  person sees what their job needs and the firm can answer "who changed this?"
- **Firm configuration** _(Roadmap)_ — custom fields on clients, jobs, and tasks, and firm
  branding on client-facing emails and request links, so firms adapt CuevikFlow
  to how they work without custom builds.
- **Firm onboarding** _(Thin-core)_ — guided setup and bulk import from existing
  spreadsheets, so a firm moves off spreadsheets without re-typing its client
  list.

## 3A. Decision Placeholders

## 4. Scope (In / Out)

### In scope — thin-core release (committed)

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
- Templated outbound email to client contacts; a per-client communication log.
- Comments, @mentions, and in-app notifications; manager review and sign-off on
  jobs.
- Personal and firm-wide dashboards: deadlines, overdue work, and team workload.
- Owner, Manager, and Staff roles; role-based and field-level access; an audit
  trail.
- Guided setup and bulk import from comma-separated values (CSV) and Excel
  files.

> **Commitment rule:** This section is the only committed scope. Everything else in this
> document, including the roadmap below and every §3 feature tagged Roadmap, is intent and
> becomes commitment only when promoted into an approved PRD.

### Planned roadmap after thin-core (timing TBD)

- Two-way email sync with AI filing of replies.
- Exportable reports on deadline compliance, workload, and throughput over time.
- AI: at-risk job detection (and at-risk jobs on dashboards), assignee suggestions,
  upload classification, extraction of client-document data into firm-defined outputs,
  and summaries and drafts. Staff review all AI output before use.
- Custom fields; firm branding on client-facing emails and request links.

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
- Internal team chat, Short Message Service (SMS) text messaging, and video calls — team discussion stays on jobs and
  tasks; client contact stays on email and links.
- Marketing: campaigns, newsletters, surveys, and referral or upsell programmes
  — CuevikFlow manages relationships and work, not marketing.
- Payment collection — payments are handled outside CuevikFlow.
- Tax-software integration.
- White-label (custom domains, removing Cuevik branding) — firm branding on
  emails and links is on the roadmap.
- Knowledge base, document co-editing, whiteboards, and staff training.
- Process mining and robotic process automation (RPA).
- The firm's own human resources (HR), payroll, and finances.
- Guardian, trust, and custodial workflows.
- Bookkeeping ledgers and lodging returns with tax authorities — the firm's
  accounting and tax software remain the system of record.

### Wish-list (not committed)

Each item below is out of scope until PRODUCT.md is updated to move it in. Moving one in
needs a named problem for a §2 persona.

- Client mobile app — requires a client login, which the product currently
  excludes; revisit §2 and the no-login decision first.
- E-signature.
- Multi-location and branch support — the firms CuevikFlow starts with operate as one
  unit; larger firms may need it.
- Proposals — proposals and engagement acceptance that convert a prospect into a client.
- Time and billing — time logged against jobs and tasks, and invoices raised from jobs and
  time.
- Workflow automation — firm-defined rules that trigger actions on events.
- Integrations — accounting-software connection and two-way calendar sync with Google and
  Microsoft 365.
- Staff mobile apps — installable mobile apps for firm staff.

## 5. Success Criteria

### Thin-Core Release Outcomes (Committed)

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
- **Owner visibility** — from day 30, the owner or a manager opens the firm-wide dashboard
  in at least 3 of every 4 weeks, measured from system records.
- **Spreadsheet replacement** — by day 60, the firm confirms it no longer uses a
  spreadsheet or inbox to track client jobs, and at least 80% of its staff use
  CuevikFlow in any given week.
- **Commercial** — 10 firms on paid subscriptions within 6 months of general
  availability, with monthly firm churn at or below 3%.

### Post-Thin-Core Outcomes (Roadmap Targets)

- **AI acceptance** — at least 90% of AI extraction outputs are accepted by
  staff with no field corrections, and at least 70% of assignee suggestions are
  accepted unchanged.

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

Canonical object names used across CuevikFlow docs. Informal synonyms in parentheses are
readable but not canonical — prefer the canonical term in specs.

- **Client lifecycle** — the stages every client record moves through: Lead → Prospect →
  Client → Inactive or Archived.
- **Lead** — a possible client at first contact.
- **Prospect** — a lead the firm is actively pursuing; it becomes a Client when the firm
  takes on its work.
- **Client** — an Organisation or an Individual the firm does work for.
- **Inactive** — a Client the firm is not currently working for. The record stays visible
  and can be reactivated.
- **Archived** — a Client relationship that has ended. The record is hidden from day-to-day
  views and is read-only.
- **Organisation** — a client entity that people act for. It MAY link to related
  Organisations, so the firm sees a client group as a whole.
- **Individual** — a client who is a person rather than an Organisation.
- **Client contact** — a person acting for an Organisation, or an Individual client. Interacts
  only through emails and request links; never logs in.
- **Engagement** — a one-time service contract stating which Jobs a client needs and when.
  Optional by default; a firm MAY require every Job to belong to one.
- **Job** — a unit of client work, either one-off or recurring on a schedule.
- **Occurrence** — one scheduled instance of a recurring Job.
- **Task** — a checklist item on a Job, assigned to a staff member with a due date. Each
  Occurrence of a recurring Job carries its own Tasks.
- **Template** — a firm-owned Engagement or Job definition that new Engagements and Jobs are
  built from.
- **Starter library** — Cuevik-supplied, region-neutral templates a firm copies and edits;
  copies are never synced back.
- **Request** — a request for documents or information that a client contact answers
  through a link, with no login (informal: "request link").
