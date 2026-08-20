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
