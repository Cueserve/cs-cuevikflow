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
  through request links, not email attachments (§5: Client request turnaround, post-thin-core).
- **See every job without asking** — the owner sees the state of every job, deadline, and
  person's workload on the firm-wide dashboard (§5: Owner visibility).
- **Leave the spreadsheet behind** — the firm sets itself up without Cuevik help and runs
  its client work in CuevikFlow alone (§5: Time to value, post-thin-core; Spreadsheet replacement).

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

- **Firm owner / partner** — loses new-client inquiries that arrive by web, phone, or
  email before anyone records them, and cannot see which jobs are overdue or at risk, or
  which leads and prospects are going cold, without asking staff; carries the
  consequence of every missed deadline.
- **Manager** — assigns and reviews work across staff but has no single view of
  team workload or of which recurring jobs are ready for the next period, so
  rebalancing, review, and hand-offs between staff happen by chasing people.
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

- **Zero-leak inquiry capture** _(Roadmap)_ — every new-client inquiry, from the firm's web
  inquiry form or logged by staff from phone, email, or walk-in, becomes one Lead that keeps
  its source; an inquiry from an existing client or Lead is matched to that record instead
  of creating a duplicate. So no prospective client is lost or entered twice.
- **Complete client record** _(Thin-core)_ — one record for each Lead, Prospect, and Client,
  as an Organisation or an Individual, from first contact to Inactive or Archived. It shows
  who acts for each Organisation and which Organisations form a group, every Engagement,
  Job, file, and message is attached to it, and likely duplicates are flagged. So any staff
  member can pick up any client without a handover.
- **Work-to-deadline tracking** _(Thin-core)_ — every piece of client work is a Job with a
  due date and a status (Not started, In progress, Waiting on client, In review, Complete),
  one-off or recurring, broken into Tasks assigned to staff with their own due dates. Each
  occurrence of a recurring Job is created on schedule with its Task checklist, and
  past-due Jobs are marked. A Job MAY sit under an Engagement that sets out what a client
  needs and when — optional unless the firm requires it. Comments, @mentions, and
  notifications keep discussion on the work. So recurring work sets itself up, and everyone
  sees what is due, who has it, and where it stands.
- **Four-eyes sign-off** _(Thin-core)_ — a Job that requires review moves to In review when
  its work is done, and only a Manager or Owner other than the person who did the work can
  sign it off as Complete or send it back with comments; who signed off, and when, is
  recorded. The firm sets which Jobs require review in their templates. So work that needs
  a second pair of eyes always gets one, and every sign-off can be shown later.
- **Reusable job templates** _(Thin-core)_ — firm-owned Engagement and Job templates, each
  setting a Job's Task checklist, recurrence, due dates relative to the period it covers,
  and whether it requires review; a firm can also copy and adapt templates from a region-neutral Cuevik starter
  library. A copied template is the firm's own and changes only when the firm edits it. So
  every job of the same kind runs the same way, without being rebuilt each cycle.
- **Deadline early warning** _(Roadmap)_ — AI checks each Job's progress against its due
  date (Tasks done, time left, and whether it is waiting on the client) and warns the
  assignee, then escalates to a manager, when a Job is at risk or past due. Warnings reach
  only someone who can act, stop once the Job is back on track, and never reach the client.
  It uses the at-risk detection in Human-approved AI and builds on the past-due list in
  Firm work at a glance. So deadlines are caught before they are missed.
- **No-login client requests** _(Roadmap)_ — staff send a client contact a checklist of
  documents and questions through a secure link that is unique to that request and
  contact, expires, can be revoked, and needs no login. The contact can answer part now
  and the rest later; automatic reminders go out until every item is answered, then stop.
  Answers and files are kept against the client and the Job, and the link and its emails
  carry the firm's name and logo so clients trust them. Before sending, staff see what the
  firm already holds, so a client is not asked twice. So documents arrive in one place
  instead of email chains and scattered attachments.
- **Communication center** _(Thin-core (partial))_ — one timeline per client of every email,
  request, call, meeting, and note, with templated email sent to client contacts from
  CuevikFlow. Two-way email sync files mail from known contacts by their address; for
  unknown senders, AI suggests the client and staff confirm. So the firm's full history
  with a client is in one place, and anyone can see what was said before they reply. The
  thin-core release ships templated outbound email, logged automatically, and a log where
  staff record calls, meetings, and notes by hand.
- **Firm work at a glance** _(Thin-core (partial))_ — a personal view of each person's own
  Jobs and Tasks, and a firm-wide view for owners and managers of every Job's status,
  upcoming deadlines, past-due Jobs, at-risk Jobs, and team workload, plus exportable
  reports on deadline compliance, workload, and throughput over time. So owners see where
  every job stands today, and the trend, without asking anyone. The thin-core release ships
  both views with Job status, upcoming deadlines, past-due Jobs, and team workload.
