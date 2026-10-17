---
name: improve-page-copy
description: Suggest a better title tag, meta description and H1 for a page Arva SEO has audited, and save the suggestions to Arva SEO's On-page section for review. Use when someone asks to improve, rewrite or optimize a page's title, meta description, headings or on-page SEO for one of their Arva SEO websites.
---

# Improve a page's copy for Arva SEO

Arva SEO audits each website's pages and lists what to fix. This skill writes better copy for one page (title tag, meta description, H1) and saves it to On-page in Arva SEO, where the person reviews it and applies it to their website.

## Before you start

The Arva SEO tools (`list_websites`, `list_pages`, `get_page`, `save_page_recommendations`) come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in to their Arva SEO account and approve. Then try again.

## Steps

1. **Find the website and page.** Call `list_websites` (ask which website if there are several), then `list_pages`. Pick the page the person names, by URL or by what it's about. If they haven't picked one, call `list_pages` with `filter: "needs_fixes"` and suggest a few.
2. **Read the page.** Call `get_page` with the page's URL or ID. It returns the current title, meta description and H1, the page's keywords, the audit's fixes for it and, when Google is connected, the Search Console queries people already find it with. Use those queries: they show what searchers expect from the page.
3. **Write the suggestions:**
   - Title tag: about 50–60 characters, the main keyword near the start, the brand at the end when it fits.
   - Meta description: about 120–160 characters, a clear reason to click, and true to what the page offers.
   - H1: one per page, close to the title but written for the reader.
   - Only promise what the page delivers. Never invent prices, offers, awards or reviews.
   - Anything else worth changing (thin sections, missing internal links, alt text) goes in `notes`, in plain words.
4. **Show them with the current copy** side by side and a one-line reason for each change, then call `save_page_recommendations`. If Arva SEO answers that the page already has recommended copy, ask whether to replace it before calling again with `replace_existing: true`.
5. **Say what happens next:** the suggestions are in Optimize in Arva SEO, marked for review. Once approved, they can be applied on the website by hand, or sent to WordPress (Yoast SEO or Rank Math) with the publish-to-wordpress skill when the site is connected.

## Rules

- Don't save anything the person hasn't seen, and never overwrite existing recommendations without asking.
- Keep each page's copy distinct from the website's other pages.
