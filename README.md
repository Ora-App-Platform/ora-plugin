# Ora for Cursor

Sell tickets to your events without leaving the chat. Ora is an event ticketing
and marketing platform; this plugin connects Cursor's agent to your Ora account.

- **Organizers:** create an event from one prompt, set ticket tiers and promo
  codes, publish, get share links and a QR code for each channel, follow sales,
  attendance and payouts.
- **Anyone:** find Ora events near you and open their pages. Tickets are always
  bought on oraapp.com, never in the chat.

## Install

Install **Ora** from the Cursor Marketplace. The plugin adds one MCP server:

```json
{ "mcpServers": { "ora": { "url": "https://www.oraapp.com/api/mcp/ora" } } }
```

No API key: the first time a tool needs your account, Cursor opens Ora's
sign-in page. Sign in with your email or phone code (a new email creates an Ora
account), choose which of your Ora accounts Cursor should use — organizer,
venue, sponsor/vendor, creator or customer — and approve. You can switch
accounts later by asking in the chat. To disconnect, say "sign out of Ora": it
ends Cursor's connection on Ora's side, and the next request asks you to sign in
again. You can also remove the server from Cursor's MCP settings.

## Try it

- "Help me sell tickets to a rooftop yoga brunch on Nov 8 at 10am in Austin,
  80 spots at $25, then publish it."
- "Add an early-bird tier: 30 tickets at $20 until Oct 25, and a 15% code
  RUNCLUB."
- "How's my rooftop yoga brunch selling? Which channel is working?"
- "Find something fun in Austin this Saturday."
- "Which Ora account am I using?" / "Switch to my organizer account."

## What it can and cannot do

| Can | Cannot |
|---|---|
| Create, edit, publish, pause and duplicate your events | Show attendee names, emails or phone numbers (totals only) |
| Ticket tiers, promo codes, share links and QR codes | Buy tickets in the chat — buyers go to the Ora event page |
| Sales, attendance and post-event totals; payout status | Issue refunds or message attendees (use the Ora dashboard) |
| Search Ora events and follow organizers | Act as an Ora admin |

Event cards, the sales dashboard and the ticket editor appear as interactive
views where Cursor supports MCP Apps, and as text otherwise. Uploading a flyer
from a chat attachment works where the assistant provides file attachments;
otherwise add the cover image on oraapp.com.

New organizers can build and save events right away; an event goes live after
Ora approves the organizer account.

## Skill

`skills/sell-tickets` walks the agent through a first event: confirm the
account, collect the essentials in one question, create a draft, publish only on
a clear yes, share it, then follow sales and payouts.

## Privacy and support

- Privacy policy: https://www.oraapp.com/privacy
- Terms: https://www.oraapp.com/terms
- Help: https://www.oraapp.com/help · help@oraapp.com

Ora receives what you type into its tools (event details, ticket prices, promo
codes) and the approximate location Cursor shares for a search. It sends back
totals for your own events only.

## License

MIT — see `LICENSE`. This repository holds the plugin manifest only; the Ora
service it connects to is operated by Kivo Ora Corp.
