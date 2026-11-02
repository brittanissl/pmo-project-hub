# PMO Project Hub

A lightweight project portfolio tool built from a PMO practitioner's point of view. It answers the questions leadership actually asks every week: *What's on track? What's at risk, and why? What needs a decision?*

**Live demo:** https://brittanissl.github.io/pmo-project-hub/

> All sample data is for a fictional company, Northwind Distribution.

---

## What's new in v2

v2 is built from feedback on v1 from PMO practitioners who tested it:

- **Pending decisions.** Decisions stay open until someone makes the call. Each shows who decides, how long it has been waiting, and the impact of delay.
- **Budget tracking.** Approved budget, actual spend and forecast at completion per project. Flags when forecast runs over budget or spend runs well ahead of progress.
- **Dependencies.** A project can depend on an upstream project. If the upstream is at risk or off track, the downstream project shows it.
- **Approval record.** Approving a request records who approved it, why, and a capacity check on the proposed owner.
- **Capacity and load by owner.** The Dashboard shows active projects, open and overdue tasks, and budget per owner, and warns above four active projects.
- **Data gaps.** Projects with no owner, no plan, no update yet, or no update in 14 days are flagged.
- **Calculated % complete.** When a project has tasks, % complete is calculated from them instead of typed in.
- **Override transparency.** A manual health override shows the automatic health beside it.
- **Week-over-week trend.** Each project shows whether its health is better, worse or unchanged over the last 7 days.
- **Upcoming milestones.** The project overview lists the next tasks due within 30 days.
- **Intake scoring rubric.** Plain definitions for each 1–5 rating, so requests are scored the same way across teams.
- **Dashboard view.** Decisions waiting, load by owner, budget, dependencies and data gaps on one page.

v1 data is migrated automatically the first time v2 opens in a browser.

## Why I built it

Most work-management tools are good at tracking tasks but weak at the PMO layer: consistent health scoring, a real RAID log, and a status report that doesn't take an hour to assemble. This project puts that layer first.

## Features

**Portfolio view**
- Every project on one screen with phase, owner, % complete, due date, health and trend
- KPI strip: active projects, on track / at risk / off track, pending decisions, overdue tasks, projects with data gaps
- Search, filter by health, and sort by worst health, due date or priority

**Dashboard**
- Decisions waiting on someone, with days waiting and impact of delay
- Load by owner, with a capacity warning
- Budget: approved, actual, forecast, and spend versus progress
- Dependencies and data gaps

**Automatic health scoring (with reasons)**
Health is calculated from the data, and the tool explains *why*:

| Rule | Result |
|---|---|
| Past due date | Off track |
| Open high-severity issue | Off track |
| Any open issue, open high risk, or overdue task | At risk |
| % complete trails % of schedule used by 20+ points | At risk |
| Forecast over approved budget | At risk |
| Spend ahead of progress by more than 15 points | At risk |
| Upstream dependency at risk or off track | At risk |

A project manager can override the calculated health, and the tool shows both values so the override stays visible.

**RAID log for every project**
Risks, Actions, Issues and Decisions, with owner, severity and status. Decisions stay open until marked decided and show how long they have been pending.

**Intake and prioritization**
New requests are scored on business value, urgency, strategic fit and effort (0–100), with a scoring rubric beside the form. Approving a request asks for the owner, the approver and the reason, runs a capacity check, and turns the request into a project with that record attached.

**One-click weekly status report**
Generates an executive-ready report from the live data: portfolio summary, what needs attention, decisions waiting, data gaps, and for each project its trend, why it is red or amber, budget, next two weeks, open risks and issues, and recent decisions. Copy it into an email or download it as Markdown.

**Your data stays with you**
No account or server. Data is saved in your browser, with Export/Import to back it up as JSON.

## How to use it

1. Open the live demo, or download `index.html` and double-click it.
2. Explore the sample portfolio, then use **Reset sample data** any time.
3. Click a project card to edit details, budget, dependencies, tasks, the RAID log and weekly updates.
4. Check **Dashboard** for decisions waiting, load and budget.
5. Go to **Status Report** to generate this week's update.

## Built with

Plain HTML, CSS and JavaScript in a single file. No frameworks, no build step, works on desktop and mobile, light and dark mode.

## Roadmap: from project hub to operating platform

This hub is the first module of a larger business operations system. The plan:

1. **Project Hub** (v2): intake, portfolio, RAID, budget, dependencies, dashboard, status reporting
2. **AI assistant**: paste meeting notes and get RAID items and action items extracted; draft status narratives
3. **Operating Rhythm Register**: daily, weekly and monthly recurring tasks by role, with an operating calendar
4. **Business domain views**: register and projects tagged by domain so they roll up into
   - **ERP** view (finance close, procurement, inventory)
   - **HCM** view (roles, RACI, workload, onboarding)
   - **CRM** view (client touchpoints, QBRs, renewals)
5. **Transformation roadmap**: current state → future state recommendations on which processes belong in which system

Later candidates from practitioner feedback: calendar and Kanban views, attachments on intake requests, an audit trail, and team sharing (these need a server, so they sit outside the single-file design).

## About me

Built by **Britta Nissl**, PMO and client services leader with a background in Oracle ERP, SCM and HCM consulting. I'm interested in where operations, project management and AI meet.
