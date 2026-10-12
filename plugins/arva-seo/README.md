# Arva SEO

Write content briefs, drafts and page copy for your [Arva SEO](https://arvaseo.com) websites with Claude, using the Claude plan you already have. Claude reads each website's details, the business's own experience notes and Arva SEO's writing guidelines, and saves its work back to Arva SEO, where you and your team review it before anything goes on your website. No API key is needed: you sign in to your Arva SEO account once and approve.

## What's included

- **The Arva SEO connector**, `https://api.arvaseo.com/mcp`: Arva SEO's own MCP server. It gives Claude tools to list your websites, content pieces and audited pages, read one in full, start a content piece, and save a brief, a draft or page copy suggestions.
- **write-content-brief**: plans a page (title options, meta description, search intent, outline, FAQs and an E-E-A-T plan) and saves the brief to Content in Arva SEO.
- **write-content-draft**: writes the article from its brief in Markdown, with placeholders where the business's own experience or a source is needed, and saves the draft to Content.
- **improve-page-copy**: suggests a better title tag, meta description and H1 for a page Arva SEO has audited, using the audit's fixes and Search Console queries, and saves them to On-page for review.

Claude shows you each brief, draft or suggestion before saving it, and asks before replacing anything already there.

## What it reads, sends and saves

- **Nothing runs on your computer.** The plugin is three skills (Markdown instructions for Claude) and the connector's address. It has no scripts, hooks or packages.
- **Claude talks only to Arva SEO's server** at `api.arvaseo.com`, over HTTPS, signed in as you with OAuth. You approve the connection on an Arva SEO page, and it uses your access: the websites you can see, saving only where your role can edit.
- **What it reads from your Arva SEO account:** website names and addresses; content pieces (topic, keywords, author, your experience notes, brief and draft); audited pages (current title, meta description and H1, word count, mapped keywords, audit fixes, and Search Console queries when Google is connected).
- **What it saves to your Arva SEO account:** new content pieces, briefs, drafts and page copy suggestions, marked for review. It never publishes to your website, deletes anything, changes settings, invites people or sees billing.
- **Nothing is sent anywhere else.** What Claude saves is kept in your Arva SEO account under the [Arva SEO Privacy Policy](https://arvaseo.com/privacy/). Disconnect Claude any time in Arva SEO under **Integrations → AI**; its access ends at once.

## Requirements

An Arva SEO account on any plan, including Free, and Claude (the Claude app, or Claude Code 2.1.275 or later).

## Install

In the Claude app, open **Customize → Plugins**, choose **Add marketplace**, enter `arvaseo/arva-seo-claude-plugin` and install **Arva SEO**. Then open the plugin's **Connectors** tab, choose **Connect** next to Arva SEO, sign in and approve.

In Claude Code:

```
/plugin install arva-seo --marketplace arvaseo/arva-seo-claude-plugin
```

Then run `/mcp`, choose **arva-seo** and sign in to Arva SEO in your browser.

## Try it

- "Write a brief for my next content piece."
- "Draft the article about dental implant costs from its brief."
- "Improve the title and meta description of my homepage."

## Help

[Use Arva SEO in Claude or ChatGPT](https://support.arvaseo.com/articles/use-arva-seo-in-claude-or-chatgpt) · [support@arvaseo.com](mailto:support@arvaseo.com) · [Terms](https://arvaseo.com/terms/) · [Privacy](https://arvaseo.com/privacy/)
