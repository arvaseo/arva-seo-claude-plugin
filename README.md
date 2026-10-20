# Arva SEO for Claude

Do your SEO in Claude with [Arva SEO](https://arvaseo.com), using the Claude plan you already have: set up and verify a website, research keywords, build a fix plan, study competitors, write content and page copy, report to clients and send finished work to WordPress. Claude works with your Arva SEO account and saves its work there for you to review. No API key needed: you sign in to your Arva SEO account once.

The plugin adds:

- **The Arva SEO connector** (`https://api.arvaseo.com/mcp`): your websites, audits, search data, keywords, rankings, PageSpeed, AI search, local SEO, tasks, backlinks, competitors, reports, content and WordPress, as tools Claude can use with your access and your plan's allowances.
- **Skills** Claude uses when you ask for them, following the SEO cycle:
  - **get-started**: adds a website and walks you through verifying it in the chat, then runs the first audit.
  - **keyword-research**: quick wins from Search Console, new keyword ideas, the keyword map and rank tracking.
  - **fix-plan**: a prioritised plan and tasks from the audit, PageSpeed, AI search and local SEO.
  - **competitor-research**: the keyword and link gaps against competitors, and link prospects for outreach.
  - **write-content-brief** and **write-content-draft**: plan and write articles, saved to Content.
  - **improve-page-copy**: better titles, meta descriptions and H1s for audited pages, saved to Optimize for review.
  - **monthly-report**: what changed, and a client report with a summary and next steps.
  - **publish-to-wordpress**: sends drafts and SEO titles and descriptions to WordPress, within what the site allows.
  - **speed-up-wordpress**: tries the Arva SEO Connector's PageSpeed fixes on your WordPress site, then turns them on once you've checked your pages.

## Install

### In the Claude app (Cowork, chat)

1. Open **Customize → Plugins**, choose **Add marketplace** and enter `arvaseo/arva-seo-claude-plugin`.
2. Install **Arva SEO**.
3. Open the plugin's **Connectors** tab and choose **Connect** next to Arva SEO. Sign in to Arva SEO and approve.

### In Claude Code

```
/plugin install arva-seo --marketplace arvaseo/arva-seo-claude-plugin
```

(On versions before 2.1.275: `/plugin marketplace add arvaseo/arva-seo-claude-plugin`, then `/plugin install arva-seo@arva-seo`.)

Then run `/mcp`, choose **arva-seo** and sign in to Arva SEO in your browser.

### Without the plugin

You can also add the connector on its own, from [Arva SEO's listing in Claude's connector directory](https://claude.ai/directory/connectors/arva-seo), or in Claude under **Settings → Connectors → Add custom connector** with the address `https://api.arvaseo.com/mcp`. The skills aren't included that way; the connector still gives Claude the same tools and writing rules.

## Try it

- "Write a brief for my next content piece on bayside-dental.com."
- "Draft the article about dental implant costs from its brief."
- "Improve the title and meta description of my homepage."

## What Claude can and can't do

Claude works with your Arva SEO access: it sees the websites you can see, and saves briefs, drafts and page suggestions only where your role can edit. Everything it saves waits for your review in Arva SEO. It changes your WordPress site only when you confirm (drafts, SEO titles and descriptions, PageSpeed fixes), within what the site's administrator allows. It can't change billing or settings, or see other workspaces. You can disconnect it any time under **Integrations → AI** in Arva SEO.

Help: [Use Arva SEO in Claude or ChatGPT](https://support.arvaseo.com/articles/use-arva-seo-in-claude-or-chatgpt) · [support@arvaseo.com](mailto:support@arvaseo.com) · [Privacy](https://arvaseo.com/privacy/) · [Terms](https://arvaseo.com/terms/)

Claude is a trademark of Anthropic; this plugin isn't made or endorsed by Anthropic.
