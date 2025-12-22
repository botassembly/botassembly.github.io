---
description: Specialized agent loop implementations built on innerloop. Includes SenpaiKit learning loop.
---

# Pyxies

> Specialized agent loops - helpful sprites for your agents

Pyxies packages common agent patterns as reusable loops. Each "pyxie" solves a specific type of agent problem, built on the solid foundation of innerloop.

## SenpaiKit

The flagship kit. A learning loop that improves through use:

- **Nudge** - Gentle corrections that inform future behavior
- **Approach** - Strategies for handling situations
- **Skill** - Concrete capabilities the agent develops

```python
from pyxies import SenpaiKit

kit = SenpaiKit(
    domain="code-review",
    protocols=["github", "jira"]
)

# Agent learns from corrections
kit.run("Review this PR", context=pr_data)
kit.nudge("Focus more on security implications")
```

## Available Kits

| Kit | Description | Status |
|-----|-------------|--------|
| **SenpaiKit** | Learning loop with nudge/approach/skill lifecycle | Active |
| **Tool-calling** | Optimized for tool-heavy workflows | Planned |
| **Conversation** | Multi-turn dialogue management | Planned |
| **Research** | Information gathering and synthesis | Planned |

## Key Concepts

### Protocol Integration

Pyxies uses protocols for domain memory - persistent knowledge about how to operate in specific contexts (GitHub, Jira, email, etc.).

### Cold Start

New domains start with minimal knowledge. The senpai loop handles cold start gracefully, learning from each interaction.

## Resources

- [:fontawesome-brands-github: GitHub](https://github.com/botassembly/pyxies)
- [SenpaiKit Deep Dive](./senpai.md)
- [Creating Custom Kits](./custom.md)

---

*Documentation is aggregated from the [pyxies repository](https://github.com/botassembly/pyxies). Updates appear nightly.*
