---
description: Creates a new website using AI. Use when the user wants to build, create, or spin up a website, landing page, or online presence for a business.
---

# Create Website

Use the `create_website` tool to create a new website from a text prompt.

## When to use
- User asks to create, build, or make a website
- User describes a business and wants an online presence
- User wants a landing page, portfolio, or company site

## How to use
1. Ask the user what kind of website they want if the prompt is vague
2. Call `create_website` with a detailed prompt describing the business, style, and pages
3. Include `schedule_at` (ISO 8601) if the user wants to schedule it for later
4. The tool returns an `instance_id` — let the user know the website is being created and it takes a few minutes

## Tips for good prompts
- Include the business name, industry, and desired style
- Mention specific pages if the user has preferences (e.g. "with a gallery and contact page")
- Include color scheme or mood if mentioned (e.g. "modern dark theme", "warm and inviting")
