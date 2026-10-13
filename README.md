<img src="logo-400.png" alt="Samautomation Video logo" width="96" height="96">

# Samautomation Video MCP server

**Render an MP4 from your own images, clips, voice-over and timed captions. JSON to video.**

Remote MCP server: `https://samautomation.work/mcp` (Streamable HTTP) · Website: [samautomation.work](https://samautomation.work/)

## What it does

Samautomation Video renders a finished MP4 from media you supply: images, video clips, a voice-over and timed captions. The assistant validates the render plan first, creates one render after you confirm, and reads the job status and a shareable download link when it is done. It suits faceless channels, product clips and short-form batches.

It renders your own media. It does not generate paid AI footage or buy credits.

## Connect

- **Server URL:** `https://samautomation.work/mcp`
- **Transport:** Streamable HTTP
- **Authentication:** OAuth with PKCE (S256), dynamic client registration and client ID metadata documents, so MCP clients connect without manual setup. Sign in with your samautomation.work account.

**Claude (claude.ai, Desktop):** Settings → Connectors → Add custom connector → paste the server URL.

**Claude Code:**

```bash
claude mcp add --transport http samautomation-video https://samautomation.work/mcp
```

**Cursor, VS Code, Cline, Windsurf and other clients** (`mcp.json` / `cline_mcp_settings.json`):

```json
{
  "mcpServers": {
    "samautomation-video": {
      "type": "http",
      "url": "https://samautomation.work/mcp"
    }
  }
}
```

Cline uses `"type": "streamableHttp"`; see [llms-install.md](llms-install.md).

## Tools

| Tool | What it does |
|---|---|
| `account` | Plan and render allowance. |
| `validate_render` | Check a render plan before it runs. |
| `create_render` | Start one render (after confirmation). |
| `render_status / list_renders` | Job status, download link, recent renders. |

## Example prompts

- Turn these five images and this voice-over into a 30-second vertical video with captions.
- Is my render plan valid?
- Give me the download link of my last render.

## Links

- Website: https://samautomation.work/
- Documentation: https://samautomation.work/plugin/
- Privacy policy: https://samautomation.work/plugin/privacy/
- Terms: https://samautomation.work/plugin/terms/

## Keywords

JSON to video API, video rendering API, automated video, faceless YouTube, shorts generator, captions, voice-over video, MP4 render.

Nederlands: video maken met AI, video automatisering, shorts maken, ondertiteling, voice-over video, video API.

## More MCP servers by Samautomation

- [Scamchecker.nl](https://scamchecker.nl/): Check a suspicious email, SMS, WhatsApp message or link for scam signals (Netherlands, Belgium). ([listing](https://github.com/smrht/scamchecker-mcp))
- [Klussenbeheer](https://samdesk.nl/klussenbeheer/): Job management for Dutch service companies: jobs, customers, planning, quotes and invoices. ([listing](https://github.com/smrht/klussenbeheer-mcp))
- [Muziek maken met AI](https://muziekmakenmetai.nl/): Make an original song from a prompt or your own lyrics. Two versions per song, MP3 download. ([listing](https://github.com/smrht/muziekmakenmetai-mcp))
- [Beheer je WP](https://beheerjewp.nl/): Manage a WordPress site from your AI assistant: read, search, propose edits, Search Console data. ([listing](https://github.com/smrht/beheerjewp-mcp))
- [UlazAI Media](https://ulazai.com/): Create private AI images with your UlazAI account: pick a model, confirm, generate, download. ([listing](https://github.com/smrht/ulazai-mcp))
- [Backlinkswinkel](https://backlinkswinkel.nl/): Search Dutch websites for backlinks, check metrics and prices, order after confirmation, track. ([listing](https://github.com/smrht/backlinkswinkel-mcp))
- [Backlinksbeheer](https://backlinksbeheer.nl/): Read your stored backlinks, link checks and lost-link alerts per domain. Read-only. ([listing](https://github.com/smrht/backlinksbeheer-mcp))
- [PDF Samenvoegen](https://pdfsamenvoegen.nl/): Merge your own PDFs in a confirmed order and get one downloadable PDF. ([listing](https://github.com/smrht/pdfsamenvoegen-mcp))
- [Diamond Painting Converter](https://diamondpaintingconverter.com/): Find your purchased diamond painting patterns and download the PDF with DMC colour legend. ([listing](https://github.com/smrht/diamondpaintingconverter-mcp))
- [Nummerschilderen.com shop advisor](https://nummerschilderen.com/): Search paint-by-number kits, get size and price advice for your own photo, shop info. No login. ([listing](https://github.com/smrht/nummerschilderen-mcp))
- [DiamondPaintingWinkel.nl shop advisor](https://diamondpaintingwinkel.nl/): Search diamond painting kits, get size and price advice for your own photo, shop info. No login. ([listing](https://github.com/smrht/diamondpaintingwinkel-mcp))
- [AI Rechtshulp](https://ai-rechtshulp.nl/): Search Dutch and EU case law with ECLI sources and verify quotes against the judgment. ([listing](https://github.com/smrht/ai-rechtshulp-mcp))
- [SamDesk Support](https://samdesk.nl/support/plugin/): Read your SamDesk support inbox, find customer agreements and draft replies. Read-only. ([listing](https://github.com/smrht/samdesk-support-mcp))

## Publisher

Samautomation, Wognum, the Netherlands · https://samautomation.work

This repository holds the public listing (README, `server.json`, install notes). The server itself is hosted by the publisher; there is nothing to install or build.
