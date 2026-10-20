# Arva SEO

Do your SEO in Claude with [Arva SEO](https://arvaseo.com), using the Claude plan you already have: set up and verify a website, research keywords, build a fix plan, study competitors, write content and page copy, report to clients and send finished work to WordPress. Claude works with your Arva SEO account and saves its work there, where you and your team review it. No API key is needed: you sign in to your Arva SEO account once and approve.

## What's included

- **The Arva SEO connector**, `https://api.arvaseo.com/mcp`: Arva SEO's own MCP server, with tools for your websites, verification and audits; Search Console and GA4 data, keywords, rankings and the keyword map; PageSpeed, AI search, local SEO and tasks; backlinks, competitors, findings and client reports; content, page copy, WordPress and its PageSpeed fixes.
- **Skills**, following the SEO cycle:
  - **get-started**: adds a website (its first check starts straight away) and walks you through verifying it right in the chat: connecting Google when the website is in Search Console, or steps for your platform (WordPress, Shopify, Wix, Squarespace, Webflow and more) and DNS host.
  - **keyword-research**: finds quick wins in Search Console and new keyword ideas, saves them, gives each one a page and tracks rankings.
  - **fix-plan**: turns the audit, PageSpeed, AI search and local SEO into a prioritised plan and tasks, with steps for your website's platform.
  - **competitor-research**: compares you with competitors, finds the keyword and link gaps, and adds link prospects to your outreach pipeline.
  - **write-content-brief** and **write-content-draft**: plan and write articles with your business's own experience, saved to Content.
  - **improve-page-copy**: better titles, meta descriptions and H1s for audited pages, saved to Optimize for review.
  - **monthly-report**: explains what changed and creates a client report with a summary and next steps.
  - **publish-to-wordpress**: sends finished drafts and SEO titles and descriptions to WordPress, within what the site allows.
  - **speed-up-wordpress**: tries the Arva SEO Connector's PageSpeed fixes on your WordPress site, then turns them on once you've checked your pages.

Claude shows you its work before saving it, and asks before replacing anything already there.

## What it reads, sends and saves

- **Nothing runs on your computer.** The plugin is skills (Markdown instructions for Claude) and the connector's address. It has no scripts, hooks or packages.
- **Claude talks only to Arva SEO's server** at `api.arvaseo.com`, over HTTPS, signed in as you with OAuth. You approve the connection on an Arva SEO page, and it uses your access: the websites you can see, saving only where your role can edit.
- **What it reads from your Arva SEO account:** what you can see in Arva SEO for your websites: their details, audits, Search Console and GA4 figures, keywords and rankings, PageSpeed, AI search and local SEO results, backlinks, competitors, tasks, reports and content. It never sees billing or other people's accounts.
- **What it changes in your Arva SEO account:** it adds websites, keywords, keyword mappings, tasks, AI questions, competitors, link prospects, content pieces, briefs, drafts, page copy and reports, and updates task and page statuses. It never deletes anything, changes settings or invites people.
- **What uses your plan:** keyword research, PageSpeed tests, Business Profile lookups, map grid scans and backlink lookups use the same monthly allowances as in the app, and rank tracking uses slots. Claude says what each one used and what's left.
- **What reaches outside Arva SEO:** verifying a website reads its homepage, DNS or file; audits crawl it; PageSpeed tests are run by Google; recrawl requests go to IndexNow (Bing and others). Sending to WordPress goes through the Arva SEO Connector plugin and never beyond the publishing mode the site's WordPress administrator set; Claude asks before each send.
- **Nothing is sent anywhere else.** What Claude saves is kept in your Arva SEO account under the [Arva SEO Privacy Policy](https://arvaseo.com/privacy/). Disconnect Claude any time in Arva SEO under **Integrations → AI**; its access ends at once.

## Requirements

An Arva SEO account on any plan, including Free, and Claude (the Claude app, or Claude Code 2.1.275 or later).

## Install

In the Claude app, open **Customize → Plugins**, choose **Add marketplace**, enter `arvaseo/arva-seo-claude-plugin` and install **Arva SEO**. Then open the plugin's **Connectors** tab, choose **Connect** next to Arva SEO, sign in and approve.

The connector alone (without the skills) is also in [Claude's connector directory](https://claude.ai/directory/connectors/arva-seo).

In Claude Code:

```
/plugin install arva-seo --marketplace arvaseo/arva-seo-claude-plugin
```

Then run `/mcp`, choose **arva-seo** and sign in to Arva SEO in your browser.

## Try it

- "Add my website to Arva SEO and help me verify it."
- "Which keywords am I close to page one for?"
- "What should I fix first on my website?"
- "Who are my competitors outranking me for, and who links to them?"
- "Write a brief for my next content piece."
- "Create last month's client report."
- "Send the dental implants article to WordPress as a draft."

## Help

[Use Arva SEO in Claude or ChatGPT](https://support.arvaseo.com/articles/use-arva-seo-in-claude-or-chatgpt) · [support@arvaseo.com](mailto:support@arvaseo.com) · [Terms](https://arvaseo.com/terms/) · [Privacy](https://arvaseo.com/privacy/)
