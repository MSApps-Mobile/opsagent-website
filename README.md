# opsagent-website

Source for **[opsagents.agency](https://opsagents.agency)** — the OpsAgent marketing landing page.

- **Netlify site:** `opsagent-website` (ID `8c9ec390-2269-43d0-8a95-cf1eefbdbcb7`)
- **Primary domain:** [opsagents.agency](https://opsagents.agency)
- **www:** redirects to apex
- **Sister sites (separate repos/deploys):**
  - [claude.opsagents.agency](https://claude.opsagents.agency) — Claude plugin marketplace
  - [shopify.opsagents.agency](https://shopify.opsagents.agency) — Shopify Partner landing page

## Stack

Plain static HTML — no build step. Everything lives in `index.html`.

## Deploy

```bash
# Manual deploy (current workflow)
npx netlify-cli deploy --prod --dir=. --site=8c9ec390-2269-43d0-8a95-cf1eefbdbcb7
```

## Navbar / Footer — do NOT drop these links

Navbar must always include:

- Services, Integrations, How It Works, SOSA™, Security, Pricing, **Claude**, **Shopify**, Get Started

Footer must always include:

- SOSA™ Framework, **Claude Agents**, **Shopify**, Contact, Privacy, Terms, Support

The Claude and Shopify links are revenue-critical — they route visitors to the two
active conversion subdomains. A prior redeploy (pre-2026-04-21) silently dropped
them and cost bizdev funnel visibility. If you're editing the navbar or footer,
keep them in.

## History

See [Notion — OpsAgents Domain Setup Session Log](https://www.notion.so/34038b5dfb27817fa736c822f2d91a92)
for full history, DNS config, email setup, and deploy cheat sheet.