- **Human-approved AI** _(Roadmap)_ — AI that flags Jobs at risk of missing their due date,
  suggests assignees, sorts client uploads, extracts client-document data into firm-defined
  outputs, suggests the client for unfiled email, and drafts summaries and messages. Flags
  are advisory; everything else waits for staff to accept it, so nothing reaches a client,
  changes a record, or becomes a figure the firm relies on until they do. So staff stop
  sorting, re-keying, and writing first drafts, while the firm keeps control of every
  output.
- **Need-to-see access** _(Thin-core)_ — Owner, Manager, and Staff roles, with sensitive
  fields restricted by role and every restriction enforced by the system, not just hidden
  on screen. Each firm's data is isolated from every other firm's, and an audit trail
  records who changed what and when. So each person sees only what their job needs, and
  the firm can always answer "who changed this?"
- **Firm-defined fields** _(Roadmap)_ — the firm adds custom fields to clients, Jobs, and
  Tasks (text, number, date, or a choice list) and defines its own Job statuses in place of
  the fixed set, with no code. So a firm shapes CuevikFlow to how it works.
- **Spreadsheet-to-live onboarding** _(Roadmap)_ — the firm imports its clients and their
  contacts from comma-separated values (CSV) or Excel files, maps its columns to
  CuevikFlow's fields, and sees a preview with errors and likely duplicates flagged before
  anything is saved; an import can be undone. Guided setup then walks the firm through
  inviting staff, copying templates from the starter library, and scheduling its first
  recurring Job. So a firm moves off spreadsheets without re-typing its client list or
  needing Cuevik's help.
- **No-chase automation** _(Roadmap)_ — firm-defined rules in the form "when this happens,
  if this is true, do this": for example, when a client document arrives, move the Job to
  In progress and notify its assignee; when every Task on a Job is done, move it to In
  review and notify a manager. Rules act on the firm's own work (notify, assign, create
  Tasks, change Job status) and never message a client, and every change a rule makes is
  recorded in the audit trail under that rule. So hand-offs happen without anyone having to
  remember them.

## 3A. Decision Placeholders

## 4. Scope (In / Out)

### In scope — thin-core release (committed)

- **Complete client record** — Leads, Prospects, and Clients as Organisations or
  Individuals, moving through Lead → Prospect → Client → Inactive or Archived; people
  linked to the Organisations they act for, and Organisations to related Organisations;
  Engagements, Jobs, files, and messages attached; likely duplicates flagged when a record
  is created; basic file upload and download on clients and Jobs.
- **Work-to-deadline tracking** — one-off and recurring Jobs with due dates and a fixed
  status set (Not started, In progress, Waiting on client, In review, Complete); Task
  checklists assigned to staff with due dates; each recurring occurrence created on
  schedule; past-due Jobs marked; Engagements optional by default, and a firm MAY make them
  mandatory; comments, @mentions, and in-app notifications.
- **Four-eyes sign-off** — review and sign-off, or send-back, by a Manager or Owner other
  than the preparer, recorded, on Jobs whose template requires it.
- **Reusable job templates** — firm-owned Engagement and Job templates that set a Job's
  Task checklist, recurrence, due dates relative to the period it covers, and whether it
  requires review; a region-neutral Cuevik starter library that firms copy; copies are
  never synced after copying.
- **Communication center** (thin-core part) — templated outbound email to client
  contacts, logged automatically; a per-client log where staff record calls, meetings, and
  notes by hand.
- **Firm work at a glance** (thin-core part) — personal and firm-wide views: every Job's
  status, upcoming deadlines, a list of past-due Jobs, and team workload.
- **Need-to-see access** — Owner, Manager, and Staff roles; role-based and field-level
  access enforced by the system; each firm's data isolated from every other firm's; an
  audit trail.

> **Commitment rule:** This section is the only committed scope. Everything else in this
> document, including the roadmap below and every §3 feature tagged Roadmap, is intent and
> becomes commitment only when promoted into an approved PRD.

### Planned roadmap after thin-core (timing TBD)

- **Zero-leak inquiry capture** — a web inquiry form that creates exactly one Lead per
  submission, with none dropped; manual logging of phone, email, and walk-in inquiries;
  matching an inquiry to an existing client or Lead instead of creating a duplicate.
- **Deadline early warning** — AI-assisted warnings to assignees and escalation to
  managers as due dates approach or pass.
- **No-login client requests** — secure, expiring request links for client documents and
  information, with automatic reminders until answered; firm branding on request links and
  their emails.
