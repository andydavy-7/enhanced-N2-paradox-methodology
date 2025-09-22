# ThreatForge Integration Platform — Reverse‑Engineered Requirements and v0.app Mockup Brief

## Overview
- Purpose: Central dashboard to convert threat intelligence into client tickets, manage feeds and integrations, and track value/analytics.
- Stack (from code): Next.js 14 App Router, React 18, Tailwind CSS 4, shadcn/ui, lucide-react icons.
- Layout: Top header (brand, live badge, settings) + left sidebar navigation with mobile drawer.

## Primary Users
- Internal Operator (ThreatForge admin/analyst)
- Client Success/Revenue Ops (reviews feedback, analytics)

## Key Views (from code)
1) Dashboard
2) Threat Intelligence (placeholder)
3) Feed Management
4) Client Management
5) Ticket Tracking (with filters + detail view)
6) Analytics (revenue/engagement)
7) Alert Feedback
8) Integrations (ServiceNow, Jira, Swim Lane)

## Functional Requirements
- Global
  - Responsive layout; mobile left‑nav drawer toggle.
  - Persist current view in component state; reset client selection on nav.

- Dashboard
  - KPI cards: Active Clients, Threats Processed, Tickets Generated, Integration Health.
  - Recent Threat Alerts list with severity badges and external link buttons.

- Client Management
  - Grid of client cards with: platform badge, monthly tickets, response rate, avg rating, resolution time.
  - Health indicators: Integration Health, Feed Quality with progress bars.
  - Recent activity list and action buttons (Configure, View Tickets).
  - Global “Add Client” button and an aggregated “Client Overview Statistics” card section.

- Ticket Tracking
  - Filters: search (by title/ID/alertId), status, priority, client, platform.
  - Results table columns: Ticket ID, Title, Status, Priority, Platform, Alert ID, Created, Rating, Actions.
  - Export action (stub).
  - Client drill‑in: shows per‑day ticket/resolution timeline with progress and a client‑scoped tickets table.
  - Ticket detail view: overview, threat intelligence details (CVE, CVSS, severity, affected systems, remediation), action timeline, and optional client feedback with 1–5 star rating.

- Feed Management
  - Summary metrics: processing rate, success rate, failed jobs.
  - Feeds table: Feed ID, Name, Client, Status (Active/Processing/Paused), Last Update, Tickets Generated, Quality, Actions (Play, Pause, Settings).
  - Ticket Templates library list: name, category, usage, last used, Use Template button.

- Analytics
  - KPI cards: Monthly Revenue, Client Retention, Avg Alert Value, Churn Risk.
  - Client Value table: Client, Monthly Value, Ticket Engagement (progress), Alert Rating, Churn Risk badge, View Details.

- Alert Feedback
  - Overview cards: Average Rating, Response Rate, Improvement Trend.
  - Ratings table: Alert ID, Title, Client, Rating (stars), Feedback (text), Ticket.

- Integrations
  - Cards for ServiceNow, Jira (Configure button), Swim Lane (Coming Soon).

## Data Model (mock)
- Ticket
  - id, client, title, description, status, priority, platform, created, updated, alertId, assignee, ticketUrl
  - rating? (1–5), feedback?, actions[] (timestamp, action, user)
  - threatDetails { cve, severity, cvss, affectedSystems[], remediation }

- ClientSummary
  - name, platform, monthlyTickets, responseRate, avgRating, resolutionTime, integrationHealth%, feedQuality%

- ClientTicketHistory
  - map<client, [{ date, tickets, resolved }...]>

- Feed
  - id, name, client, status, lastUpdate, ticketsGenerated, processingTime, quality

- Template
  - id, name, category, usage, lastUsed

- AlertRating
  - id, title, client, rating, feedback, ticketId

## Non‑Functional
- Visual: shadcn/ui components; lucide-react icons; Tailwind tokens for sidebar, card, badges.
- Accessibility: semantic structure; buttons/links have labels/icons.
- Performance: static mock data; no network calls in prototype.

## Interaction & State
- State: `currentView`, `isMenuOpen`, `selectedClient`, `selectedTicket`, `ticketFilters`.
- Nav changes reset `selectedClient` and close drawer on mobile.
- Filters recompute filtered tickets; selecting a ticket opens detail; back buttons restore previous state.

## v0.app Prompt (paste into v0)
Build a mock-only, responsive Next.js 14 + Tailwind + shadcn/ui SPA called “ThreatForge — Security Bulldog Integration Platform”. The goal is to DEMONSTRATE what’s possible without real backends: all data is mocked, all API calls are simulated, and interactions trigger toasts/drawers/wizards that FEEL real. Use a top header and a left sidebar nav (with mobile drawer). Include views: Dashboard, Threat Intelligence, Feed Management, Client Management, Ticket Tracking, Analytics, Alert Feedback, Integrations. Use lucide-react icons and consistent Cards, Tables, Badges, Progress, Selects, Inputs. Add a small “Demo Mode” badge in the header.

Global
- Mobile drawer for sidebar; highlight active nav item.
- Use seeded mock data; add a “Reset Demo Data” button in Settings to reseed.
- All external links/buttons are non-functional and can show a toast like “Would open in ServiceNow”.

