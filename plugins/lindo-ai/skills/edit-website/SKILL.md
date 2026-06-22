---
description: Edits an existing website (across its pages) using AI. Use when the user wants to change copy, layout, styling, or content on a website they already have.
---

# Edit Website

Use the `edit_website` tool to make AI-driven changes to an existing website.

## When to use
- User wants to change something on an existing website
- User asks to rewrite copy, restyle sections, update the header/footer, or adjust layout
- User wants a site-wide change applied across pages

## How to use
1. You need a `website_id` — if the user hasn't specified one, use `list_websites` first and ask which website
2. Call `edit_website` with the `website_id` and a descriptive prompt of the change
3. Include `schedule_at` if the user wants to schedule it
4. The call returns a `workflow_id` — poll `check_edit_status` to track progress
5. Let the user know the edit is running

## Tips
- Be specific about what to change and where (e.g. "update the hero headline on every page")
- Site-wide requests (branding, colors, fonts, nav) are applied across the affected pages
- One edit request per call — describe everything you want changed in a single prompt
