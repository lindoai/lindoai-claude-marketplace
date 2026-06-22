---
description: Creates a blog post on a website using AI. Use when the user wants to write, publish, or generate a blog post or article.
---

# Create Blog Post

Use the `create_blog` tool to generate an AI-written blog post on a website.

## When to use
- User wants to write or publish a blog post
- User asks for an article, blog entry, or content piece
- User wants to generate SEO content for their website

## How to use
1. You need a `website_id` — use `list_websites` if needed
2. Call `create_blog` with the `website_id` and a prompt describing the blog topic
3. Include `schedule_at` if the user wants to schedule it
4. Let the user know the blog post is being generated

## Alternative: Publish static blog
If the user has pre-written markdown content, use `publish_blog` instead to publish it directly without AI generation. This requires `path`, `blog_content`, and `page_title`.
