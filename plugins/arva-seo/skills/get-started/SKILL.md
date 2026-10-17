---
name: get-started
description: Add a website to Arva SEO, verify that the person owns it step by step in this chat, and run its first audit. Use when someone wants to set up Arva SEO, add or connect a website, verify ownership, fix a failed verification, or asks why audits or Google data need verification.
---

# Get started with Arva SEO

Arva SEO needs each website verified before it audits it or shows Google data. This skill takes the person from no website to a verified, audited one without leaving the chat.

## Before you start

The Arva SEO tools come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in to their Arva SEO account and approve. Then try again.

## Steps

1. **Find or add the website.** Call `list_websites`. If the website isn't there, ask for its address and the country it mainly serves, and call `add_website` with `country` (a two-letter code, or `worldwide`). The country sets the market for keyword data, rankings and competitor estimates; without one, a country-code address such as `.ph` sets it, and any other address uses the United States. If several are unverified, ask which one.
2. **Get the steps for this website.** Call `get_verification_steps`. It reads which platform the website runs on (WordPress, Shopify, Wix, Squarespace, Webflow, Ghost) and where its DNS is hosted (Cloudflare, GoDaddy, Namecheap and others), recommends the easiest method and gives numbered steps with the exact values.
3. **Say what you found** in one or two sentences, recommend the method and why, and offer the others if the person prefers (for example DNS when they can't edit the website).
4. **Walk through it one step at a time.** Give the exact tag, TXT record or file name and content in a code block, and wait for the person to say each step is done. If their screen looks different, help them find the setting.
5. **Check it.** Call `verify_website` with the chosen `method`. If it fails, explain in plain words what Arva SEO found (for example "the tag isn't on the homepage yet" or "no TXT record yet") and fix it together. A new DNS record can take a few minutes, sometimes hours: suggest checking again shortly.
6. **Run the first audit.** Once verified, offer `run_audit`, then `get_audit_results` a minute or two later, and summarise the most important issues.

## Rules

- Never ask for passwords, API keys or hosting logins. The person makes every change on their own website.
- On WordPress, the Arva SEO Connector plugin is usually quickest, and it also lets Arva SEO send drafts and fixes to WordPress later.
