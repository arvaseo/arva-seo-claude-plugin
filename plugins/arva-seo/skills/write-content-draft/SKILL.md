---
name: write-content-draft
description: Write the draft of an Arva SEO content piece from its brief and save it to Arva SEO for review. Use when someone asks to write, draft or rewrite an article, blog post or page for one of their Arva SEO websites or content pieces.
---

# Write a content draft for Arva SEO

This skill writes one content piece in Markdown, from the brief saved in Arva SEO, and saves the draft back to Arva SEO. The person edits, approves and publishes it there.

## Before you start

The Arva SEO tools (`list_websites`, `list_content`, `get_content_piece`, `save_content_draft`) come from the Arva SEO connector. If they aren't available, tell the person to open this plugin's Connectors tab (or Settings → Connectors in Claude), choose Connect next to Arva SEO, sign in to their Arva SEO account and approve. Then try again.

## Steps

1. **Find the piece.** Call `list_websites` (ask which website if there are several), then `list_content`, and pick the piece the person means.
2. **Read it.** Call `get_content_piece`. It returns the brief, the business context and `writing_guidelines.draft`: how an Arva SEO draft is laid out, and its accuracy and E-E-A-T rules. If the piece has no brief yet, offer to write one first (the write-content-brief skill); a draft without a brief is weaker.
3. **Write the draft** in Markdown, following `writing_guidelines.draft` and the brief's outline, search intent and angle:
   - The H1, then the byline exactly as the author is given, or the placeholder the guidelines name.
   - First-hand experience only from the business's notes. Where the brief asks for experience, examples, photos or data the notes don't have, add the bracketed placeholder the guidelines describe, so the person fills it in.
   - Careful claims, with a source placeholder where a source is needed. Never invent statistics, studies, quotes or prices.
   - The FAQ section, a short conclusion with a helpful next step, and the "Last reviewed" line.
4. **Show it, then save it.** Show the draft, make any changes the person asks for, then call `save_content_draft` with the Markdown only (no code fences). If Arva SEO answers that a draft already exists, ask whether to replace it before calling again with `replace_existing: true`.
5. **Say where to review it:** the draft is in Content in Arva SEO. The person fills in the bracketed placeholders, then approves and publishes.

## Rules

- Never invent the business's experiences, results, credentials, reviews or customer stories; placeholders are better than fiction.
- Don't save anything the person hasn't seen, and never overwrite an existing draft without asking.
- Write for the people searching, not for search engines: plain language, short paragraphs, the target keyword used naturally.
