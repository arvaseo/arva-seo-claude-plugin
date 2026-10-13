# Arva SEO for Claude

Write content briefs, drafts and page copy for your [Arva SEO](https://arvaseo.com) websites with Claude, using the Claude plan you already have. Claude reads each website's details, the brief and Arva SEO's writing rules, and saves its work back to Arva SEO, where you review it before anything is published. No API key needed: you sign in to your Arva SEO account once.

The plugin adds:

- **The Arva SEO connector** (`https://api.arvaseo.com/mcp`): your websites, content pieces, briefs and audited pages, as tools Claude can use with your access.
- **Three skills** Claude uses when you ask for them:
  - **write-content-brief**: plans a page (titles, meta description, outline, FAQs, E-E-A-T) and saves the brief to Content.
  - **write-content-draft**: writes the article from its brief, with placeholders where your own experience belongs, and saves the draft to Content.
  - **improve-page-copy**: suggests a better title tag, meta description and H1 for an audited page and saves them to On-page for review.

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

Claude works with your Arva SEO access: it sees the websites you can see, and saves briefs, drafts and page suggestions only where your role can edit. Everything it saves waits for your review in Arva SEO. It can't publish to your website, change billing or settings, or see other workspaces. You can disconnect it any time under **Integrations → AI** in Arva SEO.

Help: [Use Arva SEO in Claude or ChatGPT](https://support.arvaseo.com/articles/use-arva-seo-in-claude-or-chatgpt) · [support@arvaseo.com](mailto:support@arvaseo.com) · [Privacy](https://arvaseo.com/privacy/) · [Terms](https://arvaseo.com/terms/)

Claude is a trademark of Anthropic; this plugin isn't made or endorsed by Anthropic.
