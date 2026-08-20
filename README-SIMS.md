# SIMS — Smart Incident Management System

A custom incident management build on a ServiceNow Personal Developer Instance (PDI), featuring **automated SLA monitoring and escalation** — built independently to demonstrate end-to-end platform development beyond baseline administration.

## Overview

SIMS was built to go past routine ServiceNow admin tasks and show real application/automation development: designing incident-handling logic where SLA compliance is tracked automatically and at-risk incidents are escalated before they breach, rather than relying on manual monitoring.

## Features

- Incident tracking with priority-based SLA targets
- Automated SLA monitoring using Business Rules / Scheduled Jobs that check incident age against SLA thresholds
- Automatic escalation (priority bump and/or reassignment) when a breach is imminent
- Email notifications triggered on SLA-risk and breach events
- Client-side logic (UI Policies / Client Scripts) for dynamic form behavior

> 📝 **Add here:** confirm which of the above you implemented exactly, plus your scoped app name, key table names, and any dashboards/reports you built (e.g. Service Portal widget, list view).

## Tech Stack

`ServiceNow (PDI)` · `Business Rules` · `Scheduled Jobs` · `Client Scripts` · `GlideRecord` · `Email Notifications`

## How It Works

```
Incident created
        │
        ▼
SLA tracking starts (Business Rule / SLA definition)
        │
        ▼
Scheduled Job periodically checks elapsed time vs. SLA threshold
        │
        ├── Approaching breach ──▶ Escalate priority + notify assignment group
        │
        └── Within SLA ──▶ No action
```

> 📝 **Add here:** your actual escalation logic — thresholds used, what "escalate" means in your build (priority change? reassignment? both?), and a snippet of the core `GlideRecord` script (e.g. your `addQuery()` / `next()` loop).

## Key Learnings

- Practical use of `GlideRecord` query patterns (`addQuery()`, `next()`) for automation logic
- Building trigger-based automation with Business Rules and Scheduled Jobs
- Understanding how SLA logic and escalation paths work in ServiceNow ITSM

## Screenshots

> 📝 **Add here:** Studio view of the app, a Business Rule/Scheduled Job script, and a before/after example of an incident being escalated.

## Future Improvements

- Automated Test Framework (ATF) coverage for the escalation logic
- Service Portal widget for a live "My Open Incidents" / SLA-risk dashboard
- Tie into a Service Catalog request flow so incidents can originate from catalog items

## Author

**Sarath Vasantharaj** — ServiceNow CSA | Building hands-on ServiceNow projects on PDI while transitioning into a ServiceNow Developer/Administrator role.
