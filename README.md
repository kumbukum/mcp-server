# Kumbukum MCP Server

> Persistent memory for AI tools. Your AI forgets everything. Kumbukum doesn't.

Kumbukum is a hosted MCP server that gives any MCP-compatible AI tool access to a shared, persistent memory store. Set it up once, use it across Claude, Cursor, ChatGPT, and any other MCP client.

## Features

- **Persistent memory** — store notes, preferences, decisions, and context across sessions
- **Semantic search** — AI retrieves the right memory using natural language
- **Cross-tool** — one memory store, accessible from Claude, Cursor, ChatGPT, and more
- **Tags & organisation** — tag memories by project, topic, or type
- **Two data centers** — US (`mcp.kumbukum.com`) and EU (`mcp-eu.kumbukum.com`)

## Quick Start

1. Sign up at [kumbukum.com](https://kumbukum.com) to get your API key
2. Add to your MCP client config:

```json
{
  "mcpServers": {
    "kumbukum": {
      "url": "https://mcp.kumbukum.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

### EU Data Center

```json
{
  "mcpServers": {
    "kumbukum": {
      "url": "https://mcp-eu.kumbukum.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

## Available Tools

| Tool | Description |
|---|---|
| `store_memory` | Save a memory with title, content, and optional tags |
| `recall_memory` | Search memories using natural language |
| `create_note` | Create a structured note or document |
| `search_notes` | Search notes by keyword or semantic query |
| `search_knowledge` | Search across both notes and memories in one query |
| `list_memories` | List all memories with optional tag filter |
| `update_memory` | Update an existing memory |
| `delete_memory` | Delete a memory by ID |

## Authentication

All requests require a Bearer token in the `Authorization` header. Get your API key at [kumbukum.com](https://kumbukum.com).

## Data Centers

| Region | URL |
|---|---|
| US | `https://mcp.kumbukum.com/mcp` |
| EU | `https://mcp-eu.kumbukum.com/mcp` |

## License

AGPL-3.0
