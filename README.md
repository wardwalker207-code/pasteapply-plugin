# PasteApply — Cursor / Grok Bot plugin

Honest resume and cover-letter tailor for agents. Free generate returns a truncated teaser; humans unlock full files via Stripe.

- **Product:** https://pasteapply.com  
- **Agent docs:** https://pasteapply.com/agents.md  
- **Honesty / fact-lock:** https://pasteapply.com/honesty  
- **Remote MCP:** https://pasteapply.com/mcp  
- **Official MCP Registry:** `com.pasteapply/mcp`

## Install

### From this repo (local / marketplace git)
Install the plugin from this repository in Cursor / Grok Bot marketplace, or clone and load as a local plugin.

### Or connect MCP only
Add to your MCP config:

```json
{
  "mcpServers": {
    "pasteapply": {
      "url": "https://pasteapply.com/mcp"
    }
  }
}
```

No API key required for `status` / `generate` / `unlock_link`.

## What it does
- Bundles remote Streamable HTTP MCP at `https://pasteapply.com/mcp`
- Ships the **PasteApply honest tailor** skill (generate → teaser → human Checkout → confirm)
- Pricing for humans: **$3/mo** unlock · **$5 Export** (default ask) · **$10 Pro**

## Agent loop
1. `generate` with real job + resume  
2. Show human the free teaser + coverage/proof  
3. `unlock_link` → hand Checkout URL to human  
4. `confirm_payment` / poll `get_generation` after pay  

Never invent facts. Never complete Stripe as the user.

## License
MIT
