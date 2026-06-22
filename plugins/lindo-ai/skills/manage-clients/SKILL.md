---
description: Manages workspace clients — create, list, update, delete clients, assign websites, generate login links, and allocate credits. Use when the user wants to manage their agency clients.
---

# Manage Clients

Tools for managing clients in the workspace.

## Available tools
- `create_client` — Create a new client (name, email, optional phone)
- `list_clients` — List all clients in the workspace
- `update_client` — Update client details
- `delete_client` — Remove a client
- `assign_website` — Assign a website to a client
- `generate_magic_link` — Generate a login link for a client to access their dashboard
- `allocate_credits` — Give credits to a client (monthly, purchased, or daily)

## When to use
- User asks about clients, customers, or accounts
- User wants to onboard a new client
- User wants to give a client access to their website
- User asks about credits or billing for a client

## Tips
- When creating a client, name and email are required
- When assigning a website, you need both `website_id` and `client_id` — use list tools if needed
- Magic links let clients log in without a password
- Credit types: `monthly` (resets each cycle), `purchased` (permanent), `daily` (resets daily)
