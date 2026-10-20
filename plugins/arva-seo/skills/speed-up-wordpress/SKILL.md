---
name: speed-up-wordpress
description: Speed up a WordPress website with the Arva SEO Connector plugin's PageSpeed fixes (Speed Booster), trying each fix first and turning it on once the person has checked their pages. Use when someone asks to make their WordPress site faster, fix slow loading or Core Web Vitals on WordPress, or turn on PageSpeed fixes.
---

# Speed up a WordPress website with Arva SEO

The free Arva SEO Connector plugin has switches for what Google's PageSpeed test finds: lazy-loading images and videos, deferring scripts, WebP images, faster fonts, lighter styles and more. Each fix is off until it's turned on, most can be tried first (only signed-in administrators see a fix while it's tried), and turning one off puts the pages back as they were.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in and approve.

## Steps

1. **Check the site** with `get_wordpress`. Its `speed_fixes` show each fix's state, which ones the latest phone test asks for, and whether Arva SEO may switch them (`switch_from_arva_seo`). If it may not, explain that the site's WordPress administrator ticks "Let Arva SEO switch these fixes" in WordPress → Arva SEO → PageSpeed fixes, or switches them there.
2. **See what to fix.** `get_pagespeed_results` gives the findings, each with `connector_fixes`. With no recent test, `run_pagespeed_test` uses one PageSpeed test per device from the plan: say so first.
3. **Pick a few**, starting with the ones the latest test asks for and those marked `safe`. Explain each in plain words.
4. **Try first.** With the person's OK, call `switch_speed_fix` with `to: trying` for a fix that can be tried. Ask them to open their homepage and a few important pages while signed in to WordPress, and to check menus, forms, sliders and anything that moves.
5. **Turn it on** with `to: on` once they say the pages look right, or `to: off` if something broke. "Defer scripts" goes on only in WordPress, after it's been tried there. "New uploads as WebP" and "Browser caching and compression" have no trying step: they go straight on, so confirm first.
6. **Measure.** WordPress picks each change up within a minute or two (`get_wordpress` shows the state). Then `run_pagespeed_test` again to show the difference.

## Rules

- These change the live website: always ask before trying or turning on a fix.
- One or two fixes at a time, so a problem is easy to trace.
- Never try to get around the site's settings; if switching isn't allowed, say who can change it.
