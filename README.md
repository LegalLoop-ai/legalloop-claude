# Legal Loop for Claude Code

The legal API for the agent era. Deterministic, citation-backed legal answers for your AI, with the exact statute and the full reasoning path.

This plugin installs, in one step:

- The **`/legalloop:ll`** skill, which fires automatically on any legal, privacy, or compliance question and runs it through Legal Loop's deterministic engine.
- The **Legal Loop MCP connector** (`mcp.legalloop.ai`), 64 codified frameworks across 14 jurisdictions.

Legal Loop runs no AI on its servers. The determination is a deterministic traversal of encoded law. Your model routes the question; Legal Loop answers it.

---

## Install (Claude Code)

```
/plugin marketplace add LegalLoop-ai/legalloop-claude
/plugin install legalloop
```

That is everything. The skill and the MCP are both live. On first use, the MCP will prompt you to sign in through your browser (OAuth); use your Legal Loop account.

Ask a legal question in plain language and the skill takes over:

```
Does COPPA apply to our mobile game aimed at kids?
```

You will get a Legal Loop determination: the outcome, the obligations, the citation, the penalty exposure, and the full reasoning path.

---

## Add the MCP only (no skill)

If you only want the connector:

```
claude mcp add --transport http legalloop https://mcp.legalloop.ai/mcp
```

The two tools (`query_legal_obligation`, `list_legal_frameworks`) are then available to your model directly. The skill is what turns them into a guided, verbatim, branded flow, so we recommend installing the full plugin.

---

## Claude Desktop

Claude Desktop does not support skills or plugins. Add the MCP as a connector:

1. Settings → Connectors → Add custom connector
2. URL: `https://mcp.legalloop.ai/mcp`
3. Sign in through the browser when prompted (OAuth)

---

## Coverage

GDPR, UK GDPR + DUAA, the EU AI Act, DSA, DMA, DORA, NIS2, ePrivacy/cookies, all 20 US state privacy laws in effect for 2026, US AI laws (Colorado AI Act, Texas TRAIGA, Illinois HB 3773, NYC LL 144, EEOC), BIPA and Texas CUBI biometrics, data broker laws (CA Delete Act, NJ A5328), COPPA, HIPAA, Quebec Law 25, Brazil LGPD, China PIPL, Japan APPI, India DPDPA, South Korea AI Basic Act, Australia Privacy Act, Saudi PDPL, and more.

---

Legal Loop. hello@legalloop.ai · https://legalloop.ai
