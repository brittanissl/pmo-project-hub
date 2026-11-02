# PMO Project Hub

A lightweight project portfolio tool built from a PMO practitioner's point of view. It answers the questions leadership actually asks every week: *What's on track? What's at risk, and why? What needs a decision? Do we have the people and money to take on more?*

**Live demo:** https://brittanissl.github.io/pmo-project-hub/

> All sample data is for a fictional company, Northwind Distribution.

---

## Why I built it

Most work-management tools are good at tracking tasks but weak at the PMO layer: consistent health scoring, a real risk log, governance over what gets approved, and a status report that doesn't take an hour to assemble. This project puts that layer first.

## What's new in v2

v2 was shaped by feedback from PMO practitioners who tested v1.

| Feedback | What changed |
|---|---|
| Record who approved, why, and check capacity | Approving a request now requires an approver and a reason, and runs a live **capacity check** (team FTE and per-owner load) before the project is created. Approving over capacity needs an explicit acknowledgement and is flagged on the record. Declines record who and why too. |
| Flag projects with no owner, plan or recent update | **Data gaps** are flagged on every card, in the project panel and in the status report: no owner, no plan, no due date, no update in 14 days, and health overrides with no reason or that are overdue for review. New "Missing data" filter and KPI. |
| Always show the calculated health and its reasons | A manual override now requires a reason and records who set it and when. The **calculated health and its reasons stay visible** next to it on the card, the project panel and the status report. |
| Team sharing and an audit trail | **Activity log** records every change (who, what, old → new value, when), per project and portfolio-wide, with search and CSV export. **Team sharing** lets a team work from one shared data file. |
| Cross-project dependencies are where portfolios break down | Projects can **depend on other projects** with a needed-by date. A dependency is flagged when the upstream project is off track or due after it's needed, and that flows into the downstream project's health. New Dependencies view shows every link and which projects others rely on most. Loops are prevented. |
| Add budgeting | **Approved, actual and forecast** budget per project. Forecast more than 10% over budget marks a project at risk, more than 20% off track, and spending well ahead of progress is flagged. Portfolio totals in the new Capacity & Budget view. |

v1 data saved in your browser upgrades automatically.

## Features

**Portfolio view**
- Every project on one screen with phase, owner, % complete, due date, health, team size and budget
- KPI strip: active projects, on track / at risk / off track, overdue tasks, open high-severity items, projects with data gaps, capacity used
- Search, filter (by health, missing data, manual overrides), and sort by worst health, due date or priority

**Automatic health scoring (with reasons)**

| Rule | Result |
|---|---|
| Past due date | Off track |
| Open high-severity issue | Off track |
| Forecast more than 20% over budget | Off track |
| Waiting on a project that's late past its needed-by date | Off track |
| Any open issue, or open high-severity risk | At risk |
| Overdue task | At risk |
| % complete trails % of schedule used by 20+ points | At risk |
| Forecast more than 10% over budget, or spending well ahead of progress | At risk |
| Waiting on a project that's off track or due after it's needed | At risk |

A project manager can override the calculated health with a reason. Both values are always shown.

**Intake and governance**
New requests are scored on business value, urgency, strategic fit and effort (0–100), with an estimated team size and cost. Approval records the approver, the reason and the capacity at the time of approval.

**Capacity & Budget**
Team capacity in FTE, load by owner against a max-projects limit, and a budget table with variance and spend vs. progress. Thresholds are adjustable.

**Dependencies**
Every cross-project link in one table, with status and the projects others depend on most.

**One-click weekly status report**
Portfolio summary, capacity, budget, dependencies at risk, data gaps, and for each project: reported and calculated health with reasons, budget, latest update, what it's waiting on, next two weeks and open items. Copy it into an email or download it as Markdown.

**Activity log**
Audit trail of every change with who, when and what changed. Filter by project or person, search, and export to CSV.

## Team sharing

There's no server, so a team shares one data file:

1. Set your name (top right) so changes are attributed to you.
2. Open **Team sharing** → **Create a shared file from my current data**, and save it in a folder everyone can reach that syncs (OneDrive, SharePoint, Google Drive for desktop, or a network drive).
3. Teammates open the hub, choose **Team sharing** → **Open an existing shared file**, and pick the same file.

Changes save to the file automatically and others' changes load within about 20 seconds. If two people save at the same moment, the app asks whose version to keep. Works in Chrome and Edge on a computer; other browsers can use Export/Import.

## How to use it

1. Open the live demo, or download `index.html` and double-click it.
2. Explore the sample portfolio, then use **Reset sample data** any time.
3. Click a project card to edit details, tasks, the log, dependencies, budget and weekly updates.
4. Go to **Status Report** to generate this week's update.

## Built with

Plain HTML, CSS and JavaScript in a single file. No frameworks, no build step, works on desktop and mobile, light and dark mode.

## Roadmap: from project hub to operating platform

This hub is the first module of a larger business operations system. The plan:

1. **Project Hub** (v1: intake, portfolio, RAID, status reporting · v2: governance, capacity, budget, dependencies, audit trail)
2. **Shared database**: real multi-user editing with sign-in, replacing the shared file
3. **AI assistant**: paste meeting notes and get log items and action items extracted; draft status narratives
4. **Operating Rhythm Register**: daily, weekly and monthly recurring tasks by role, with an operating calendar
5. **Business domain views**: register and projects tagged by domain so they roll up into
   - **ERP** view (finance close, procurement, inventory)
   - **HCM** view (roles, RACI, workload, onboarding)
   - **CRM** view (client touchpoints, QBRs, renewals)
6. **Transformation roadmap**: current state → future state recommendations on which processes belong in which system

## About me

Built by **Britta Nissl**, PMO and client services leader with a background in Oracle ERP, SCM and HCM consulting. I'm interested in where operations, project management and AI meet.
