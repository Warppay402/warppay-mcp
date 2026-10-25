# WarpPay402 MCP Gateway

[![MCP Registry](https://img.shields.io/badge/MCP-Registry_Listed-blue.svg)](https://github.com/modelcontextprotocol/registry)
[![x402 Micropayments](https://img.shields.io/badge/Protocol-x402_USDC-green.svg)](https://api.warppay402.com/.well-known/x402-manifest.json)
[![Status](https://img.shields.io/badge/Gateway-Active-brightgreen.svg)](https://api.warppay402.com/health)
[![M8ven Score](https://m8ven.ai/badge/mcp/warppay402-warppay-mcp-18kjig)](https://m8ven.ai/mcp/warppay402-warppay-mcp-18kjig?s=readme)

Official Model Context Protocol (MCP) remote SSE gateway for **WarpPay402**. This repository hosts the canonical `server.json` manifest used for registry indexing and connectivity metadata.

---

## ⚡ Gateway Quick Connect

- **Remote SSE Endpoint:** `https://api.warppay402.com/mcp?v=2`
- **Transport:** `sse` (Server-Sent Events v2)
- **MCP Manifest:** `https://api.warppay402.com/.well-known/mcp.json`
- **LLM Context Manifest:** `https://api.warppay402.com/llms.txt`
- **OpenAPI Spec:** `https://api.warppay402.com/openapi.json`
- **Agent Card:** `https://api.warppay402.com/.well-known/agent.json`

---

## 🛠️ Provided Tools (29 Monetized Capabilities)

This remote gateway exposes AI agents to low-cost, pay-per-use tools monetized via `x402` USDC micropayments across Base, Solana, Arbitrum One, and Arc Mainnet:

1. **`public_data_feed`**: Raw signed attestation JSON record feeds ($0.0001 USDC).
2. **`data_feeds`**: Pre-scraped AI intelligence and market reports ($0.001 USDC).
3. **`web_scraper`**: Extracts clean Markdown content from public webpages ($0.001 USDC).
4. **`browser_scraper`**: Unblockable headless Chromium page renderer ($0.005 USDC).
5. **`base_analytics`**: Wallet balance and transaction nonce analytics on Base Mainnet ($0.002 USDC).
6. **`arc_analytics`**: Gas pricing, latency, and block height metrics on Arc Mainnet ($0.001 USDC).
7. **`arc_network_oracle_query`**: Pre-flight Arc RPC latency and telemetry oracle ($0.10 USDC).
8. **`arc_dex_oracle`**: Real-time ETH/USDC spot price resolver on Arc Mainnet ($0.001 USDC).
9. **`pdf_extractor`**: Plain text extraction from public PDF documents ($0.005 USDC).
10. **`render_screenshot`**: Captures full-page rendered website screenshots ($0.01 USDC).
11. **`extract_json`**: Schema-driven structured JSON extraction from HTML ($0.01 USDC).
12. **`smart_contract_verifier`**: Source code analysis, ABI fetching, and proxy detection via Basescan ($0.02 USDC).
13. **`get_aerodrome_yields`**: Live APYs, TVL, and pool contract addresses for Aerodrome on Base ($0.003 USDC).
14. **`aerodrome_swap`**: Programmatic low-slippage token swaps on Aerodrome Base Router ($0.01 USDC).
15. **`aerodrome_clamm`**: Concentrated liquidity range management on Aerodrome Slipstream ($0.01 USDC).
16. **`aerodrome_veaero`**: veAERO locking, epoch gauge voting, and bribe harvesting ($0.01 USDC).
17. **`deploy_contract`**: Programmatic smart contract deployment factory for Base Mainnet ($5.00 USDC).
18. **`deploy_solana_contract`**: Programmatic SPL Escrow, cNFT Badge, and Raydium Vault factory ($5.00 USDC).
19. **`deploy_arc_contract`**: Programmatic Escrow and Bounty contract factory for Arc Mainnet ($5.00 USDC).
20. **`arc_cctp_bridge`**: Circle CCTP V2 cross-chain USDC bridge engine ($0.25 USDC).
21. **`real_estate_calculator`**: Cap rate, NOI, and cash flow financial calculator ($0.0005 USDC).
22. **`address_normalizer`**: USPS address normalization and geocoding via OpenStreetMap ($0.001 USDC).
23. **`weather_oracle`**: Live atmospheric conditions and drone flight clearance oracle ($0.001 USDC).
24. **`outage_oracle`**: Real-time utility grid, ISP broadband, and cellular blackout oracle ($0.002 USDC).
25. **`forex_oracle`**: Real-time global foreign exchange fiat spot rates (EUR, GBP, JPY, CAD) ($0.0005 USDC).
26. **`shipping_rate_estimator`**: USPS ground, priority, and express rate estimator ($0.001 USDC).
27. **`github_health_analyzer`**: Repository stars, open issue counts, and license inspector ($0.002 USDC).
28. **`property_comps_estimator`**: Property tax assessor and valuation comps estimator ($0.005 USDC).
29. **`ucp_deals_oracle`**: Universal Commerce Protocol product catalog, inventory, and deal finder ($0.001 USDC).

---

## 💻 Client Configuration

### Claude Desktop (`claude_desktop_config.json`)

To connect Claude Desktop directly to your remote gateway:

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

## 📦 Related Repositories

- Client SDK: `Warppay402/warppay402-sdk` (`@warppay402/sdk` on NPM)
- NPM Package: `npm install @warppay402/sdk`
- ClawHub Plugin: `https://clawhub.ai/warppay402/plugins/sdk`

---

## 📄 License

MIT License © 2026 WarpPay402