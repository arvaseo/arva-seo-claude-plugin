---
name: publish-to-wordpress
description: Send a finished draft, or the SEO titles and meta descriptions saved in Arva SEO, to the website's WordPress site through the Arva SEO Connector plugin, within the publishing mode the site's WordPress administrator set. Use when someone asks to post, publish, schedule or send an article to WordPress, or to push titles and descriptions to Yoast SEO or Rank Math.
---

# Send work to WordPress with Arva SEO

The last step: getting reviewed work onto the website. The site's WordPress administrator decides the ceiling in the Arva SEO Connector plugin (draft only, editorial review, scheduling or full publishing), and Arva SEO never goes beyond it.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in and approve.

## Steps

1. **Check the connection** with `get_wordpress`: whether the site is connected, its publishing mode and allowed statuses, and whether SEO titles and descriptions can be sent. Not connected: explain how to install and connect the free Arva SEO Connector plugin.
2. **For an article**: find it with `list_content` and confirm it has a reviewed draft (`get_content_piece`). Ask how it should arrive: as a draft (the default and safest), for review, scheduled, or published, but only among the statuses the site allows. Confirm the exact choice, then call `send_to_wordpress`. Publishing straight away needs `confirm_publish: true`, only after the person says yes to it going live now.
3. **For titles and descriptions**: the pages need recommended copy saved in Arva SEO first (the improve-page-copy skill). Show the person the pages and the new copy, confirm, then call `send_seo_to_wordpress`. It replaces what the live pages have; each update can be undone from the website's WordPress page in Arva SEO.
4. **Afterwards**: the plugin picks it up within a few minutes. `request_recrawl` can tell Bing and other IndexNow search engines about changed pages.

## Rules

- Always confirm before sending: these change the live website.
- Never try to get around the site's publishing mode; if something isn't allowed, say who can change it (the WordPress administrator, in Arva SEO → Settings in WordPress).
