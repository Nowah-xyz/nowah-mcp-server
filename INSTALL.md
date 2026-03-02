# Nowah Travel MCP Server — Installation Guide

The Nowah MCP server is available as a **remote HTTP server** — no local installation, Docker, or npm package required. Connect any MCP-compatible client to:

```
https://claw.nowah.xyz/mcp
```

Authentication is handled via OAuth (the server will prompt you to sign in on first connection).

---

## Quick Install (Universal)

Works with any MCP-compatible agent:

```bash
npx @anthropic-ai/add-mcp https://claw.nowah.xyz/mcp --name nowah-travel
```

---

## Platform-Specific Instructions

### Claude Code (CLI)

```bash
claude mcp add --transport http nowah-travel https://claw.nowah.xyz/mcp
```

### VS Code (Copilot)

```bash
code --add-mcp '{"type":"http","name":"nowah-travel","url":"https://claw.nowah.xyz/mcp"}'
```

Or add to `.vscode/mcp.json` in your project:

```json
{
  "servers": {
    "nowah-travel": {
      "type": "http",
      "url": "https://claw.nowah.xyz/mcp"
    }
  }
}
```

### Cursor

Add to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "nowah-travel": {
      "url": "https://claw.nowah.xyz/mcp"
    }
  }
}
```

### Windsurf

Add to your Windsurf MCP config:

```json
{
  "mcpServers": {
    "nowah-travel": {
      "serverUrl": "https://claw.nowah.xyz/mcp"
    }
  }
}
```

### Claude Desktop

Add to `claude_desktop_config.json`:

- **macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

```json
{
  "mcpServers": {
    "nowah-travel": {
      "type": "url",
      "url": "https://claw.nowah.xyz/mcp"
    }
  }
}
```

### Codex CLI (OpenAI)

```bash
codex mcp add nowah-travel --url https://claw.nowah.xyz/mcp
```

### Gemini CLI (Google)

Add to `~/.gemini/settings.json`:

```json
{
  "mcpServers": {
    "nowah-travel": {
      "httpUrl": "https://claw.nowah.xyz/mcp"
    }
  }
}
```

### ChatGPT

1. Go to **Settings** > **Apps and Connectors**
2. Click **Add MCP Server**
3. Enter the URL: `https://claw.nowah.xyz/mcp`

### JetBrains IDEs (IntelliJ, WebStorm, etc.)

1. Go to **Settings** > **AI Assistant** > **MCP Servers**
2. Click **Add** > **As JSON**
3. Paste:

```json
{
  "nowah-travel": {
    "type": "http",
    "url": "https://claw.nowah.xyz/mcp"
  }
}
```

---

## Available Tools

Once connected, you get access to 35+ travel tools:

| Category | Tools |
|----------|-------|
| **Flights** | `search_flights`, `search_locations`, `get_offer`, `book_flight`, `get_booking_fees` |
| **Hotels** | `search_hotels`, `get_hotel_quote`, `book_hotel` |
| **Trips** | `list_trips`, `get_trip`, `create_trip`, `update_trip`, `cancel_trip`, `get_trip_documents` |
| **Flight Tracking** | `get_flight_info`, `get_booking_tracking`, `get_airport_delays` |
| **Seatmaps** | `get_seat_info`, `get_seat_recommendations` |
| **Order Management** | `get_cancellation_quote`, `confirm_cancellation`, `get_order_services`, `add_order_services`, `create_change_request`, `confirm_flight_change` |
| **Payments** | `create_checkout_session`, `list_payment_methods`, `pay_with_saved_card`, `get_payment_status`, `manage_payment_method` |
| **Travel Info** | `get_visa_requirements`, `get_weather`, `convert_currency`, `get_safety_info` |
| **POIs & Itinerary** | `find_pois` (51M+ locations), `generate_itinerary` |
| **Claims** | `check_claim_eligibility`, `file_claim`, `list_claims` |
| **AI Agent** | `chat_with_agent` |
| **Meta** | `get_usage_stats`, `get_server_info` |

---

## Verify Connection

After setup, ask your AI assistant:

> "Use nowah to search for flights from NYC to London next week"

If the connection is working, it will call `search_flights` and return real results.

---

## Links

- **MCP Server**: https://claw.nowah.xyz/mcp
- **Dashboard & API Keys**: https://dash.nowah.xyz
- **Documentation**: https://docs.nowah.xyz
- **GitHub**: https://github.com/Nowah-xyz/nowah-mcp-server
