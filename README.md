# SIMS 窶・Smart Incident Management System

A custom incident management build on a ServiceNow Personal Developer Instance (PDI), featuring **automated SLA monitoring and escalation** 窶・built independently to demonstrate end-to-end platform development beyond baseline administration.

## Overview

SIMS was built to go past routine ServiceNow admin tasks and show real application/automation development: designing incident-handling logic where SLA compliance is tracked automatically and at-risk incidents are escalated before they breach, rather than relying on manual monitoring.

## Features

- Incident tracking with priority-based SLA targets
- Automated SLA monitoring using Business Rules / Scheduled Jobs that check incident age against SLA thresholds
- Automatic escalation (priority bump and/or reassignment) when a breach is imminent
- Email notifications triggered on SLA-risk and breach events
- Client-side logic (UI Policies / Client Scripts) for dynamic form behavior

> 統 **Add here:** confirm which of the above you implemented exactly, plus your scoped app name, key table names, and any dashboards/reports you built (e.g. Service Portal widget, list view).

## Tech Stack

`ServiceNow (PDI)` ﾂｷ `Business Rules` ﾂｷ `Scheduled Jobs` ﾂｷ `Client Scripts` ﾂｷ `GlideRecord` ﾂｷ `Email Notifications`

## How It Works

```
Incident created
        笏・        笆ｼ
SLA tracking starts (Business Rule / SLA definition)
        笏・        笆ｼ
Scheduled Job periodically checks elapsed time vs. SLA threshold
        笏・        笏懌楳笏 Approaching breach 笏笏笆ｶ Escalate priority + notify assignment group
        笏・        笏披楳笏 Within SLA 笏笏笆ｶ No action
```

> 統 **Add here:** your actual escalation logic 窶・thresholds used, what "escalate" means in your build (priority change? reassignment? both?), and a snippet of the core `GlideRecord` script (e.g. your `addQuery()` / `next()` loop).

## Key Learnings

- Practical use of `GlideRecord` query patterns (`addQuery()`, `next()`) for automation logic
- Building trigger-based automation with Business Rules and Scheduled Jobs
- Understanding how SLA logic and escalation paths work in ServiceNow ITSM

## Screenshots

> 統 **Add here:** Studio view of the app, a Business Rule/Scheduled Job script, and a before/after example of an incident being escalated.

## Future Improvements

- Automated Test Framework (ATF) coverage for the escalation logic
- Service Portal widget for a live "My Open Incidents" / SLA-risk dashboard
- Tie into a Service Catalog request flow so incidents can originate from catalog items

## Author

**Sarath Vasantharaj** 窶・ServiceNow CSA | Building hands-on ServiceNow projects on PDI while transitioning into a ServiceNow Developer/Administrator role.
