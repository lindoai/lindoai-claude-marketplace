---
description: Manages pages and blog posts — list, view, publish, update, unpublish, and delete content on websites. Use when the user wants to manage existing pages or blog posts.
---

# Manage Content

Tools for managing pages and blog posts on websites.

## Page tools
- `list_pages` — List all pages on a website
- `get_page` — Get page details
- `publish_page` — Publish a static HTML page
- `update_page` — Update page metadata (name, path, SEO)
- `update_page_content` — Update page HTML content
- `unpublish_page` — Take a page offline
- `delete_page` — Delete a page
- `get_page_html` — Get the raw HTML of a page

## Blog tools
- `list_blogs` — List blog posts on a website (12 per page, use `page` for more)
- `get_blog` — Get blog post details
- `publish_blog` — Publish a static markdown blog post, with optional `featured_image` and `author_image`
- `update_blog` — Change a post's featured image, author, author image, category, excerpt, publish date, SEO, name or path without touching its content
- `update_blog_content` — Replace a blog post's body
- `unpublish_blog` — Take a blog post offline
- `delete_blog` — Delete a blog post
- `get_blog_html` — Get a post's current body, path, SEO and blog settings

## Editing a blog post
Never delete and recreate a post to edit it. That gives it a new ID and created date, which moves it in the blog list order.
- **Images, author, category, date or excerpt:** call `update_blog` with only the fields to change. Use `featured_image` for the photo at the top of the post (it is also the blog list and social share image). Put `author_image`, `author`, `category`, `excerpt` and `publish_date` in `blog_settings`. Everything you leave out is kept, and the live post is republished.
- **The text of the post:** call `get_blog_html`, change the part the user asked for, then send the full body back with `update_blog_content`.
- **Many posts at once:** loop over `list_blogs` pages and call `update_blog` per post.

## Blog list settings
Post order on the blog list, category colors and the related-posts sidebar are set by the user in Settings → SEO → Blog Config. There is no tool for them, so point the user there.

## When to use
- User asks to see, edit, or manage pages or blog posts
- User wants to change a blog post's image, author photo, category or date
- User wants to publish pre-written content (HTML for pages, markdown for blogs)
- User wants to unpublish or delete content
