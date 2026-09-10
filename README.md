# PasteApply

**Honest resume & cover-letter tailor for job-apply agents.**

Install this plugin → your agent gets PasteApply MCP + a skill that refuses to invent employers, dates, or skills. Free preview for the human; they unlock downloads when they want the file.

| | |
| --- | --- |
| Product | https://pasteapply.com |
| MCP | https://pasteapply.com/mcp |
| Agent docs | https://pasteapply.com/agents.md |
| Honesty | https://pasteapply.com/honesty |
| Registry | `com.pasteapply/mcp` |

## Why install

Raw LLMs invent careers. PasteApply only rearranges what’s already true, returns a **teaser** for free, and makes the **human** pay Stripe for the full letter/resume/files. That’s the product — and the trust model.

## 2-minute first run

1. Install this plugin from the Cursor / Grok Bot marketplace (or clone locally).
2. In a new chat, ask: *“Tailor my resume for this job with PasteApply”* and paste a real posting + resume (or say *use the sample*).
3. Agent calls MCP `generate` → shows you the teaser + coverage/proof.
4. When you want the file: agent calls `unlock_link` and gives you the Checkout URL ($5 Export default · $3/mo · $10 Pro).
5. After you pay, agent confirms and continues the apply flow.

**Hard rules for agents:** never invent facts; never complete Stripe as you.

## MCP only (no plugin UI)

```json
{
  "mcpServers": {
    "pasteapply": {
      "type": "http",
      "url": "https://pasteapply.com/mcp"
    }
  }
}
```

Tools: `status` · `generate` · `unlock_link` · `confirm_payment` · `get_generation`  
No API key for those.

## Skill

`skills/pasteapply-honest-tailor` — use whenever a job-apply bot needs a tailored resume or cover letter.

## Pricing (humans)

- Generate / teaser: **free**
- **$3/mo** unlock · **$5 Export** (default ask) · **$10 Pro**

## License

MIT
