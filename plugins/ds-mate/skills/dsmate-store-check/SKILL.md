---
name: dsmate-store-check
description: Check a DS-Mate dropshipping account with the DS-Mate tools. Use when the user asks which orders need attention, about one order, unlinked variants, store performance, suppliers, buyer messages, or to find AliExpress products.
---

# DS-Mate store check

The DS-Mate tools read the seller's own DS-Mate account. They are read only:
they never pay, place, cancel or fulfil an order, import a product, link a
variant, delete a store or send a buyer message. When the user asks for one
of those, say that it is done in the DS-Mate dashboard and that nothing was
changed.

## Start

Call `dsmate_get_account` first. It names the seller's stores, plan and
connected suppliers, so later calls can be scoped to the right store.

## Which tool answers what

| The user asks | Tool |
| --- | --- |
| Which orders need my attention | `dsmate_list_orders` with `attention` (the dashboard's "Awaiting your action"), then `dsmate_get_order` for the reason and next step |
| One order: status, items, tracking | `dsmate_get_order` |
| How did my stores do | `dsmate_get_dashboard_summary` (periods: last 7, 30 or 90 days) |
| Variants with no supplier | `dsmate_list_unmapped_variants` |
| My stores and their products | `dsmate_list_stores`, `dsmate_list_store_products` |
| My supplier accounts | `dsmate_list_suppliers` |
| Buyer messages (eBay, on a plan with messaging) | `dsmate_list_messages`, `dsmate_get_message_thread` |
| Find products on AliExpress | `dsmate_search_products` (keywords), `dsmate_search_by_image` (image link), `dsmate_get_product_by_url` (product link) |

## How to answer

- Report what the tools returned, with order numbers and statuses as DS-Mate
  shows them. Do not guess a value a tool did not return.
- When a figure is still settling (fees, profit), say so.
- Shipping costs from product search are DS-Mate's estimate, not a quote.
- If a tool asks the user to sign in again, tell them to reconnect DS-Mate
  with `/mcp`.
