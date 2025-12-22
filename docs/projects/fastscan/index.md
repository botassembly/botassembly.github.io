---
description: High-performance text scanning library for agent workloads.
---

# Fastscan

> High-performance text scanning

Fastscan is a fast pattern matching library optimized for agent workloads. When your agent needs to search through large amounts of text quickly, Fastscan delivers.

## Quick Start

```bash
pip install fastscan
```

```python
from fastscan import Scanner

scanner = Scanner(patterns=["error", "warning", "critical"])
matches = scanner.scan(log_text)

for match in matches:
    print(f"Found '{match.pattern}' at position {match.start}")
```

## Features

- **High performance** - Optimized for speed
- **Multiple patterns** - Search for many patterns at once
- **Streaming** - Process large files without loading into memory
- **Agent-friendly** - Designed for AI agent use cases

## Use Cases

- Log analysis
- Code search
- Document processing
- Real-time monitoring

## Resources

- [:fontawesome-brands-github: GitHub](https://github.com/botassembly/fastscan)
- [API Reference](./api.md)
- [Performance Guide](./performance.md)

---

*Documentation is aggregated from the [fastscan repository](https://github.com/botassembly/fastscan). Updates appear nightly.*
