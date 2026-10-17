---
name: monthly-report
description: Explain what changed on an Arva SEO website and what needs attention, and create a client report for a finished month with an executive summary and next steps written for the client. Use when someone asks for an SEO report, a monthly update, what changed, why traffic went up or down, or what to tell a client.
---

# Monthly report with Arva SEO

The report step of the SEO cycle.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in and approve.

## Steps

1. **Pick the website** with `list_websites`.
2. **Read what happened.** `get_findings` gives what needs attention and what changed, each labelled a measurement, observation or correlation. `get_search_performance` gives the totals against the period before, and `get_rankings`, `list_tasks` (completed work) and `get_audit_results` fill in the rest.
3. **Explain it plainly**: what went up or down, by how much, and what was done. Observations and correlations show what moved together, not a proven cause: say so.
4. **Create the report.** `list_reports` gives the months available. Draft an executive summary and next steps for the client (facts from the data only, no jargon, three to six short points each), show them, and once agreed call `create_report` with the month, the sections and that text.
5. **Next**: the report is in Arva SEO as a web report (its link is in the answer); the person can make a PDF and share it from there. `get_report` reads any report back.

## Rules

- Every number comes from the tools; never estimate or round in a way that changes the story.
- Nothing is sent to the client from here.
