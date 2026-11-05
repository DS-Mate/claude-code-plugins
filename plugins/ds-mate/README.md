# DS-Mate for Claude Code

Ask Claude Code about your DS-Mate dropshipping account: orders, stores,
products, suppliers, unlinked variants, eBay buyer messages, the dashboard
summary and AliExpress product search. You choose what Claude may do when you
sign in; today it can only read.

For example: which orders need your attention and why, one order's status,
items and tracking, how your stores did over the last 7, 30 or 90 days, which
variants are not linked to a supplier yet, and AliExpress products by
keywords, image link or product link. Buyer messages need a DS-Mate plan that
includes messaging.

Paying for or placing supplier orders, importing products, linking variants,
deleting stores and sending buyer messages stay in the DS-Mate dashboard.

## What you need

- A DS-Mate account with at least one connected store
  ([www.ds-mate.com](https://www.ds-mate.com)).

## Install

```
/plugin marketplace add DS-Mate/claude-code-plugins
/plugin install ds-mate@ds-mate
```

The first time a DS-Mate tool runs, Claude Code opens DS-Mate's sign-in page.
Sign in, choose what Claude may read, and approve. To disconnect, go to
DS-Mate, Settings, Connected apps, or run `/mcp` in Claude Code.

## What is inside

- The DS-Mate MCP server at `https://ai.ds-mate.com/mcp` (OAuth sign-in).
- The `dsmate-store-check` skill, which tells Claude which DS-Mate tool
  answers which question.

Tool reference: [www.ds-mate.com/ai/tools](https://www.ds-mate.com/ai/tools)

## Support and privacy

- Support: support@ds-mate.com, [www.ds-mate.com/contact](https://www.ds-mate.com/contact)
- Privacy: [www.ds-mate.com/privacy](https://www.ds-mate.com/privacy)
- Terms: [www.ds-mate.com/terms](https://www.ds-mate.com/terms)
