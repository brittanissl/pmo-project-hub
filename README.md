# PMO Project Hub

A lightweight project portfolio tool built from a PMO practitioner's point of view. It answers the questions leadership actually asks every week: *What's on track? What's at risk, and why? What needs a decision?*

**Live demo:** https://brittanissl.github.io/pmo-project-hub/

> All sample data is for a fictional company, Northwind Distribution.

---

## Why I built it

Most work-management tools are good at tracking tasks but weak at the PMO layer: consistent health scoring, a real RAID log, and a status report that doesn't take an hour to assemble. This project puts that layer first.

## Features

**Portfolio view**
- Every project on one screen with phase, owner, % complete, due date and health
- KPI strip: active projects, on track / at risk / off track, overdue tasks, open high risks and issues
- Search, filter by health, and sort by worst health, due date or priority

**Automatic health scoring (with reasons)**
Health is calculated from the data, and the tool explains *why*:

| Rule | Result |
|---|---|
| Past due date | Off track |
| Open high-severity issue | Off track |
| Any open issue, open high risk, or overdue task | At risk |
| % complete trails % of schedule used by 20+ points | At risk |

A project manager can override the calculated health, and the tool shows both values so the override stays visible.

**RAID log for every project**
Risks, Actions, Issues and Decisions, with owner, severity and open/closed status.

**Intake and prioritization**
New requests are scored on business value, urgency, strategic fit and effort (0–100). Approving a request turns it into a project with its priority score attached.

**One-click weekly status report**
Generates an executive-ready report from the live data: portfolio summary, what needs attention, why each project is red or amber, next two weeks, open risks and issues, and recent decisions. Copy it into an email or download it as Markdown.

**Your data stays with you**
No account or server. Data is saved in your browser, with Export/Import to back it up as JSON.

## How to use it

1. Open the live demo, or download `index.html` and double-click it.
2. Explore the sample portfolio, then use **Reset sample data** any time.
3. Click a project card to edit details, tasks, the RAID log and weekly updates.
4. Go to **Status Report** to generate this week's update.

## Built with

Plain HTML, CSS and JavaScript in a single file. No frameworks, no build step, works on desktop and mobile, light and dark mode.

## Roadmap: from project hub to operating platform

This hub is the first module of a larger business operations system. The plan:

1. **Project Hub** (this release): intake, portfolio, RAID, status reporting
2. **AI assistant**: paste meeting notes and get RAID items and action items extracted; draft status narratives
3. **Operating Rhythm Register**: daily, weekly and monthly recurring tasks by role, with an operating calendar
4. **Business domain views**: register and projects tagged by domain so they roll up into
   - **ERP** view (finance close, procurement, inventory)
   - **HCM** view (roles, RACI, workload, onboarding)
   - **CRM** view (client touchpoints, QBRs, renewals)
5. **Transformation roadmap**: current state → future state recommendations on which processes belong in which system

## About me

Built by **Britta Nissl**, PMO and client services leader with a background in Oracle ERP, SCM and HCM consulting. I'm interested in where operations, project management and AI meet.
