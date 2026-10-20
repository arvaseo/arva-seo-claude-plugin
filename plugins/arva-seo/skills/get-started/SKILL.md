---
name: get-started
description: Add a website to Arva SEO, start its first check, and verify that the person owns it step by step in this chat. Use when someone wants to set up Arva SEO, add or connect a website, verify ownership, fix a failed verification, or asks why full audits or Google data need verification.
---

# Get started with Arva SEO

A website works in Arva SEO before it's verified: it gets a first check of up to 100 pages a day, and PageSpeed tests. Verifying shows the person owns it and unlocks full audits, their Google data and the benchmark (which then records itself). This skill takes the person from no website to a checked, verified one without leaving the chat.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in to their Arva SEO account and approve. Then try again.

## Steps

1. **Find or add the website.** Call `list_websites`. If the website isn't there, ask for its address and the country it mainly serves, and call `add_website` with `country` (a two-letter code, or `worldwide`). Adding it starts its first check of up to 100 pages. The country sets the market for keyword data, rankings and competitor estimates; without one, a country-code address such as `.ph` sets it, and any other address uses the United States. If several are unverified, ask which one.
2. **Quickest, when the website is in Google Search Console:** ask. If it is, the person opens the website's **Search data** page in Arva SEO and connects Google with the account that owns the website there (Owner or Full user). That one sign-in, which they do in the app, verifies the website and links its Search Console and Analytics. If a Google account is already connected, `verify_website` with `method: search_console` checks it.
3. **Otherwise, get the steps for this website.** Call `get_verification_steps`. It reads which platform the website runs on (WordPress, Shopify, Wix, Squarespace, Webflow, Ghost) and where its DNS is hosted (Cloudflare, GoDaddy, Namecheap and others), recommends the easiest method and gives numbered steps with the exact values. Say what you found in one or two sentences, recommend the method and why, and offer the others if the person prefers (for example DNS when they can't edit the website).
4. **Walk through it one step at a time.** Give the exact tag, TXT record or file name and content in a code block, and wait for the person to say each step is done. If their screen looks different, help them find the setting.
5. **Check it.** Call `verify_website` with the chosen `method`. If it fails, explain in plain words what Arva SEO found (for example "the tag isn't on the homepage yet" or "no TXT record yet") and fix it together. A new DNS record can take a few minutes, sometimes hours: suggest checking again shortly.
6. **Results.** `get_audit_results` shows the first check a few minutes after the website was added: summarise the most important issues, with the steps for the website's platform (`how_on_platform`). Once verified, offer a full audit with `run_audit`.

## Rules

- Never ask for passwords, API keys or hosting logins. The person makes every change on their own website.
- On WordPress, the Arva SEO Connector plugin is usually quickest, and it also lets Arva SEO send drafts and fixes to WordPress later.
