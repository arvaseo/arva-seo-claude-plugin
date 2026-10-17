---
name: keyword-research
description: Research keywords for an Arva SEO website, decide which page should target each one, save them, and track their Google rankings, using the website's Search Console data and Arva SEO's keyword data. Use when someone asks for keyword ideas, what to rank for, quick wins, striking-distance keywords, a keyword map, pages competing for the same search, or to track rankings.
---

# Keyword research and mapping with Arva SEO

Research comes first in the SEO cycle: find what people search, pick a page for each search, and track how it ranks.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in and approve.

## Steps

1. **Pick the website** with `list_websites`.
2. **Start from what already works.** Call `get_search_queries` with `filter: "striking"` (positions 8–20, the quickest gains) and `filter: "unsaved"`, and `get_search_performance` for the overall picture. Without Search Console, say so and point to the website's Integrations page in Arva SEO.
3. **Find new ideas** with `research_keywords` for the seed topics the person cares about. It uses one of the plan's monthly keyword research lookups, unless the same search ran in the last 30 days: say what it cost and how many are left from its answer, and check before running several.
4. **Recommend a shortlist**: relevant to the business, a realistic difficulty for the website, and grouped by search intent. Explain each pick in a few words.
5. **Save and map.** With the person's agreement, call `add_keywords`, then `get_keyword_map` to see which pages already target what, and `map_keyword` to give each keyword one page (its main keyword, or a secondary one).
6. **Check for competing pages** with `get_pages_competing` (or with `keyword` before writing new content) and explain the fix for each conflict.
7. **Track rankings** with `track_keywords` for the keywords that matter most. Each uses a rank-tracking slot: say how many are in use from its answer. `get_rankings` shows positions once checked.

## Rules

- Use only figures the tools return; say "unknown" when a value is missing rather than guessing.
- Ask before anything that uses the plan's allowance (lookups, slots).