- **Communication center** (beyond thin-core) — two-way email sync that files mail from
  known contacts by address; AI suggests the client for unknown senders, and staff confirm.
- **Firm work at a glance** (beyond thin-core) — at-risk Jobs; exportable reports on
  deadline compliance, workload, and throughput over time.
- **Human-approved AI** — at-risk Job detection, assignee suggestions, upload sorting,
  extraction of client-document data into firm-defined outputs, client suggestions for
  unfiled email, and drafted summaries and messages; flags are advisory, and everything
  else waits for staff to accept it.
- **Firm-defined fields** — custom fields on clients, Jobs, and Tasks, and firm-defined Job
  statuses.
- **Spreadsheet-to-live onboarding** — guided setup and bulk import from CSV and Excel
  files, with a preview before saving and undo.
- **No-chase automation** — firm-defined workflow rules.

### Out of scope

Permanently excluded — not deferred. Each carries the reason it stays out, so the decision
does not get re-argued; anything that might come in later belongs on the Wish-list.

- Cuevik-maintained or jurisdiction-specific compliance templates, deadline libraries, or
  regulatory updates — the starter library is region-neutral and copy-on-use; Cuevik takes
  on no per-country content obligation.
- Tax calculations on CuevikFlow's own authority — AI extraction fills firm-defined
  outputs; the firm owns every formula.
- Full document management (folders, versioning, in-app preview, retention policies) —
  firms keep their existing document store; CuevikFlow holds only files attached to its
  clients and Jobs.
- Internal team chat, Short Message Service (SMS) text messaging, and video calls — team
  discussion stays on Jobs and Tasks; client contact stays on email and links.
- Marketing: campaigns, newsletters, surveys, and referral or upsell programmes —
  CuevikFlow manages relationships and work, not marketing.
- Payment collection — handling payments would bring payment-security and reconciliation
  obligations unrelated to delivering client work.
- Tax-software integration — tax software differs by country, so integrating it would
  build one country into the core (§6).
- White-label (custom domains, removing Cuevik branding) — the product stays
  Cuevik-branded; firm branding on client-facing messages is on the roadmap.
- Knowledge base, document co-editing, whiteboards, and staff training — firms use
  dedicated tools for these; none of them moves client work forward.
- Process mining and robotic process automation (RPA) — enterprise automation;
  No-chase automation covers the hand-offs a firm needs.
- The firm's own human resources (HR), payroll, and finances — CuevikFlow runs client
  work, not the firm's back office.
- Bookkeeping ledgers and lodging returns with tax authorities — the firm's accounting and
  tax software remain the system of record.

### Wish-list (not committed)

Each item below is out of scope until PRODUCT.md is updated to move it in. Moving one in
needs a named problem for a §2 persona.

- Client mobile app — requires a client login, which the product currently
  excludes; revisit §2 and the no-login decision first.
- Client portal with a login — client contacts use only emails and request links today;
  revisit together with the Client mobile app, which needs the same login.
- Household and family links — grouping Individuals, such as spouses filing jointly or a
  parent and dependants.
- Guardian, trust, and custodial workflows.
- E-signature.
- Multi-location and branch support — the firms CuevikFlow starts with operate as one
  unit; larger firms may need it.
- Proposal to engagement — a proposal sets out services and fees; when the prospect
  accepts it (see E-signature), it becomes an Engagement and the Prospect becomes a Client.
- Time and billing — time logged against jobs and tasks, and invoices raised from jobs and
  time.
- Integrations — accounting-software connection and two-way calendar sync with Google and
  Microsoft 365.
- Staff mobile apps — installable mobile apps for firm staff.

## 5. Success Criteria

### Thin-Core Release Outcomes (Committed)

- **Recurrence reliability** — 100% of scheduled Job occurrences are created on
  their scheduled date; zero missed generations per month, measured from system
  records.
- **On-time delivery** — after 90 days of use, at least 95% of a firm's Jobs are
  completed on or before their due date.
- **Owner visibility** — from day 30, the owner or a manager opens the firm-wide dashboard
  in at least 3 of every 4 weeks, measured from system records.
- **Spreadsheet replacement** — by day 60, the firm confirms it no longer uses a
  spreadsheet or inbox to track client jobs, and at least 80% of its staff use
  CuevikFlow in any given week.
- **Commercial** — 10 firms on paid subscriptions within 6 months of general
  availability, with monthly firm churn at or below 3%.

### Post-Thin-Core Outcomes (Roadmap Targets)

- **Time to value** — a new firm imports its client list and has its first
  recurring Job scheduled within 60 minutes of sign-up, without Cuevik help.
- **Client request turnaround** — at least 80% of link requests are fully
  answered through the link (no email attachments); median time from sent to
  answered is 5 days or less.
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
