# Nowah Travel MCP Server

AI-powered travel assistant for any MCP-compatible client — search and book flights, hotels, explore 51M+ points of interest, track flights, check visa requirements, weather, safety info, and more.

**Server URL:** `https://claw.nowah.xyz/mcp`

No local installation required — connect directly via HTTP.

## Quick Start

```bash
npx @anthropic-ai/add-mcp https://claw.nowah.xyz/mcp --name nowah-travel
```

Or platform-specific:

| Platform | Command |
|----------|---------|
| **Claude Code** | `claude mcp add --transport http nowah-travel https://claw.nowah.xyz/mcp` |
| **VS Code** | `code --add-mcp '{"type":"http","name":"nowah-travel","url":"https://claw.nowah.xyz/mcp"}'` |
| **Cursor** | Add to `~/.cursor/mcp.json` ([see details](INSTALL.md#cursor)) |
| **Claude Desktop** | Add to `claude_desktop_config.json` ([see details](INSTALL.md#claude-desktop)) |
| **Windsurf** | Add to MCP config ([see details](INSTALL.md#windsurf)) |
| **Codex CLI** | `codex mcp add nowah-travel --url https://claw.nowah.xyz/mcp` |
| **Gemini CLI** | Add to `~/.gemini/settings.json` ([see details](INSTALL.md#gemini-cli-google)) |
| **ChatGPT** | Settings > Apps and Connectors > Add MCP Server ([see details](INSTALL.md#chatgpt)) |
| **JetBrains** | Settings > AI Assistant > MCP ([see details](INSTALL.md#jetbrains-ides-intellij-webstorm-etc)) |

See [INSTALL.md](INSTALL.md) for full platform instructions.

## Available Tools (35+)

### Search & Discovery
| Tool | Description |
|------|-------------|
| `search_flights` | Search flights between airports with flexible dates and passengers |
| `search_locations` | Find airport IATA codes by city or airport name |
| `get_offer` | Get detailed pricing for a specific flight offer |
| `search_hotels` | Search hotels by city, dates, and guest count |
| `get_hotel_quote` | Get a detailed quote for a hotel room |
| `find_pois` | Discover points of interest from 51M+ locations worldwide |
| `generate_itinerary` | Generate a day-by-day travel itinerary |

### Booking & Trips
| Tool | Description |
|------|-------------|
| `book_flight` | Book a flight offer for passengers |
| `book_hotel` | Book a hotel room |
| `get_booking_fees` | Get fee breakdown before booking |
| `list_trips` | List all user trips |
| `get_trip` | Get detailed trip information |
| `create_trip` | Create a new trip |
| `update_trip` | Update trip details |
| `cancel_trip` | Cancel a trip |
| `get_trip_documents` | Get booking documents (e-tickets, confirmations) |

### Order Management
| Tool | Description |
|------|-------------|
| `get_cancellation_quote` | Get refund quote before cancelling |
| `confirm_cancellation` | Confirm a flight cancellation |
| `get_order_services` | View available add-ons (bags, seats, meals) |
| `add_order_services` | Add services to an existing booking |
| `create_change_request` | Request flight date/route changes |
| `confirm_flight_change` | Confirm a flight change |

### Flight Tracking
| Tool | Description |
|------|-------------|
| `get_flight_info` | Track a flight by flight number |
| `get_booking_tracking` | Track flights from a booking |
| `get_airport_delays` | Check current delay status at an airport |

### Seatmap Intelligence
| Tool | Description |
|------|-------------|
| `get_seat_info` | Get detailed seatmap and seat information |
| `get_seat_recommendations` | AI-powered seat recommendations based on preferences |

### Payments
| Tool | Description |
|------|-------------|
| `create_checkout_session` | Create a payment checkout session |
| `list_payment_methods` | List saved payment methods |
| `pay_with_saved_card` | Pay using a saved card |
| `get_payment_status` | Check payment status |
| `manage_payment_method` | Add or remove payment methods |

### Travel Information
| Tool | Description |
|------|-------------|
| `get_visa_requirements` | Check visa requirements between countries |
| `get_weather` | Current weather and forecasts for any location |
| `convert_currency` | Convert between currencies with live rates |
| `get_safety_info` | Travel safety information for a country |

### Claims & Support
| Tool | Description |
|------|-------------|
| `check_claim_eligibility` | Check if a disruption qualifies for compensation |
| `file_claim` | File a compensation claim |
| `list_claims` | View claim status |

### AI & Meta
| Tool | Description |
|------|-------------|
| `chat_with_agent` | Chat with the Nowah AI travel agent |
| `get_usage_stats` | Get API usage statistics |
| `get_server_info` | Server version and capabilities |

## Resources & Prompts

The server also exposes:

- **Resource** `nowah://trips` — List of all user trips
- **Prompt** `plan_trip` — Generate a complete trip plan with flights, hotels, and itinerary
- **Prompt** `check_travel_requirements` — Check visa, weather, safety, and customs for a destination

## Authentication

The server uses OAuth. On first connection, you'll be prompted to sign in via your browser. Sessions persist across reconnections.

## Links

- [Install Guide](INSTALL.md)
- [Dashboard & API Keys](https://dash.nowah.xyz)
- [Documentation](https://docs.nowah.xyz)
- [Nowah App](https://nowah.xyz)
