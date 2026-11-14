# WarpPay402 MCP Gateway

[![MCP Registry](https://img.shields.io/badge/MCP-Registry_Listed-blue.svg)](https://github.com/modelcontextprotocol/registry)
[![x402 Micropayments](https://img.shields.io/badge/Protocol-x402_USDC-green.svg)](https://api.warppay402.com/.well-known/x402-manifest.json)
[![Status](https://img.shields.io/badge/Gateway-Active-brightgreen.svg)](https://api.warppay402.com/health)
[![M8ven Score](https://m8ven.ai/badge/mcp/warppay402-warppay-mcp-18kjig)](https://m8ven.ai/mcp/warppay402-warppay-mcp-18kjig?s=readme)

Official Model Context Protocol (MCP) and Agent-to-Agent (A2A) remote gateway for **WarpPay402**. This repository hosts the canonical `server.json` manifest used for registry indexing and connectivity metadata.

---

## ⚡ Gateway Quick Connect

- **Remote MCP Endpoint (SSE & Streamable HTTP):** `https://api.warppay402.com/mcp?v=2`
- **Transport:** `sse` (Server-Sent Events v2) / Streamable JSON-RPC
- **MCP Manifest:** `https://api.warppay402.com/.well-known/mcp.json`
- **A2A Agent Card:** `https://api.warppay402.com/.well-known/agent.json`
- **x402 Manifest:** `https://api.warppay402.com/.well-known/x402-manifest.json`
- **LLM Context Manifest:** `https://api.warppay402.com/llms.txt`
- **OpenAPI Spec:** `https://api.warppay402.com/openapi.json`

---

## 🤖 Stateless Autonomous Multi-Agent Workflows

Instead of stitching multiple API calls client-side, agents can send a single natural-language goal with an x402 USDC micropayment and let the gateway orchestrate the entire multi-step workflow autonomously:

- **`warppay_defi_executor` ($0.15 USDC):** Autonomous DeFi due-diligence and quote agent that audits wallets/contracts, queries live Aerodrome Base pool yields, and simulates swap routes in a single execution (`POST /api/v1/agents/defi-executor`).
- **`warppay_deep_research` ($0.05 USDC):** Parallel research workflow combining UCP merchant catalog search, live web scraping, and forex spot rates into a synthesized JSON report (`POST /api/v1/agents/deep-research`).
- **`warppay_a2a_concierge` ($0.02 USDC):** Stateless tool-equipped A2A task agent available via JSON-RPC `message/send` on `/mcp?v=2`.

---

## 🛠️ Provided Tools (31 Monetized Capabilities)

This remote gateway exposes AI agents to low-cost, pay-per-use tools monetized via `x402` USDC micropayments across Base, Robinhood Chain, Solana, Arbitrum One, and Arc Mainnet:

1. **`public_data_feed` ($0.0001 USDC):** Raw signed attestation JSON record feeds.
2. **`data_feeds` ($0.001 USDC):** Pre-scraped AI intelligence and market reports.
3. **`web_scraper` ($0.001 USDC):** Extracts clean Markdown content from public webpages.
4. **`browser_scraper` ($0.005 USDC):** Unblockable headless Chromium page renderer.
5. **`base_analytics` ($0.002 USDC):** Wallet balance and transaction nonce analytics on Base Mainnet.
6. **`arc_analytics` ($0.001 USDC):** Gas pricing, latency, and block height metrics on Arc Mainnet.
7. **`arc_network_oracle_query` ($0.10 USDC):** Pre-flight Arc RPC latency and telemetry oracle.
8. **`arc_dex_oracle` ($0.001 USDC):** Real-time ETH/USDC spot price resolver on Arc Mainnet.
9. **`pdf_extractor` ($0.005 USDC):** Plain text extraction from public PDF documents.
10. **`render_screenshot` ($0.01 USDC):** Captures full-page rendered website screenshots.
11. **`extract_json` ($0.01 USDC):** Schema-driven structured JSON extraction from HTML.
12. **`smart_contract_verifier` ($0.02 USDC):** Source code analysis, ABI fetching, and proxy detection via Basescan.
13. **`get_aerodrome_yields` ($0.003 USDC):** Live APYs, TVL, and pool contract addresses for Aerodrome on Base.
14. **`aerodrome_swap` ($0.01 USDC):** Programmatic low-slippage token swaps on Aerodrome Base Router.
15. **`aerodrome_clamm` ($0.01 USDC):** Concentrated liquidity range management on Aerodrome Slipstream.
16. **`aerodrome_veaero` ($0.01 USDC):** veAERO locking, epoch gauge voting, and bribe harvesting.
17. **`aerodrome_quote_simulator` ($0.001 USDC):** Read-only spot quote and price impact simulator for Aerodrome Base.
18. **`wallet_reputation_oracle` ($0.01 USDC):** Wallet sanctions and anti-poisoning reputation oracle.
19. **`solana_token_risk_oracle` ($0.005 USDC):** SPL token mint and freeze authority security oracle.
20. **`multi_chain_gas_oracle` ($0.001 USDC):** Real-time EIP-1559 gas station telemetry across Base, Arbitrum, Robinhood, and Arc.
21. **`arc_cctp_bridge` ($0.25 USDC):** Circle CCTP V2 cross-chain USDC bridge engine.
22. **`real_estate_calculator` ($0.0005 USDC):** Cap rate, NOI, and cash flow financial calculator.
23. **`address_normalizer` ($0.001 USDC):** USPS address normalization and geocoding via OpenStreetMap.
24. **`weather_oracle` ($0.001 USDC):** Live atmospheric conditions and drone flight clearance oracle.
25. **`outage_oracle` ($0.002 USDC):** Real-time utility grid, ISP broadband, and cellular blackout oracle.
26. **`forex_oracle` ($0.0005 USDC):** Real-time global foreign exchange fiat spot rates (EUR, GBP, JPY, CAD).
27. **`shipping_rate_estimator` ($0.001 USDC):** USPS ground, priority, and express rate estimator.
28. **`github_health_analyzer` ($0.002 USDC):** Repository stars, open issue counts, and license inspector.
29. **`property_comps_estimator` ($0.005 USDC):** Property tax assessor and valuation comps estimator.
30. **`ucp_deals_oracle` ($0.001 USDC):** Universal Commerce Protocol product catalog, inventory, and deal finder.
31. **`fast_intelligence` ($0.001 USDC):** Sub-second deterministic text classification, summarization, and triage.

---

## 💻 Client Configuration

### Claude Desktop (`claude_desktop_config.json`)

```json
{
  "mcpServers": {
    "warppay402-mcp": {
      "url": "https://api.warppay402.com/mcp?v=2",
      "transport": "sse"
    }
  }
}
```

### Cursor / OpenClaw

Add `https://api.warppay402.com/mcp?v=2` as an SSE remote server in your MCP settings panel.

---

## 📦 Related Repositories & SDKs

- **TypeScript SDK:** `@warppay402/sdk` (v1.4.1 on NPM) - `Warppay402/warppay402-sdk`
- **Stdio Auto-Signing Bridge:** `@warppay402/mcp-client` - `Warppay402/warppay402-mcp-client`
- **Python MCP & LangChain Suite:** `warppay402-mcp` (v1.3.0 on PyPI) - `Warppay402/warppay402-python`
- **Semantic Kernel Plugin:** `semantic-kernel-warppay402` (v1.1.0 on PyPI)
- **AutoGen Integration:** `autogen-warppay402` (v1.1.0 on PyPI)
- **ClawHub Plugin:** `https://clawhub.ai/warppay402/plugins/sdk`

---

## 📄 License

MIT License © 2026 WarpPay402
