---
name: fix-plan
description: Turn an Arva SEO website's audit, PageSpeed, AI search and local SEO results into a prioritised fix plan and tasks on its Arva SEO task board. Use when someone asks what to fix first, for an SEO health check, why the site is slow, how it shows in ChatGPT or Google AI Overviews, how to improve local or Google Maps rankings, or to create or update SEO tasks.
---

# Build a fix plan with Arva SEO

The optimize step of the SEO cycle: find what holds the website back and turn it into tasks.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in and approve.

## Steps

1. **Pick the website** with `list_websites`, then read what's known:
   - `get_audit_results` for technical and on-page issues (no audit yet: offer `run_audit`).
   - `get_pagespeed_results` for speed and Core Web Vitals. To test a page now, `run_pagespeed_test` uses the plan's monthly PageSpeed tests (one per device): say what it uses first.
   - `get_ai_search` for AI readiness, Google AI Overviews and answers from AI assistants. `track_ai_question` adds a question to follow.
   - `get_local_seo` for a local business: Business Profile, map pack and local checks. `check_business_profile` and `run_map_grid_scan` use monthly allowances: say what they cost first.
2. **Prioritise**: critical issues and anything that blocks indexing first, then what affects the most pages or traffic, then quick wins. Keep it to the five to ten things that matter most, each with why and how in plain words. Audit issues, tasks and PageSpeed findings include `how_on_platform`: numbered steps for the website's own platform (WordPress, Shopify, Wix, Squarespace, Webflow) with how long they take. Use those steps when explaining a fix.
   - On WordPress with the Arva SEO Connector, PageSpeed findings list `connector_fixes`: switches in the plugin that fix them. The speed-up-wordpress skill tries and turns them on.
3. **Create tasks** the person agrees to: `create_tasks_from_audit` for audit issues (one task per issue, with the affected pages), and `create_task` for the rest. `list_tasks` shows the board; `update_task` moves a task along.
4. **Page by page**, `get_page` and `save_page_recommendations` (or the improve-page-copy skill) handle titles and descriptions, `set_page_status` tracks progress, and `request_recrawl` tells Bing and other IndexNow search engines when a page has changed.

## Rules

- Say which findings are measured and which are suggestions; never promise rankings.
- Ask before anything that uses the plan's allowance.
