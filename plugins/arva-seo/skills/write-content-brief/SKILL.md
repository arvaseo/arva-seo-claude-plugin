---
name: write-content-brief
description: Plan a page for an Arva SEO website and save its content brief to Arva SEO. Use when someone asks to write, plan or outline a content brief, article plan or page outline for one of their Arva SEO websites or content pieces, or for a topic or keyword they track in Arva SEO.
---

# Write a content brief for Arva SEO

Arva SEO keeps each website's content pieces (a topic, its target keyword, the business's own experience and the author). This skill plans one piece as a brief and saves it to Arva SEO, where the person reviews it before anything is written.

## Before you start

The Arva SEO tools (`list_websites`, `list_content`, `get_content_piece`, `create_content_piece`, `save_content_brief`) come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in to their Arva SEO account and approve. Then try again.

## Steps

1. **Find the website.** Call `list_websites`. If there's more than one, ask which website the brief is for, unless the request already says. Saving needs `can_edit: true`; if it's false, say the person's role can only read, and offer to write the brief in the chat instead.
2. **Find the content piece.** Call `list_content` for that website and pick the piece that matches the request. If none matches, ask before calling `create_content_piece` with the topic and target keyword.
3. **Read what Arva SEO knows.** Call `get_content_piece`. It returns the business context (website, country, author, the business's first-hand experience, existing pages) and `instructions.brief`, the writing rules and the exact JSON the brief must follow. Follow those instructions; they're the same rules Arva SEO's own writer uses.
4. **Research when you can.** If web search is available, look at what currently ranks for the target keyword to judge search intent and find what the page can do better. Never present guesses about the results as facts.
5. **Write the brief** as the JSON object `instructions.brief` describes: title options, meta description, search intent, audience, angle, word count, outline, FAQs, secondary keywords, internal links (only pages from the context) and the E-E-A-T plan. Base experience and examples on the business's notes only; where they're missing, say what the business should add.
6. **Show it, then save it.** Show the person a readable summary of the brief, then call `save_content_brief`. If Arva SEO answers that the piece already has a brief, ask whether to replace it before calling again with `replace_existing: true`.
7. **Say where to review it:** the piece is in Content in Arva SEO, marked as briefed. The next step is a draft (the write-content-draft skill).

## Rules

- Never invent the business's experiences, results, prices, credentials or customer stories.
- Don't save anything the person hasn't seen, and never overwrite an existing brief without asking.
- Keep the person's language and country in mind (the context says which country the website targets).
