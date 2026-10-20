# BnBGenius MCP server

Connect your own AI (Claude, ChatGPT or any MCP client) to your [BnBGenius](https://bnbgenius.ai) account and ask about your short-term rentals in plain language.

**Server URL:** `https://my.bnbgenius.ai/mcp` (Streamable HTTP)

BnBGenius is not affiliated with, endorsed by or sponsored by Airbnb or VRBO.

## What it does

Read-only access to your own BnBGenius data:

- Listings, listing details and occupancy
- Reservations, reservation details, revenue, occupancy and nightly-rate metrics
- Guests and top guests
- Guest message inbox: conversations, search, unread counts and full message history
- Pending host reviews and their status
- Gap-night upsell offers and recovered revenue
- Chrome extension connection status
- Account credits and plan

It cannot send messages, approve upsells, submit reviews or change settings. Each user only ever sees their own account's data.

## Requirements

- A BnBGenius account with the BnBGenius Chrome extension connected (it keeps your Airbnb and VRBO data up to date).

## Connect in Claude

1. Open **Settings → Connectors → Add → Add custom connector**.
2. Name: `BnBGenius`. Server URL: `https://my.bnbgenius.ai/mcp`.
3. Click **Add**, then **Connect**, sign in with your BnBGenius login and choose your account.

Then ask things like "Which guests check in this week?", "How many messages need a reply?" or "Show my pending reviews".

## Authentication

OAuth 2.1 through Clerk (`https://clerk.bnbgenius.ai`), with Client ID Metadata Documents. Scopes: `user:org:read`, `offline_access`.

## Support

hello@bnbgenius.ai
