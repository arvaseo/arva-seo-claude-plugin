---
name: competitor-research
description: Compare an Arva SEO website with its competitors (keywords, traffic estimates, backlinks, speed), find the keyword gap and the link gap, and add link-building prospects to its outreach pipeline. Use when someone asks about competitors, why a competitor outranks them, keyword or content gaps, backlinks, domain authority, toxic links or link building.
---

# Competitor and authority research with Arva SEO

The authority and compete steps of the SEO cycle.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in and approve.

## Steps

1. **Pick the website** with `list_websites`, then `get_competitors`. With none yet, ask who they compete with and call `add_competitor` (the plan sets how many per website; its answer says how many are in use). Estimates arrive in the background within a few minutes.
2. **Compare** keywords, estimated traffic, top-10 rankings, backlinks and domain rank side by side. Estimates are estimates: say so, and use the website's own measured figures where they exist.
3. **Keyword gap**: `get_keyword_gap` with `class: "missing"` and `"weak"` shows what competitors rank for that the website doesn't, or ranks lower for. Suggest which to target and which page should do it (the keyword-research skill can save and map them).
4. **Backlinks**: `get_backlinks` shows the profile and its audit (toxic links, broken targets, anchors). `get_link_gap` shows websites linking to competitors but not to this one. To fetch fresh data, `refresh_backlinks` uses the plan's backlink lookups: say what it uses first.
5. **Outreach**: with the person's agreement, `add_link_prospects` adds the best link gap domains to the outreach pipeline in Arva SEO. Suggest an angle for each (a resource, a local news story, a directory listing). Nothing is sent to anyone.

## Rules

- Prefer relevant, real websites over high numbers; never suggest buying links or link schemes.
- Ask before anything that uses the plan's allowance.
