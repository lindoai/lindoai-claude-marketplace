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

Optional fields: `featured_image` (photo at the top of the post, on the blog list and for social sharing), `author`, `author_image`, `excerpt`, `category`, `publish_date`, `read_time` and `meta_description`.

## Importing many posts
- Set `publish_date` to each post's original date, so readers see the real date.
- Reuse the same category names across posts. Categories drive the blog list filter, the category colors and the related-posts sidebar, so "News" and "news " should not both exist.
- Set `featured_image` on every post. Posts without one show an empty image on the blog list.
- To fix something after publishing, use `update_blog` (see the manage-content skill). Do not delete and republish.
