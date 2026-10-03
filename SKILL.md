---
name: vector-graphics-pipeline-mcp
description: Vector SVG path optimization, sub-pixel PNG rasterization, EXIF scrubbing, and vector QR code generation. Use when an autonomous agent needs optimize_vector_svg or related tools.
metadata: { "icon": "https://raw.githubusercontent.com/Whambammy/vector-graphics-pipeline-mcp/main/assets/logo.png", "homepage": "https://github.com/Whambammy/vector-graphics-pipeline-mcp" }
---

# Vector Graphics Pipeline MCP

**Vector SVG path optimization, sub-pixel PNG rasterization, EXIF scrubbing, and vector QR code generation.**

Part of the WHAM ENGINE fleet of deterministic AI agent micro-services with automated **Base L2 HTTP 402 (x402) USDC micropayments**.

---

## Tools Included in this Suite (4 Tools)

- `optimize_vector_svg`: Strips bloated XML, cleans SVG nodes, converts paths for direct cutting, sublimation, and high-performance web graphics.
- `convert_svg_to_png`: Deterministic SVG to PNG rasterizer with crisp sub-pixel antialiasing, custom DPI, and transparent alpha channel preservation.
- `generate_qr_code_svg`: Generates high-precision scalable vector (SVG) QR codes with High error correction (ECC Level H), tailored for Base payment URIs.
- `compress_image_webp`: Serverless WebP image compressor: optimizes alpha channels, strips privacy-invasive EXIF tags, and cuts image weight by 80%.

---

## Recommended Workflow

A designer agent generates an SVG graphic -> optimizes vector paths and cleans nodes for web rendering -> produces high-res crisp PNG previews -> embeds a vector QR code -> compresses the final preview to WebP.

---

## Quickstart Configuration

Add this server to your `claude_desktop_config.json`:

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

Or connect the skill directly via Smithery:
```bash
smithery skill add whambammy/vector-graphics-pipeline-mcp
```
