<p align="center">
  <img src="./assets/logo.png" width="130" height="130" alt="Vector Graphics Pipeline MCP Logo" />
</p>

# Vector Graphics Pipeline MCP

[![Smithery Compatible](https://img.shields.io/badge/Smithery-Compatible-blue.svg)](https://smithery.ai)
[![Model Context Protocol](https://img.shields.io/badge/MCP-Standard%20v1.0-emerald.svg)](https://modelcontextprotocol.io)
[![Base L2 Settlement](https://img.shields.io/badge/Base%20L2-USDC%20x402-blue.svg)](https://base.org)
[![Tools](https://img.shields.io/badge/Tools-4%20Curated-purple.svg)](#included-tools)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Vector SVG path optimization, sub-pixel PNG rasterization, EXIF scrubbing, and vector QR code generation.**

Built specifically for Frontend UI engineers, graphic designers, print-on-demand sellers, and vector asset generation agents.

---

## ⚡ Quickstart

### Smithery Install
```bash
smithery skill add whambammy/vector-graphics-pipeline-mcp
```

### Claude Desktop / Cursor (`claude_desktop_config.json`)
```json
{
  "mcpServers": {
    "vector-graphics-pipeline-mcp": {
      "command": "npx",
      "args": ["-y", "@whambammy/vector-graphics-pipeline-mcp"],
      "env": {
        "PAYMENT_WALLET": "0x9793E7269b3301893318dEa8338576Ba612F39B3",
        "BASE_RPC_URL": "https://mainnet.base.org"
      }
    }
  }
}
```

---

## 🛠️ Included Tools

| Tool Name | Price (USDC) | Capability |
| :--- | :---: | :--- |
| `optimize_vector_svg` | $0.02 | Strips bloated XML, cleans SVG nodes, converts paths for direct cutting, sublimation, and high-performance web graphics. |
| `convert_svg_to_png` | $0.015 | Deterministic SVG to PNG rasterizer with crisp sub-pixel antialiasing, custom DPI, and transparent alpha channel preservation. |
| `generate_qr_code_svg` | $0.01 | Generates high-precision scalable vector (SVG) QR codes with High error correction (ECC Level H), tailored for Base payment URIs. |
| `compress_image_webp` | $0.025 | Serverless WebP image compressor: optimizes alpha channels, strips privacy-invasive EXIF tags, and cuts image weight by 80%. |


---

## 🔄 End-to-End Workflow

A designer agent generates an SVG graphic -> optimizes vector paths and cleans nodes for web rendering -> produces high-res crisp PNG previews -> embeds a vector QR code -> compresses the final preview to WebP.

---

## 💰 The x402 Base L2 Micropayment Protocol

When an agent invokes a tool without payment, the server responds with a deterministic `HTTP 402 Payment Required` challenge containing:
- Target tool price in USDC
- Base Native USDC Contract: `0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`
- Recipient payout wallet address
- Single-use cryptographic nonce

Once broadcasted on Base L2, resubmitting with `paymentSignature` unlocks deterministic execution.

---

## 📄 License
MIT License. Created by [Whambammy](https://github.com/Whambammy).