Header & Sidebar
- Header: left brand with shield icon, title “ThreatForge” and subtitle “Integration Platform”; right: Live badge, Demo Mode badge, Settings button (opens settings drawer with theme toggle + reset demo data).
- Sidebar nav items (with icons): Dashboard, Threat Intelligence, Feed Management, Client Management, Ticket Tracking, Analytics, Alert Feedback, Integrations.

Dashboard
- KPI cards: Active Clients, Threats Processed, Tickets Generated, Integration Health (with progress/health badges and tiny trend text).
- “Recent Threat Alerts” card: 3–5 items with severity badges (Critical/High/Medium), CVE/title, short subtitle; an external link button per row (toast on click).

Client Management
- Top bar: title/subtitle + “Add Client” button.
- Clicking “Add Client” opens an Onboarding Wizard (modal/stepper) with 5 steps and fake validation:
  1) Integration (choose ServiceNow or Jira, show fields for base URL + auth; validate shows success)
  2) Defaults (project/issuetype OR table/category/assignment group)
  3) Field Mapping (show common source→target mappings with editable selects/text)
  4) Test Connection (simulate a successful test with latency/time)
  5) Finish (summary with “Activate Integration” toggle)
- Client cards (e.g., Acme • ServiceNow; TechStart • Jira): monthly tickets, response rate, avg rating (stars), resolution time; health (Integration Health and Feed Quality with progress bars); recent activity (3 items); “Configure” opens Integration drawer, “View Tickets” jumps to Ticket Tracking filtered by that client.
- “Client Overview Statistics” card with Total Clients, Avg Response Rate, Avg Rating, Avg Resolution Time.

Ticket Tracking
- Filters row: search (title/ID/alert), selects for Status, Priority, Client, Platform; results summary (“Showing N of M”).
- Table columns: Ticket ID, Title, Status (badge), Priority (badge), Platform, Alert ID (monospace), Created, Rating (stars or “No rating”), Actions (open details).
- Ticket Detail (drawer or page):
  - Overview (client, platform, assignee; created/updated; alert id; “View in {Platform}” button → toast)
  - Threat details (CVE, CVSS, Severity, Affected Systems list, Remediation text)
  - Action timeline (timestamp, action, user)
  - Client feedback (stars + text if present)
- Client drill‑in view: timeline list by date (tickets vs resolved with progress), below a client-only tickets table.
- “Export” shows a toast “Export started (mock)”.

Feed Management
- Summary metrics: Processing Rate, Success Rate, Failed Jobs.
- Feeds table: Feed ID, Name, Client, Status (Active/Processing/Paused with badges), Last Update, Tickets Generated, Quality (star rating), Actions (Play, Pause, Settings → drawer).
- “Ticket Templates” grid: 3+ cards with name, category badge, usage count, last used, “Use Template” button (pre-fills editor drawer, no save).
- Feed Editor (open from table row or “Configure”): Tabbed interface:
  1) Source & Parsing (show sample payload preview)
  2) Rules (filters by vendor/product/CVE regex/severity threshold; priority mapping; assignment rules)
  3) Templates (title/body template with variables like {CVE}, {product}, {cvss})
  4) Mapping (source → ServiceNow/Jira fields with helpful defaults)
  5) Test Run (shows 10 sample alerts with proposed Create/Update/Skip; per-row toggle; “Approve All”)
  6) Activation (toggle to enable; show rate limit notes)
- Run History: table of recent jobs (time, feed, action, result, duration); clicking opens Job Detail drawer with redacted request/response and error (mock data).
- Integration Health widget: auth status, rate limit, last error, next retry ETA.

Analytics
- KPI cards: Monthly Revenue, Client Retention, Avg Alert Value (stars), Churn Risk (# clients at risk with alert icon).
- Client Value table: Client, Monthly Value, Ticket Engagement (progress + %), Alert Rating (star + value), Churn Risk (Low/Medium/High badges), View Details.

Alert Feedback
- Overview cards: Average Rating (big number + star), Response Rate (%), Improvement Trend (+delta with trending icon).
- Recent Alert Ratings table: Alert ID (monospace), Title, Client, Rating (stars), Feedback (truncate), Ticket (link‑style button → toast).

Integrations
- Cards: ServiceNow (Configure), Jira (Configure), Swim Lane (Coming Soon outline button).
- Configure opens Integration drawer (same fields as wizard) with a “Re-test Connection” button (simulated success/failure).

Demo Notes
- Everything is mocked; no real API calls.
- Show toasts and skeletons to simulate activity.
- Provide enough seed data to make filters, tables, and previews feel real.

## Acceptance Criteria
- All views reachable via sidebar; active state visible.
- Ticket Tracking supports filter interactions and renders a detail view.
- Client Management shows at least two client cards and aggregate stats.
- Feed Management shows summary metrics, a feeds table with status badges and action buttons, and a templates grid.
- Analytics and Alert Feedback show KPI cards and tables as specified.
- Integrations shows three provider cards with appropriate button states.

## Out of Scope (prototype)
- Real auth, persistence, or API integrations.
- Editing entities beyond stub buttons.

## Notes
- Existing code uses shadcn/ui components and tailwind tokens for a unified look; mirror that in the mockup.
