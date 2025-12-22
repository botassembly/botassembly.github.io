---
description: Agent-native ETL framework. NDJSON pipelines with plugins for formats and protocols.
---

# jn

> Agent-native ETL - NDJSON pipelines for AI

jn is an ETL framework designed for AI agent workflows. It uses NDJSON (newline-delimited JSON) as its native format and provides plugins for common formats (xlsx, markdown, xml) and protocols (gmail, mcp, http).

## Quick Start

```bash
# Download the binary
make download  # From botassembly/workspace

# Or install via pip
pip install jn
```

```bash
# Convert Excel to JSON
jn xlsx input.xlsx | jn query '.[] | select(.status == "active")'

# Fetch and transform
jn http GET https://api.example.com/data | jn query '.items[]'
```

## Features

- **NDJSON native** - One JSON object per line, streaming-friendly
- **Format plugins** - xlsx, markdown, xml, csv, and more
- **Protocol plugins** - HTTP, Gmail, MCP servers
- **Built-in query** - Uses `zq` for JSON querying
- **Composable** - Unix pipes for complex workflows

## CLI Tools

| Command | Description |
|---------|-------------|
| `jn` | Main entry point |
| `jn-edit` | JSON manipulation |
| `zq` | JSON/Zed querying |
| `todo` | Task management CLI |

## Resources

- [:fontawesome-brands-github: GitHub](https://github.com/botassembly/jn)
- [CLI Reference](./cli.md)
- [Plugin Guide](./plugins.md)

---

*Documentation is aggregated from the [jn repository](https://github.com/botassembly/jn). Updates appear nightly.*
