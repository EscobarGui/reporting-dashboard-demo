# Automated Reporting Dashboard — Demo

Single-file interactive dashboard modeled on a production reporting system I built at a fintech company: replacing a manual, department-by-department reporting process with an automated dashboard.

**Real-world result this is modeled on:** reduced daily report preparation from ~3 hours to 10–20 minutes by automating data collection and formatting across departments.

## What it does

- Pulls together department-level KPIs (tasks completed, SLA %, pending items, average handling time) into a single view, the exact numbers a manager previously had to compile by hand from separate sources.
- Highlights which department needs attention based on SLA target, instead of someone scanning a spreadsheet to notice it.
- Shows a 14-day SLA trend so a dip is visible immediately, not just in hindsight.
- "Regenerate report" button demonstrates the automated generation running client-side, with the elapsed time shown live against the ~3 hour manual baseline.

## Run it

Open `dashboard.html` directly in a browser — no build step, no server required. All data is generated client-side (seeded, so it's stable across reloads) as stand-in sample data; in production this would be replaced with a real data source (database query, API, or export).

## Why this matters for a client

Most small and mid-size teams build their "dashboard" by hand in a spreadsheet every day: pulling numbers from different tools, formatting them, and emailing them around. This shows what that process looks like once it's automated — same data, same departments, but nobody manually compiling it anymore.

## Adapting this for a real client

- Replace the sample-data generator with a real data source (SQL query, API call, Google Sheets, internal tool export).
- Add scheduled generation (e.g. a cron job or serverless function) plus automatic delivery (Slack message, emailed PDF, etc.).
- Add authentication/multi-tenant support if more than one team needs to see their own slice of the data.
