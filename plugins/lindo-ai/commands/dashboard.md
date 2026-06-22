---
description: Show a summary dashboard of your Lindo AI workspace — websites, clients, and usage at a glance.
---

Generate a workspace dashboard summary:

1. Use `list_websites` to get all websites
2. Use `list_clients` to get all clients
3. Present a clean summary:

**Workspace Overview**
- Total websites: [count]
- Total clients: [count]
- Websites with custom domains: [count]

**Recent Websites** (last 5)
| Name | Domain | Status |
|------|--------|--------|

**Clients** (all)
| Name | Email | Websites Assigned |
|------|-------|-------------------|

Keep it brief and scannable. Don't fetch analytics unless the user asks.
