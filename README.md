# Nowah Travel MCP Server

Your personal AI travel concierge. Search and book flights across 300+ airlines, find hotels worldwide, explore 116M+ points of interest, track live flights, get AI-powered seat recommendations, check visa requirements for any passport, live weather forecasts, currency conversion, travel safety advisories, and full trip lifecycle management — all from your favorite AI coding assistant or agent.

**Server URL:** `https://claw.nowah.xyz/mcp`

No local installation, no Docker, no npm package. Connect directly via HTTP and start planning trips in seconds.

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

## What You Can Do

- "Find me the cheapest flight from NYC to Tokyo in April"
- "Book a hotel near the Eiffel Tower for 3 nights"
- "What are the visa requirements for a US passport holder visiting Vietnam?"
- "Track flight BA117 — is it on time?"
- "Plan a 5-day itinerary in Barcelona with local restaurants and hidden gems"
- "What's the weather like in Bali next week?"
- "Find the best seat on my upcoming Emirates A380 flight"
- "Cancel my London booking and show me the refund amount"

## Available Tools (35+)

### Search & Discovery
| Tool | Description |
|------|-------------|
| `search_flights` | Search flights across 300+ airlines with flexible dates, multi-city, and cabin class options |
| `search_locations` | Find airport IATA codes by city or airport name |
| `get_offer` | Get detailed pricing breakdown for a specific flight offer |
| `search_hotels` | Search hotels worldwide by city, dates, and guest count |
| `get_hotel_quote` | Get a detailed quote with room types, amenities, and cancellation policy |
| `find_pois` | Discover restaurants, landmarks, activities from 116M+ points of interest worldwide |
| `generate_itinerary` | Generate a personalized day-by-day travel itinerary for any destination |

### Booking & Trip Management
| Tool | Description |
|------|-------------|
| `book_flight` | Book a flight with passenger details and payment |
| `book_hotel` | Book a hotel room |
| `get_booking_fees` | Get full fee breakdown before committing to a booking |
| `list_trips` | List all trips for the authenticated user |
| `get_trip` | Get complete trip details with bookings, documents, and status |
| `create_trip` | Create a new trip to organize bookings |
| `update_trip` | Update trip details, dates, or notes |
| `cancel_trip` | Cancel a trip and all associated bookings |
| `get_trip_documents` | Retrieve e-tickets, booking confirmations, and travel documents |

### Order Management
| Tool | Description |
|------|-------------|
| `get_cancellation_quote` | Get refund amount and policy before cancelling |
| `confirm_cancellation` | Confirm a flight cancellation and process refund |
| `get_order_services` | View available add-ons — extra bags, seat upgrades, meals, lounge access |
| `add_order_services` | Add services to an existing booking |
| `create_change_request` | Request flight date or route changes |
| `confirm_flight_change` | Confirm and pay for a flight change |

### Live Flight Tracking
| Tool | Description |
|------|-------------|
| `get_flight_info` | Track any flight in real-time by flight number |
| `get_booking_tracking` | Track all flights associated with a booking |
| `get_airport_delays` | Check current delay and disruption status at any airport |

### Seatmap Intelligence
| Tool | Description |
|------|-------------|
| `get_seat_info` | Get detailed seatmap with legroom, recline, power, and window positions |
| `get_seat_recommendations` | AI-powered seat recommendations based on your preferences |

### Payments
| Tool | Description |
|------|-------------|
| `create_checkout_session` | Create a secure payment checkout session |
| `list_payment_methods` | List saved payment methods |
| `pay_with_saved_card` | Pay using a saved card |
| `get_payment_status` | Check payment status and transaction details |
| `manage_payment_method` | Add or remove payment methods |

### Travel Intelligence
| Tool | Description |
|------|-------------|
| `get_visa_requirements` | Check visa requirements between any two countries |
| `get_weather` | Current conditions and multi-day forecasts for any location |
| `convert_currency` | Convert between 150+ currencies with live exchange rates |
| `get_safety_info` | Travel safety advisories, health risks, and local laws for any country |

### Flight Disruption Claims
| Tool | Description |
|------|-------------|
| `check_claim_eligibility` | Check if a delay or cancellation qualifies for compensation |
| `file_claim` | File a compensation claim for a disrupted flight |
| `list_claims` | View all claims and their status |

### AI Concierge
| Tool | Description |
|------|-------------|
| `chat_with_agent` | Chat with the Nowah AI travel concierge for complex planning |
| `get_usage_stats` | Get API usage statistics |
| `get_server_info` | Server version and capabilities |

## Resources & Prompts

The server also exposes MCP resources and prompts for richer agent workflows:

- **Resource** `nowah://trips` — Live list of all user trips
- **Prompt** `plan_trip` — Generate a complete trip plan with flights, hotels, and day-by-day itinerary
- **Prompt** `check_travel_requirements` — Check visa, weather, safety, and customs for any destination

## Authentication

The server uses OAuth. On first connection, your MCP client will open a browser window to sign in. Sessions persist across reconnections — you only need to authenticate once.

## Links

- [Install Guide](INSTALL.md)
- [Dashboard & API Keys](https://dash.nowah.xyz)
- [Documentation](https://docs.nowah.xyz)
- [Nowah App](https://nowah.xyz)
