# Installing Samautomation Video in Cline

This is a hosted remote MCP server. There is nothing to clone, build or install.

Add this entry to `cline_mcp_settings.json`:

```json
{
  "mcpServers": {
    "samautomation-video": {
      "type": "streamableHttp",
      "url": "https://samautomation.work/mcp",
      "disabled": false
    }
  }
}
```

Authentication: OAuth with PKCE (S256), dynamic client registration and client ID metadata documents, so MCP clients connect without manual setup. Sign in with your samautomation.work account.

With OAuth, Cline opens the sign-in page the first time a tool is used; approve access and return to Cline.

Check the connection by asking: "Turn these five images and this voice-over into a 30-second vertical video with captions."
