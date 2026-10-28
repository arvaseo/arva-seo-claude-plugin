---
name: speed-up-wordpress
description: Speed up a WordPress website with the Arva SEO Connector plugin's PageSpeed fixes (Speed Booster), trying each fix first and turning it on once the person has checked their pages. Use when someone asks to make their WordPress site faster, fix slow loading or Core Web Vitals on WordPress, or turn on PageSpeed fixes.
---

# Speed up a WordPress website with Arva SEO

The free Arva SEO Connector plugin has switches for what Google's PageSpeed test finds: lazy-loading images and videos, deferring scripts, WebP and compressed images, faster fonts, lighter styles, page caching, minified CSS and JavaScript and more. Each fix is off until it's turned on, most can be tried first (only signed-in administrators see a fix while it's tried), and turning one off puts the pages back as they were.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in and approve.

## Steps

1. **Check the site** with `get_wordpress`. Its `speed_fixes` show each fix's state, which ones the latest phone test asks for, and whether Arva SEO may switch them (`switch_from_arva_seo`). If it may not, explain that the site's WordPress administrator ticks "Let Arva SEO switch these fixes" in WordPress → Arva SEO → Speed, or switches them there. A fix with `needs_plugin_update` needs a newer plugin first (`added_in` says which version): `switch_speed_fix` answers `update_needed` until the site updates.
2. **See what to fix.** `get_pagespeed_results` gives the findings, each with `connector_fixes`. With no recent test, `run_pagespeed_test` uses one PageSpeed test per device from the plan: say so first.
3. **Pick a few**, starting with the ones the latest test asks for and those marked `safe`. Explain each in plain words.
4. **Try first.** With the person's OK, call `switch_speed_fix` with `to: trying` for a fix that can be tried. Ask them to open their homepage and a few important pages while signed in to WordPress, and to check menus, forms, sliders and anything that moves.
5. **Turn it on** with `to: on` once they say the pages look right, or `to: off` if something broke. "Defer scripts" goes on only in WordPress, after it's been tried there. "New uploads as WebP", "Compress images", "Browser caching and compression" and "Page caching" have no trying step: they go straight on, so confirm first.
6. **Updates to check** (plugin 2.11.0 and later). A fix with `update_to_check` in `get_wordpress` was changed by a plugin update, and visitors still get the version the administrator checked. Explain its `note` in plain words, ask the person to open their important pages while signed in to WordPress (that is where they see the new version), then call `switch_speed_fix` with `to: use_update`. Don't turn such a fix on with `to: on`: it answers `update_to_check`. Defer scripts is updated for visitors only in WordPress (`in_wordpress_only`).
7. **Measure.** WordPress picks each change up within seconds with plugin 2.7.0 and later, a minute or two on older versions (`get_wordpress` shows the state). `caches.clear_it_yourself` lists the page caches Arva SEO can't clear: ask the person to clear the ones with `needs_clearing_now` first, or PageSpeed may test the old page. The caches Arva SEO can clear are cleared at most every 15 minutes, so wait a little before testing a second switch. Then `run_pagespeed_test` again to show the difference.

## Rules

- These change the live website: always ask before trying or turning on a fix.
- One or two fixes at a time, so a problem is easy to trace.
- Never try to get around the site's settings; if switching isn't allowed, say who can change it.
- Combining files (Combine CSS or JavaScript files, and from plugin 2.10.0 the inline and external minify and combine options) isn't a PageSpeed finding: suggest it only when the person asks, and test again after. Combining inline snippets or files from other websites only uses what an administrator approved in WordPress.
- DNS prefetch and Preconnect use the websites an administrator lists in WordPress; `switch_speed_fix` only switches them on or off.
- From plugin 2.10.0.1, the optimized CSS of "Load styles faster" and "Remove unused CSS" keeps newer CSS syntax whole (for example phone menus written with `(width<=…)`), and CSS saved by older versions is downloaded again automatically, at no cost. If a phone menu or layout looked wrong with either fix on an older plugin (`get_wordpress` shows `plugin_version`), suggest updating the plugin and checking again before turning the fix off.
