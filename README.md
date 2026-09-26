# WarpPay402 MCP Remote Gateway

[![MCP Registry](https://img.shields.io/badge/MCP-Registry_Listed-blue.svg)](https://github.com/modelcontextprotocol/registry)
[![x402 Micropayments](https://img.shields.io/badge/Protocol-x402_USDC-green.svg)](https://api.warppay402.com/.well-known/x402-manifest.json)
[![Status](https://img.shields.io/badge/Gateway-Active-brightgreen.svg)](https://api.warppay402.com/health)

Official Model Context Protocol (MCP) Remote SSE Gateway for **WarpPay402**. This repository hosts the canonical `server.json` manifest for indexing on the official [MCP Registry](https://github.com/modelcontextprotocol/registry).

---

## ⚡ Gateway Quick Connect

- **Remote SSE Endpoint:** `https://api.warppay402.com/mcp?v=2`
- **Transport:** `sse` (Server-Sent Events v2)
- **MCP Manifest:** `https://api.warppay402.com/.well-known/mcp.json`
- **LLM Context Manifest:** `https://api.warppay402.com/llms.txt`
- **OpenAPI Spec:** `https://api.warppay402.com/openapi.json`
- **Agent Card:** `https://api.warppay402.com/.well-known/agent.json`

---

## 🛠️ Provided Tools (28 Monetized Capabilities)

This remote gateway provides AI agents with low-cost, pay-per-use tools monetized via `x402` USDC micropayments across Base, Solana, Arbitrum One, and Arc Mainnet:

1. **`web_scraper`**: Extracts clean Markdown content from public webpages.
2. **`browser_scraper`**: Unblockable headless Chromium page renderer.
3. **`pdf_extractor`**: Plain text extraction from public PDF documents.
4. **`render_screenshot`**: Captures full-page rendered website screenshots.
5. **`extract_json`**: Schema-driven structured JSON extraction from HTML.
6. **`base_analytics`**: Wallet balance and transaction nonce analytics on Base Mainnet.
7. **`arc_analytics`**: Gas pricing and block height metrics on Arc Mainnet.
8. **`arc_network_oracle_query`**: Pre-flight Arc RPC latency and telemetry oracle ($0.10 USDC).
9. **`arc_dex_oracle`**: Real-time ETH/USDC spot price resolver on Arc Mainnet.
10. **`smart_contract_verifier`**: Source code analysis, ABI fetching, and proxy detection via Basescan.
11. **`get_aerodrome_yields`**: Live APYs and TVL for Aerodrome DEX pools on Base.
12. **`aerodrome_swap`**: Programmatic token swap execution on Aerodrome Router.
13. **`aerodrome_clamm`**: Concentrated liquidity range management on Aerodrome Slipstream.
14. **`aerodrome_veaero`**: veAERO locking, epoch voting, and bribe harvesting.
15. **`deploy_contract`**: Programmatic Smart Contract factory for Base Mainnet ($5.00 USDC).
16. **`deploy_solana_contract`**: Programmatic SPL Escrow and Raydium Vault factory for Solana ($5.00 USDC).
17. **`deploy_arc_contract`**: Programmatic Escrow and Bounty contract factory for Arc ($5.00 USDC).
18. **`arc_cctp_bridge`**: Circle CCTP V2 cross-chain USDC bridge engine ($0.25 USDC).
19. **`real_estate_calculator`**: Cap rate, NOI, and cash flow financial calculator.
20. **`address_normalizer`**: USPS address normalization and geocoding via OpenStreetMap.
21. **`weather_oracle`**: Live atmospheric conditions and drone flight clearance oracle.
22. **`forex_oracle`**: Real-time global foreign exchange fiat rates (EUR, GBP, JPY, CAD).
23. **`shipping_rate_estimator`**: Parcel ground, priority, and express shipping rate estimator.
24. **`github_health_analyzer`**: Repository stars, open issue counts, and license inspector.
25. **`property_comps_estimator`**: Property tax assessor and valuation comps estimator.
26. **`public_data_feed`**: Raw signed attestation JSON record feeds ($0.0001 USDC).
27. **`data_feeds`**: Pre-scraped AI intelligence reports ($0.001 USDC).
28. **`x402_telemetry_feed`**: Public on-chain settlement proofs and uptime telemetry (Free).

---

## 💻 Client Configuration

### Claude Desktop (`claude_desktop_config.json`)

To connect Claude Desktop directly to your remote gateway:

```json
{
  "mcpServers": {
    "warppay402-mcp": {
      "url": "https://api.warppay402.com/mcp",
      "transport": "sse"
    }
  }
}
```

### Cursor / OpenClaw

Add `https://api.warppay402.com/mcp` as an SSE Remote Server in your MCP settings panel.

---

## 📦 Related Repositories

- Client SDK: `Warppay402/warppay402-sdk` (`@warppay402/sdk` on NPM)
- NPM Package: `npm install @warppay402/sdk`
- ClawHub Plugin: `clawhub.ai/warppay402/plugins/sdk`

---

## 📄 License

MIT License © 2026 WarpPay402